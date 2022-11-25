[![npm](https://img.shields.io/npm/v/@pautym/modern-eleventy-plugin-schema)](https://www.npmjs.com/package/@pautym/modern-eleventy-plugin-schema)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[Eleventy](https://www.11ty.dev/) plugin to generate JSON-LD [structured data](https://schema.org/).

- [Installation](#installation)
- [Introduction](#introduction)
- [Usage](#usage)
- [Related plugins](#related-plugins)
- [License](#license)

# Installation

Install the package:

```sh
npm install --save @pautym/modern-eleventy-plugin-schema
```

Add the plugin to your [Eleventy configuration](https://www.11ty.dev/docs/config/)
(usually `.eleventy.js`):

```js
const schema = require("@pautym/modern-eleventy-plugin-schema");

module.exports = function(eleventyConfig) {
  eleventyConfig.addPlugin(schema);
};
```

## Introduction

The plugin adds a shortcode to generate the JSON-LD script (including the `<script>` tag).

The shortcode supports the following schema types:

- [WebSite](https://schema.org/WebSite).
- [BlogPosting](https://schema.org/BlogPosting).
- [WebPage](https://schema.org/WebPage).

## Usage

Add data/front matter to your pages. Please refer to the files in [demo](./demo).
If you already have the value in other properties, you can use
[computed data](https://www.11ty.dev/docs/data-computed/) to clone them.

Call the shortcode where you want the script to be displayed:

```njk
{% jsonLdScript meta, type, tags %}
```

### Validation

You can validate the structured data using one of the following tools:

- [Google's Structured Data Testing Tool](https://search.google.com/structured-data/testing-tool/u/0/).
- [JSON-LD Playground](https://json-ld.org/playground/).
- [JSON Schema Validator](https://www.jsonschemavalidator.net/).

## License

MIT. See [LICENSE](./LICENSE).
