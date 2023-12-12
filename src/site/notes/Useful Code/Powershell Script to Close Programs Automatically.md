---
{"wordcount":0,"dg-publish":true,"permalink":"/useful-code/powershell-script-to-close-programs-automatically/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-13T03:32:57.590+05:30","updated":"2023-12-13T03:43:46.827+05:30"}
---

🧶 Tags - #Code
# [[Useful Code/Powershell Script to Close Programs Automatically\|Powershell Script to Close Programs Automatically]]
==2023-12-13 - 03:33==
```powershell
# Set the idle time threshold in seconds (e.g., 300 seconds = 5 minutes)
$idleThreshold = 300

# Get the start time and initialize the idle time counter
$startTime = Get-Date
$idleTime = 0

# Loop indefinitely
while ($true) {
    # Get the current idle time
    $currentIdle = (New-Object -ComObject Shell.Application).Namespace('Application').Items() | ForEach-Object { $_.GetFolder.DisplayOf }

    # If the current idle time is greater than the threshold, start counting
    if ($currentIdle -gt $idleTime) {
        $idleTime = $currentIdle
    } else {
        # If the system is idle for the specified duration, close all applications
        if ((New-TimeSpan -Start $startTime).TotalSeconds -ge $idleThreshold) {
            Stop-Process -Name *
            break
        }
    }

    # Sleep for a second before checking again
    Start-Sleep -Seconds 1
}
```

> [!hint]  run this script:
1. Open Notepad or any text editor.
2. Copy and paste the script above into the text editor.
3. Save the file with a `.ps1` extension (e.g., `CloseAppsOnIdle.ps1`).

>[! hint] To execute the script:
1. Right-click on the saved PowerShell script file (`CloseAppsOnIdle.ps1`).
2. Choose "Run with PowerShell" from the context menu.

Please note that running scripts directly may require adjusting your system's execution policy. You can set the PowerShell execution policy to allow script execution by opening PowerShell as an administrator and running `Set-ExecutionPolicy RemoteSigned` (choose 'Yes' when prompted).

Always be cautious when using scripts that terminate processes, as it will forcefully close all applications without saving any unsaved data. Make sure all important work is saved before running such scripts.

>[! note] Task Scheduling
you can set up a script to run automatically on your PC by creating a scheduled task in Windows Task Scheduler. Here's a step-by-step guide to adding the PowerShell script as a scheduled task:

**Open Task Scheduler**:
- Press `Win + R` to open the Run dialog.
- Type `taskschd.msc` and press Enter.

**Create a Basic Task**:  
- In Task Scheduler, click on `Create Basic Task…` in the right-hand pane.
- Give your task a name and description. Click `Next`.

**Trigger Configuration**:
- Choose the trigger that suits your requirement (e.g., `When the computer starts`). Click `Next`.

**Action Configuration**:
- Select `Start a program` and click `Next`.

**Program/Script and Arguments**:
- In the "Program/script" field, browse and select `powershell.exe`.
- In the "Add arguments" field, enter the path to your PowerShell script (e.g., `C:\path\to\your\script\CloseAppsOnIdle.ps1`).
- Click `Next`.

**Summary**:
- Review your settings. If everything looks correct, click `Finish`.

**Task Properties (Optional)**:
- You can further customize the task by right-clicking on it in Task Scheduler and choosing `Properties`.
- Adjust settings in the `General`, `Triggers`, `Actions`, `Conditions`, and `Settings` tabs as needed.

This scheduled task will run your PowerShell script under the specified conditions. Ensure that the script has appropriate permissions to run and that the execution policy in PowerShell allows the script to be executed. Adjust the task settings as per your preferences and security requirements.

Please note that forcibly closing applications can result in data loss if there are unsaved changes. Ensure that all important work is saved before the scheduled task runs.