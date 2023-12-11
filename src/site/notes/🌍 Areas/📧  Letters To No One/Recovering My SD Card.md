---
{"dg-publish":true,"permalink":"/areas/letters-to-no-one/recovering-my-sd-card/","noteIcon":"1"}
---

🧶 Tags - #Letterstonoone

# [[🌍 Areas/📧  Letters To No One/Recovering My SD Card\|Recovering My SD Card]]
==2023-06-22 - 13:06==

---
So my SD card was showing that it's corrupted. A similar thing happened to me 2 years ago, just after Harshi got married. I had all the pictures in my cellphone and it was all gone suddenly.

So I thought, I should buy a good quality card that won't corrupt in a few years. So I bought a 64gb Samsung class 10 card.

Really good transfer speeds and all. I was happy with it until it decided to just corrupt a few days ago. It worked for just 2 years, and remember I'm not transferring a lot of files and huge data dumps in this, I had just gradually filled it up to 40gb and kept it that way.

Now that my data was gone, I looked up a few options as to how can I recover it. There are quite a lot of options when it comes to data recovery softwares. I downloaded a bunch of them, I think around 8 but, none of them was able to get it done.

Maybe because I'm using Linux and most of them are designed to be used on windows. And it's really annoying because you can't do anything about it. I was scared to format as I would lose any chance of getting any data back, and even if I do format it, there is no guarantee that it'll start working again.

But I knew that windows software was not working well on my PC but even using some of the Linux based software I couldn't get it done, but then I read about using the terminal to try to recover the data. So, after digging a bit around that I thought let's give it a try and see what happens.

### Here's what I did -
A thread suggested using <mark style="background: #FF5582A6;">'lsblk'</mark> to first see all the drives present in the system. My card was mounted as <mark style="background: #FF5582A6;">'mmcblk1p1'.</mark>
Then use the command <mark style="background: #FF5582A6;">'sudo umount /mnt/sdcard'</mark> to unmount the card if it is mounted.
Then finally use <mark style="background: #FF5582A6;">'sudo fsck -y /dev/mmcblk1p1'</mark> to try and repair the error on the card.

It took <mark style="background: #FFB86CA6;">4 min 20s to repair over 27,000</mark> files with error and got the data. I still need to check if I'm missing something, but I don't think that's the case as I can see all the files present. I can see the pictures, play the videos, etc etc.

## You Can Copy From Here
```bash
lsblk
sudo fsck -y /dev/mmcblk1p1
```

The first thing after getting all the files back was to create a backup. There goes my 40 some GBs of hard drive space. I really need to buy a HDD to store these things.

I'm thinking about building a NAS with 2 identical drives. So that I can have a second backup in case one drive fails. Some kind of [RAID setup](https://www.howtogeek.com/162676/how-to-use-multiple-disks-intelligently-an-introduction-to-raid/) will be need with [TrueNAS](https://www.truenas.com/) software.

One thing I learned from this experience is to never trust storage devices especially SD cards even if they are expensive and not used much. And make sure to create multiple backups on the same thing.