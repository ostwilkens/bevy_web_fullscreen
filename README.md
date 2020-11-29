# bevy_web_fullscreen
plugin for automatic resizing of primary bevy window to fit browser viewport

tested with [mrks-its/bevy_webgl2](https://github.com/mrk-its/bevy_webgl2) in [ostwilkens/arugio](https://github.com/ostwilkens/arugio)

currently requires specific git version of bevy:
```toml
[dependencies.bevy]
git = "https://github.com/bevyengine/bevy"
rev = "01ba7c44255059f833c2b90d3d6b7ac7e9c025ca"
default-features = false
```

### usage
`.add_plugin(FullViewportPlugin)`

### recommended html/css
```html
<meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0"/>
```

```css
body {
    margin: 0px;
    display: flex;
}
canvas {
    touch-action: none;
}
```