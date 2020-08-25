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

## Usage
```javascript
this.$media.isClient && this.$media.m && !this.$media.ms
```

## Requirments
Vue 2.6.0+
