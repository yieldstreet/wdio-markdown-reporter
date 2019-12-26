# WebdriverIO Markdown Reporter

> A WebdriverIO plugin to report in Markdown style.

![Reporter](./img/reporter.png)

## Installation

You can simple do it by:

```bash
npm install wdio-markdown-reporter --save-dev
```

Instructions on how to install `WebdriverIO` can be found [here.](https://webdriver.io/docs/gettingstarted.html)

## Configuration

At the top of the wdio.conf.js-file, add:

```js
// wdio.conf.js
var markdownReporter = require("wdio-markdown-reporter");
```

In order to use the service you need to add reporter to your services array in wdio.conf.js

```js
// wdio.conf.js
export.config = {
  reporter: : [
    [markdownReporter, {
      outputDir: ' ',
    }],
  ],
};
```

## Configuration Options

The following configuration options are supported and are all optional.
By default none of the config options are set.

### outputDir

Define a directory where your markdown file should get stored.

Type: `String`<br>
Required

## Merge all \*.md files

To generate only one markdown file use the **concat-cli** CLI to concat the files

```bash
concat-cli -f ./markdown-reporter/*.md -o mergeResult.md

```
