# argparse-array-formatter

A custom formatter that allows you to use multiple paragraphs in your JS
[argparse](https://github.com/nodeca/argparse) descriptions.

This depends on implementation details of argparse, so it could break in future
versions. At the moment, it works with 1.0.2.

## Example

```js
var ArgumentParser = require('argparse').ArgumentParser;
var ArrFormatter = require('argparse-array-formatter');

var parser = new ArgumentParser({
  'version': '1.0.0',
  'addHelp': true,
  'customFormatter': ArrFormatter,
  'description': ['Paragraph 1. Make it as long as you like.', 'Paragraph 2.']
});
```

As with normal description strings, the width is limited to 80 characters
for readability.

## Copyright

© 2015, MIT License