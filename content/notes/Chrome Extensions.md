---
title: "Chrome Extensions"
---
My notes on how to work with Chrome Extensions

## Manifest.json

Manifest.json is similar to your config.json or package.json in most projects
Configure your icon & starting file

Functionality of each line of manifest.json

```json
{
  "manifest_version": 3, // what version you are using (2 or 3)
  "name": "Name", // name of your extension
  "description": "Description", // description of your extension
  "version": "1.0", // version of your extension (unnecessary unless publishing)
  "action": {
    "default_popup": "PATH" // default 
  },
  "host_permissions": ["<all_urls>"] // allows http calls to be made to all URLs
}

```
## Button

```html
<button id="ID">text</button>
```

```js
document.addEventListener('DOMContentLoaded', function(){
	document.getElementById("ID").addEventListener("click", funcName)
})
```

*Warning the script file has to be attached*

To add more than 1 button add to addEventListener

This is how to configure a button using an event listener

## HTTP Calls

define the function passed in the eventListener and have it use [fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

Example Usage:

```js
async function req() {
	fetch("URL")
	.then((r) => r.json())
	.then((data) => console.log(data))
}
```
Now you can pass the js function in the event listener