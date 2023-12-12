---
{"dg-publish":true,"permalink":"/useful-code/responsive-embed-code-for-video/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-10T19:38:21.834+05:30","updated":"2023-12-10T19:40:36.279+05:30"}
---


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

You can add the video embed link in **"src"**, works well for YouTube videos