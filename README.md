# ⚠️ this plugin is deprecated, as bevy now has this built-in. see [link](https://github.com/ostwilkens/bevy_web_fullscreen/pull/9#issuecomment-1472676869)

# bevy_web_fullscreen
plugin for automatic resizing of primary bevy window to fit browser viewport

tested with [mrks-its/bevy_webgl2](https://github.com/mrk-its/bevy_webgl2) in [ostwilkens/arugio](https://github.com/ostwilkens/arugio)

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
    overflow: hidden;
}
canvas {
    touch-action: none;
}
```

### Conditional compilation
Make use of this cfg in order to have your code only include the plugin when targeting wasm.

```rust
#[cfg(target_family = "wasm")]
app.add_plugin(FullViewportPlugin);
```
