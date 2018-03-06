# Android Simple Tooltip

A simple library based on [PopupWindow](http://developer.android.com/intl/pt-br/reference/android/widget/PopupWindow.html) to create Tooltips on Android.

## Features

 - Working from Android 2.1 (API 7) *Note: animation above 3.0 (API 11)*
 - Simple to use: few parameters in a single line of code
 - Animation with speed and size control
 - Option to close with touch inside or outside of the tooltip.
 - Modal mode (prevents touch in the background)
 - Overlay (darkens the background highlighting the anchor)
 - Customizable arrow
 - Inflatable content from a `View` or `XML` layout.
 - Colors and dimensions customized by `Builder` or `XML` resources

## Demo

![Demo](https://raw.githubusercontent.com/douglasjunior/android-simple-tooltip/master/screenshots/demo.gif)

## Usage
### Basic

```java
View yourView = findViewById(R.id.your_view);

new SimpleTooltip.Builder(this)
    .anchorView(yourView)
    .text("Texto do Tooltip")
    .gravity(Gravity.END)
    .setWidth(200)
    .setHeight(200)
    .animated(true)
    .transparentOverlay(false)
    .build()
    .show();
```

### Resources

```xml
<color name="simpletooltip_background">@color/colorAccent</color>
<color name="simpletooltip_text">@android:color/primary_text_light</color>
<color name="simpletooltip_arrow">@color/colorAccent</color>
```
```xml
<dimen name="simpletooltip_max_width">150dp</dimen>
<dimen name="simpletooltip_overlay_offset">10dp</dimen>
<dimen name="simpletooltip_margin">10dp</dimen>
<dimen name="simpletooltip_padding">8dp</dimen>
<dimen name="simpletooltip_arrow_width">30dp</dimen>
<dimen name="simpletooltip_arrow_height">15dp</dimen>
<dimen name="simpletooltip_animation_padding">4dp</dimen>
```
```xml
<integer name="simpletooltip_overlay_alpha">120</integer>
<integer name="simpletooltip_animation_duration">800</integer>
```
```xml
<style name="simpletooltip_default" parent="@android:style/TextAppearance.Medium"></style>
```


## Download
### Release

1. Add it in your root `build.gradle` at the end of repositories:

    ```javascript
    allprojects {
    	repositories {
    		...
    		maven { url "https://jitpack.io" }
    	}
    }
    ```

2. Add the dependency

    ```javascript
    dependencies {
        compile 'com.github.tabassumLatif:SimpleTooltip:1.0.0'
    }
    ```
