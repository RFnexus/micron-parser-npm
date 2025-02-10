Micron Parser JS - NPM Version
-
This NPM package provides a JavaScript parser for Micron, a lightweight, terminal-friendly markdown format used
in  [NomadNet](https://github.com/markqvist/NomadNet) and [MeshChat](https://github.com/liamcottle/reticulum-meshchat)

## Usage

```js
import MicronParser from 'micron-parser';
// Create a new parser (darkTheme = true/false)
const parser = new MicronParser(true);

// Input Micron markup
const micronMarkup = `
> Example Heading
-∿
This is a simple line in Micron.
# This line is a comment and won't appear in the output.
`;

// Convert Micron to an HTML string
const htmlOutput = parser.convertMicronToHtml(micronMarkup);

// Insert it into your page
document.getElementById('yourElement').innerHTML = htmlOutput;

// Or create a DocumentFragment from Micron
const domFragment = parser.convertMicronToFragment(micronMarkup);
// and append it to the DOM
document.body.appendChild(domFragment);
```

## Best practices

For optimal display of Micron content in the browser it's recommended to use a monospaced font such
as [Roboto Mono](https://fonts.google.com/specimen/Roboto+Mono), available through Google Fonts, or wrap content in a
`<pre>` tag

The line height for your container should also be set to `line-height: normal !important;` to better match the terminal
environment

