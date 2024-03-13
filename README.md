# Scroll-Animator
Similar to the AOS library however less complicated and more simple! Adjustments will be made in the future. Refer to the readme.

## Installation:
❗ Place both within your head tag:

``` html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/sup3r0001/Scroll-Animator@latest/Scroll%20Animator/scrollanimator.css">
```

``` html
<script src="https://cdn.jsdelivr.net/gh/sup3r0001/Scroll-Animator@latest/Scroll%20Animator/scrollanimator.js"></script>
```

## Usage:
❗ After installing SA, to use it, just assign a class name to an element!


### Animation Styles:
- **sa**:

Slides object in from the left
``` html
<div class="sa"></div>
```

- **sa-right**:

Slides object in from the right
``` html
<div class="sa-right"></div>
```

- **sa-zoom**:

Zooms in object
``` html
<div class="sa-zoom"></div>
```

- **sa-flip**:

Flips object
``` html
<div class="sa-flip"></div>
```

- **sa-shift**:

Slides object in from the left with a bounce
``` html
<div class="sa-flip"></div>
```


### Scroll Animation Threshold

**data-sa-threshold="{px height}"**
``` html
<div class="sa" data-sa-threshold="400"></div>
```

_Default value is: 250._



### Duration:

**sa-duration{time}**
``` html
<div class="sa sa-duration0_1"></div>
```

Time format: {second}_{millisecond}

MIN: 0_1s

MAX: 15s

*The underscore is substituted for a dot.* 



### Delay:

**sa-delay{time}**
``` html
<div class="sa sa-delay0_4></div>
```

Time format: {second}_{millisecond}

MIN: 0_1s

MAX: 15s

*The underscore is substituted for a dot.* 



### Easing:


- **sa-easeinout**

``` html
<div class="sa sa-easeinout"></div>
```

- **sa-easein**

``` html
<div class="sa sa-easein"></div>
```

- **sa-easeout**

``` html
<div class="sa sa-easeout"></div>
```

- **sa-ease**

``` html
<div class="sa sa-ease"></div>
```

- **sa-easeincubic**

``` html
<div class="sa sa-easeincubic"></div>
```

- **sa-easeoutcubic**

``` html
<div class="sa sa-easeoutcubic"></div>
```



### Animation Grouping

Animation Grouping is a way to group scroll animations 
so that they can trigger at the same breakpoint with no issues! 
It applies to the parent element of a animation group

- **sa-group** 

``` html
<div class="sa-group">
  <h3 class="sa">Some Head Text!</h3>
  <p class="sa">Some paragrapg text.</p>
</div>
```


**AG Nesting**

_✅ Nesting Animation Groups is supported.
❗ AG nesting requires another sa-group class on the very next parent to work. 

See Usage below_!

``` html
<div class="sa-group">
  <h2 class="sa">Side Head Text!/h2>
  <div class="sa-group">
    <h3 class="sa">Some Head Text!</h3>
    <p class="sa ">Some paragrapg text.</p>
  </div>
</div>
```



## ON-LOAD Shift

- **onload-shift**:

Slides object in from the left with a bounce
``` html
<div class="onload_shift"></div>
```

- **onload-shift-delay{time}**:

Slides object in from the left with a bounce and a delay.
``` html
<div class="onload-shift-delay5_5"></div>
```

Time format: {second}_{millisecond}

MIN: 0_1s
