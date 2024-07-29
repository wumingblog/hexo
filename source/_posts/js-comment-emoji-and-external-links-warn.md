---
abbrlink: ''
categories: []
date: '2024-07-29T18:12:41.639512+08:00'
tags: []
title: JS实现评论表情包及站外链接提醒
updated: '2024-07-29T18:12:40.673+08:00'
---
## 评论表情包

> **OSS文件已删除，请自行替换!**
> 替换`textarea`成评论框的ID

```html
<span id="sticker_box"></span>
<a onclick="toggleStickerBox()" a="#">表情</a>
```

```js
<script>const stickers = [
        //这里填你的图片
      '001', '002', '003', '004', '005', '006', '007', '008'
    ];
    const stickerBox = document.getElementById('sticker_box');
    stickers.forEach(sticker => {
      const button = document.createElement('button');
      button.className = 'sk';
      button.onclick = function() {
        sticker01(sticker);
      };

      const img = document.createElement('img');
      //这里填图片目录
      img.src = `//oss.wuminboke.site/sticker/${sticker}.webp`;
      img.style.height = '50px';
      img.style.width = '50px';
      img.loading = "lazy";

      button.appendChild(img);
      stickerBox.appendChild(button);
    });
    function toggleStickerBox() {
      const divToToggle = document.getElementById('sticker_box');
      divToToggle.style.display = divToToggle.style.display === 'none' ? 'block' : 'none';
    }
    function sticker01(stickernum) {
      const textarea1 = document.getElementById('textarea');
      //这里填图片目录
      textarea1.value += `<img src="//oss.wuminboke.site//sticker/${stickernum}.webp" height="100px" width="100px">`;
    }</script>
```

## 站外链接提醒

> 把`wuminboke.site`替换成自己域名可直接使用

```js
<script>function links(){const t=document.querySelectorAll("#post-body a"),e=["#"],n=[{url:"github.com",tag:" - Github"},{url:"t.me",tag:" - Telegram"},{url:"wuminboke.site",tag:""}];for(let u=0;u<t.length;u++){const l=t[u],o=l.href;if(e.includes(o))continue;const i=n.find((t=>o.includes(t.url)));l.innerText+=i?i.tag:" - 站外链接"}}links();</script>
```

