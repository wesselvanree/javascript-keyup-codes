# Javascript Keyboard event Tool

A tool for quickly getting the javascript `keydown`-event properties. This tool is meant for developers who want to for example add keyboard shortcuts to their webapp.

Visit [the webpage](https://wesselvanree.github.io/js-keydown-event/) to use this tool.

## How to Create Keyboard Shortcuts

First, you need to add a `keyup` event listener to an element or, as in this example, the document.

```js
document.onkeydown = function(event) {
  // Code ...
}
```

After that, use the available properties of the keyup event. Take a look at the console in the tool for all event properties, or visit the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent).

```js
document.onkeydown = function(event) {
  const ctrl = event.ctrlKey // boolean
  const alt = event.altKey // boolean
  const shift = event.shiftKey // boolean
  const metaKey = event.metaKey // boolean

  // Specific code for a key
  const which = event.which // number

  // alt + shift + N
  if (alt && shift && which == 78) {
    yourCommand();
  }
  
  // This does the same
  if (alt && shift && event.code == "KeyN") {
    yourCommand();
  }
}

function yourCommand() {
  // Code ...
}
```

You can find the corresponding `event.which` number with the key you want in the tool.
