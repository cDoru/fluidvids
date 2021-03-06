# FluidVids.js [![Build Status](https://travis-ci.org/toddmotto/fluidvids.png)](https://travis-ci.org/toddmotto/fluidvids)

FluidVids is a raw JavaScript solution for responsive and fluid YouTube and Vimeo video embeds. It's extremely lightweight, and comes with a minified version for production environments. FluidVids supports IE8+, need [IE7 Support?](#ie7).

## Demo
Check out a [demo of FluidVids](http://toddmotto.com/labs/fluidvids).

## Options
Add the script just before the closing `</body>` tag, and initialise the module:

```html
<body>
  <!-- html content above -->
  <script src="dist/fluidvids.js"></script>
  <script>
  Fluidvids.init({
    selector: 'iframe',
    players: ['www.youtube.com', 'player.vimeo.com']
  });
  </script>
</body>
```

#### selector
Type: `String` Default: `iframe`

Give your fluidvids a custom selector if needed, this selector will be passed into a `querySelectorAll()`.

#### players
Type: `Array` Default: `['www.youtube.com', 'player.vimeo.com']`

To add more players, specify the domains that you need FluidVids to check against, be sure to include the subdomain for any videos that have a `src` with a subdomain.

## Installing with Bower
To install FluidVids into your project using Bower, use the GitHub repository hook:

```
bower install https://github.com/toddmotto/fluidvids.git
```

## IE7
For IE7 support, you lose a custom selector and need to default to getting elements by tag name. Change this:

```
var nodes = document.querySelectorAll(selector);
```

To this:

```
var nodes = document.getElementsByTagName(selector);
```

## Scaffolding
Project files and folder structure.

```
├── dist/
│   ├── fluidvids.js
│   └── fluidvids.min.js
├── src/
│   └── fluidvids.js
├── .editorconfig
├── .gitignore
├── .jshintrc
├── .travis.yml
├── Gruntfile.js
├── config.json
└── package.json
```

## License
MIT license
