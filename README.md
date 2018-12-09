# netlify-cms-widget-inline-select

[Check out the demo!](https://netlify-cms-widget-inline-select.netlify.com/demo)

Inline radio + multi-checkboxes select widget.

[![npm version][version-badge]][version]
[![Build Status][build-badge]][build]
[![module formats: cjs][module-formats-badge]][unpkg-bundle]
[![License: MIT][license-badge]][license]

[![semantic-release][semantic-release-badge]][semantic-release]
[![code style: prettier][code-style-badge]][code-style]

![preview](docs/preview.png)

This widget was inspired by original [netlify-cms-widget-select][netlify-cms-widget-select].

## Install

As an npm package:

```shell
npm install --save netlify-cms-widget-inline-select
```

```js
import { InlineSelectControl, InlineSelectPreview } from 'netlify-cms-widget-inline-select';

CMS.registerWidget('inline-select', InlineSelectControl, InlineSelectPreview);
```

## How to use

Add to your Netlify CMS configuration:

```yaml
fields:
  - name: radio_select
    label: Radio select
    widget: inline-select
    options: ['left', 'center', 'right']
```

## Configuration

You can customize the preview of the url with these options:

- `options` - you can also specify the `value` and `label` in `options` option

```yaml
fields:
  - name: radio_select
    label: Most recent framework
    widget: inline-select
    options:
      - { value: react, label: React }
      - { value: angular, label: Angular 1.x }
      - { value: vue, label: Vue.js }
      - { value: $, label: jQuery }
```

- `multiple` - add ability to select multiple items

```yaml
fields:
  - name: checkboxes_select
    label: Favorite frameworks
    widget: inline-select
    multiple: true
    options: ['React', 'Angular', 'Vue', 'Other']
```

## License

MIT

## Support

For help with this widget, open an [issue](https://github.com/buz-zard/netlify-cms-widget-inline-select)
or ask the Netlify CMS community in [Gitter](https://gitter.im/netlify/netlifycms).

[version-badge]: https://badge.fury.io/js/netlify-cms-widget-inline-select.svg
[version]: https://www.npmjs.com/package/netlify-cms-widget-inline-select
[build-badge]: https://travis-ci.org/buz-zard/netlify-cms-widget-inline-select.svg?branch=master
[build]: https://travis-ci.org/buz-zard/netlify-cms-widget-inline-select
[license-badge]: https://img.shields.io/badge/License-MIT-yellow.svg
[license]: https://opensource.org/licenses/MIT
[semantic-release-badge]: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
[semantic-release]: https://github.com/semantic-release/semantic-release
[code-style-badge]: https://img.shields.io/badge/code_style-prettier-ff69b4.svg
[code-style]: https://github.com/prettier/prettier
[module-formats-badge]: https://img.shields.io/badge/module%20formats-cjs-green.svg
[unpkg-bundle]: https://unpkg.com/netlify-cms-widget-inline-select/lib/
[netlify-cms-widget-select]: https://www.npmjs.com/package/netlify-cms-widget-select
