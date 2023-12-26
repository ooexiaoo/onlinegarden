---
{"dg-publish":true,"wordcount":0,"permalink":"/useful-code/responsive-embed-code-for-video/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-10T19:38:21.834+05:30","updated":"2023-12-17T22:04:24.509+05:30"}
---

🧶 Tags:: #code #Reference_Notes 
# [[Useful Code/Responsive Embed Code For Video\|Responsive Embed Code For Video]]
==2023-12-13 - 03:44==
```HTML
<div style="position: relative; padding-bottom: 56.25%; /* 16:9 aspect ratio */">
  <iframe
    src=""
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    allow="autoplay; fullscreen"
    frameborder="0"
    scrolling="no"
  ></iframe>
</div>
```

You can add the video embed link in **"src"**, works well for YouTube videos.