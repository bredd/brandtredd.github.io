---
title: Cyber Camp 2025
---
Download this blank web page and save it to your computer:

* <a href="/cc/page.html" download="page.html">Blank Web Page</a>

Or, you can copy and paste this text.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Cyber Camp - Web Tricks</title>

    <style>

    </style>
</head>
<body>
    <h1>Cyber Camp - Web Tricks</h1>

    <script>

    </script>
</body>
</html>
```

Open the file in Notepad (or any other text editor) and add the following right under the `<h1>` title.

```html
<button id="win">Click to win $1 million.</button>
```

Save your changes and open the page in your web browser by double-clicking on the file.

But wait! We don't have a million dollars to give away. So, we need to add some stuff.

First, add this to the `<style>` section of your page. (Don't include the `<style>` tags.)

```html
<style>
#win {
    position: fixed;
    left: 10em;
    top: 10em;
    transition-duration: 0.3s;
}
@keyframes shade {
    0% {
        opacity: 100%;
    }
    50% {
        opacity: 0%;
    }
    100% {
        opacity: 100%;
    }
}

h1 {
    animation-name: shade;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    position: absolute;
}
</style>
```

Refresh the page and you will see how your button has moved to 10 spaces from the top and 10 spaces from the left.

Now, add this to the `<script>` section of your page.

```html
<script>
function onMouseOver(e) {
    const style = e.target.style;
    if (style.left == "30em") style.left = "10em";
    else style.left = "30em";
}
document.getElementById("win").onmouseover = onMouseOver;
</script>
```

Now, refresh the page and try to click the button!

You can experiment with things. Change the `transition-duration`. Change the positions. Or change the text on the button.

**Here is what your whole page should look like at this point:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Cyber Camp - Web Tricks</title>

    <style>
#win {
    position: fixed;
    left: 10em;
    top: 10em;
    transition-duration: 0.3s;
}
    </style>
</head>
<body>
    <h1>Cyber Camp - Web Tricks</h1>
    <button id="win">Click to win $1 million.</button>

    <script>
function onMouseOver(e) {
    const style = e.target.style;
    if (style.left == "30em") style.left = "10em";
    else style.left = "30em";
}
document.getElementById("win").onmouseover = onMouseOver;
    </script>
</body>
</html>
```

## Animation

Add this to the `<style>` section of your page:

```css
@keyframes shade {
    0% {
        opacity: 100%;
    }
    50% {
        opacity: 0%;
    }
    100% {
        opacity: 100%;
    }
}

h1 {
    animation-name: shade;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    position: absolute;
}
```

Save and refresh the page to see what happens!

You can experiment with the keyframes. For example, try setting the `left:` or `top:` properties to make the title move around. Or try setting `color:` to make the color change.

**Here is what your whole page should look like at this point:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Cyber Camp - Web Tricks</title>

    <style>
#win {
    position: fixed;
    left: 10em;
    top: 10em;
    transition-duration: 0.3s;
}

@keyframes shade {
    0% {
        opacity: 100%;
    }
    50% {
        opacity: 0%;
    }
    100% {
        opacity: 100%;
    }
}

h1 {
    animation-name: shade;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    position: absolute;
}
    </style>
</head>
<body>
    <h1>Cyber Camp - Web Tricks</h1>
    <button id="win">Click to win $1 million.</button>

    <script>
function onMouseOver(e) {
    const style = e.target.style;
    if (style.left == "30em") style.left = "10em";
    else style.left = "30em";
}
document.getElementById("win").onmouseover = onMouseOver;
    </script>
</body>
</html>
```

## Videoception

Add a button and a video panel to the page by putting this right under the existing button:

```html
<button onclick="videoception()">Videoception!</button>
<video id="vid" muted autoplay style="position: fixed; top:15em; left: 5em; width: 60em; height: 35em;"></video>
```

Now add this to the script part of your page:
```js
async function videoception() {
    let mediaStream = await navigator.mediaDevices.getDisplayMedia({video: {cursor: "always"}, audio: true});
    document.getElementById("vid").srcObject = mediaStream;
}
```

Save and refresh the page and then click on "Videoception!" When it asks what to share, select `Entire Screen` and then click `Share`.

**At this point, your page should look something like this:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Cyber Camp - Web Tricks</title>

    <style>
#win {
    position: fixed;
    left: 10em;
    top: 10em;
    transition-duration: 0.3s;
}

@keyframes shade {
    0% {
        opacity: 100%;
    }
    50% {
        opacity: 0%;
    }
    100% {
        opacity: 100%;
    }
}

h1 {
    animation-name: shade;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    position: absolute;
}
    </style>
</head>
<body>
    <h1>Cyber Camp - Web Tricks</h1>
    <button id="win">Click to win $1 million.</button>
    <button onclick="videoception()">Videoception!</button>
    <video id="vid" muted autoplay style="position: fixed; top:15em; left: 5em; width: 60em; height: 35em;"></video>

    <script>
function onMouseOver(e) {
    const style = e.target.style;
    if (style.left == "30em") style.left = "10em";
    else style.left = "30em";
}
document.getElementById("win").onmouseover = onMouseOver;

async function videoception() {
    let mediaStream = await navigator.mediaDevices.getDisplayMedia({video: {cursor: "always"}, audio: true});
    document.getElementById("vid").srcObject = mediaStream;
}
   </script>
</body>
</html>
```
