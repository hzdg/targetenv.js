targetenv.js
============

This module is for doing things conditionally based on the environment you're
targeting. It uses the build tool itself ([browserify], [webpack]) instead of
relying on examining the environment (for example, `module.exports`, etc).


## Usage

```javascript
var targetEnv = require('targetenv');
if (targetEnv.isBrowser) {
  // Do something.
}
```


## Properties

<table>
  <tr>
    <td><code>target</code></td>
    <td>
      Either <code>"main"</code>, <code>"browser"</code>, <code>"web"</code>,
      or <code>"webpack"</code>, depending on which file was used as the main
      module.
    </td>
  </tr>
  <tr>
    <td><code>isBrowser</code></td>
    <td>A boolean that indicates whether this code built for the browser.</td>
  </tr>
</table>


## How

The module's package.json tells your build tool ([browserify], [webpack]) to use
a different entry point (which can be examined).


[browserify]: http://browserify.org
[webpack]: http://webpack.github.io
