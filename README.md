# JScroll

Smooth scrolling sections based on <a href="http://www.everyday3d.com/blog/index.php/2014/08/18/smooth-scrolling-with-virtualscroll/">VirtualScroll</a>.

## Usage

###### Install
`yarn add @twotwentytwo/jscroll`

###### Javascript
```Javascript
import JScroll from '@twotwentytwo/jscroll'

JScroll.init({ // Options are optional })
```
###### Markup
```HTML
<div data-smooth> <!-- Add data-smooth to ur containeer -->
  <div data-smooth-item></div>
  <div data-smooth-item></div>
  <div data-smooth-item data-speed="1.1"></div> <!-- Use data-speed to control speed of item -->
  <div>
    <div>
      <div data-smooth-item></div> <!-- No need to be top lvl -->
    </div>
  </div>
</div>
```

## Options
`ease`: Easing value (defaults to `0.1`)

`scrollbar`: Virtual scrollbar (defaults to `false`)

`disableMobile`: Disable JScroll on mobilee devices (defaults to `true`)

`preload`: Trigger resize after loading all images (defaults to `false`)

`vs`:
  - `mouseMultiplier`: Defaults to 0.45
  - `touchMultiplier`: Defaults to 2.5
  - `firefoxMultiplier`: Defaults to 90
  
## Methods
`init()`: Initialise instance

`update()`: Update instance

`resize()`: Trigger resize

`preload()`: Preload images

`stop()`: Stop scrolling

`resume()`: Resume scrolling

`destroy()`: Clean instance

`scrollTo(someElement.offsetTop)`: Anchor scroll

## Events

`on('tick', ({ target, current })`: Raf callback. Scroll and lerped scroll params.

`on('scroll', ({ delta, target })`: Scroll callback. Delta and scroll params.

## Getters
`getSmooth`: Returns lerped scroll value

`getScroll`: Returns scroll value

