# usage-time-checker
It is simple script code, stopwatch using browser DOM API⏰

## Usage

### 1. Copy Script

```js
function changeFavicon(src) {
    let link = document.querySelector("link[rel~='icon']");

    if (!link) {
        link = document.createElement('link');
        link.rel = 'icon';
        document.getElementsByTagName('head')[0].appendChild(link);
    }

    link.href = src;
}


let count = 0;

function getElapsedTime(second) {
  const hours = Math.floor(second / 3600);
  const minutes = Math.floor((second - hours * 3600) / 60);
  const seconds = second - (hours * 3600 + minutes * 60);
  
  return [fillZeroToNumber(hours), fillZeroToNumber(minutes), fillZeroToNumber(seconds)].join(':');
}

const fillZeroToNumber = (number) => number.toString().padStart(2, '0');

setInterval(() => {
  ++count;
  document.title = getElapsedTime(count);
}, 1000);

document.title = getElapsedTime(count);

changeFavicon('https://png.pngtree.com/png-vector/20190216/ourlarge/pngtree-cute-baby-dog-face-vector-png-image_550082.jpg');
```

### 2. Open any website and open Inspector(F12, cmd(⌘) + shift + i, fn + F12)

### 3. Paste copied text of first step

### 4. Finish, Now you can check your usage time on borwser tab!

Useful Study, Coding, Youtube Watching, Game, etc...

## Additional You can change Favicon you want.

In code, last line. Just modify inside single quote.

`changeFavicon('https://png.pngtree.com/png-vector/20190216/ourlarge/pngtree-cute-baby-dog-face-vector-png-image_550082.jpg');`

Change link you want!

## ScreenShot

![ScreenShot](https://user-images.githubusercontent.com/48552260/106499362-d81cb780-6503-11eb-8a31-974c8adfc8a2.png)
