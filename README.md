# vitepress-plugin-maps

This is a simple [VitePress](https://vitepress.dev/) plugin that provides a global component wrapping [Maps](https://kalisio.github.io/maps/), _a powerful real-time Geovisualizer_.

## Installation

You can install it with

```bash
yarn add -D https://github.com/kalisio/vitepress-plugin-maps
```

And then you just need to register the plugin in your `.vuepress/theme/index.js` or `.vitepress/theme/index.ts` file:

```js
import initializeMaps from '@kalisio/vitepress-plugin-maps'
import './style.css'

export default {
  extends: DefaultTheme,
  enhanceApp({ app }) {
    initializeMaps(app)
  }
}
```

## Usage

The recommended usage is to place your **Maps** declaration as an HTML element:

```md
<maps source="your Kalisio Maps URL" token="your Kalisio Maps token" />
```

The tag handles the following attributes:

| Attribute | Description |
| --- | --- |
| `source` | the url to the Kano website. The default value is `https://kano.dev.kalisio.xyz` |
| `token` | the token to be used if you want to be authenticated automatically. There is no default token and if you do not provide any token you have to authenticate yourself. |
| `css-style` | The style to apply to the **iframe**. The default value is `width: 100%; height: 50vh` |

## License

Copyright (c) 2017-20xx Kalisio

Licensed under the [MIT license](LICENSE).

## Authors

This project is sponsored by 

[![Kalisio](https://s3.eu-central-1.amazonaws.com/kalisioscope/kalisio/kalisio-logo-black-256x84.png)](https://kalisio.com)