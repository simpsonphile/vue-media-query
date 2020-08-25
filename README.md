# vue-media-query
Vue reactive, configurable, easy to use and SSR friendly media query plugin

## Configuration

### Configuration object
| Property name  | Value Type | Default | Description |
| ------------- | ------------- | ------------- | ------------- |
| breakpoints  | Array | ([breakpoints configuration and default](#breakpoints-object)) | Breakpoint rules |
| ssrWidth  | Integer | 1920 | When in SSR mode what width to pretend |
| debounce  | Integer | 300 | Latency used for debounce. When value <= 0 then disabled |
| throttle  | Integer | 0 | Latency used for throttle. When value <= 0 then disabled |

### Breakpoints object
```javascript
{
  breakpoints: {
    m: {
      width: 670,
      type: 'max'
    }
  }
}
```

## Instalation

### NUXT.js
1. Create js file in plugins folder with choosed name

2. Use your [configuration object](#configuration-object)
```javascript
//  plugins/[choosed-name].js
import vueMediaQuery from 'vue-media-query'
import Vue from 'vue'

Vue.use(media, [options-object])
})
```

3. Import as plugin in nuxt.config.js
```javascript
//  nuxt.config.js
plugins {
  '~plugins/[choosed-name].js'
}
```

## Usage
You can use plugin in script
```javascript
this.$media.isClient && this.$media.m && !this.$media.ms
```
or in template
```javascript
{{ $media.isClient && $media.m && !$media.ms }}
```

### Examples
to get width, height, screen type You can simply:
```javascript
{{ $media.width }}
{{ $media.height }}
{{ $media.scrType }}
```
To use specified breakpoint rules:
```javascript
{{ $media.[rule-name] }}
```
rule-name is specified breakpoint name

To render something only in client mode you can:
```javascript
{{ $media.isClient && $media.[rule-name] }}
// it will evaluate to true only if it is client mode and in specified rule 
```

## Requirments
* Vue 2.6.0+
* IE8+
