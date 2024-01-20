---
title: "Chrome Extensions"
---
My notes on how to work with Chrome Extensions

## Manifest.json

Manifest.json is similar to your config.json or package.json in most projects
Configure your icon & starting file
## Button

```html
<button id="ID">text</button>
```

```js
document.addEventListener('DOMContentLoaded', function(){
	document.getElementById("ID").addEventListener("click", name)
})
```

*Warning the script file has to be attached*

To add more than 1 button add to addEventListener

This is how to configure a button using an event listener
