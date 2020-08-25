# vue-media-query
Vue reactive, configurable and SSR friendly media query plugin

## 

## Configuration
| Property name  | Value Type | Default | Description |
| ------------- | ------------- | ------------- | ------------- |
| breakpoints  | Array | (link for default breakpoints) | Breakpoint rules |
| ssrWidth  | Integer | 1920 | When in SSR mode what width to pretend |
| debounce  | Integer | 300 | Latency used for debounce. When value <= 0 then disabled |
| throttle  | Integer | 0 | Latency used for throttle. When value <= 0 then disabled |

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
