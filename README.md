# Scroll-Animator

Similar to the AOS library however less complicated and more simple! Adjustments will be made in the future. Refer to the readme.

## Installation:

❗ Place both within your head tag:

```html
<link
  rel="stylesheet"
  type="text/css"
  href="https://cdn.jsdelivr.net/gh/sup3r0001/Scroll-Animator@latest/Scroll%20Animator/scrollanimator.css"
/>
```

```html
<script src="https://cdn.jsdelivr.net/gh/sup3r0001/Scroll-Animator@latest/Scroll%20Animator/scrollanimator.js"></script>
```

# Usage

❗ After installing SA, to use it, just assign a class trigger to an element.

<br>

## 💖 On-scroll Animations

<details>
<summary><strong>View On Scroll Animation Syntax</strong></summary>
<br>

- **sa**:

Slides object in from the left

```html
<div class="sa"></div>
```

- **sa-right**:

Slides object in from the right

```html
<div class="sa-right"></div>
```

- **sa-zoom**:

Zooms in object

```html
<div class="sa-zoom"></div>
```

- **sa-flip**:

Flips object

```html
<div class="sa-flip"></div>
```

- **sa-shift**:

Slides object in from the left with a bounce

```html
<div class="sa-shift"></div>
```

<span style="color:orange">NOTE : This uses the animation property, you must replace <span style="color:orange">NOTE : This uses the animation property, you must replace **sa** with **animation** for durations and delays to work properly.</span>**sa** with **animation** for durations and delays to work properly.</span>


### Custom Animations

<details>
<summary><strong>View Custom Animation Syntax</strong></summary>
<br>

- Custom animations are a way for you to customize animations on scroll. They have no inherit animation attached.
- Custom animations only receive the .active class when scrolled past the breakpoint.


To Animate:

**1**. Use Transform:

```css
.my-custom-animation {
  transform: translateY(500px);
  opacity: 0;
  transition: 1s;
}

.my-custom-animation.active {
  transform: translateY(0);
  opacity: 1;
}
```

**2**. Use Keyframes:

```css

.my-custom-animation {
  opacity: 0;
}

.my-custom-animation.active {
    animation: myAnimation 0.4s ease-in-out 0s 1 forwards;
}

@keyframes myAnimation {
  0% {
    transform: translate(-6%, -6%);
        opacity: 0;
        
        
    }
    40% {
      transform: translate(3%, 3%);
        opacity: 1;
    }
    100% {
      transform: translate(0%, 0%);
        opacity: 1;
    }
}
```

</details>
</details>

<br>

## 🔄 On-load Animation Styles

<details>
<summary><strong>View On-load Syntax</strong></summary>
<br>

- **onload-shift**:

Slides object in from the left with a bounce

```html
<div class="onload-shift"></div>
```

<span style="color:orange">NOTE : This uses the animation property, you must replace **sa** with **animation** for durations and delays to work properly.</span>

- **onload-top**:

Slides object in from the top with a bounce

```html
<div class="onload-top"></div>
```

<span style="color:orange">NOTE : This uses the animation property, you must replace **sa** with **animation** for durations and delays to work properly.</span>

- **onload-bottom**:

Slides object in from the bottom with a bounce

```html
<div class="onload-bottom"></div>
```

<span style="color:orange">NOTE : This uses the animation property, you must replace **sa** with **animation** for durations and delays to work properly.</span>

</details>

<br>

## 🚦 Scroll Animation Threshold

Controls at what point an animation triggers

<details>
<summary><strong>View SAT Syntax</strong></summary>
<br>

**data-sa-threshold="{px height}"**

```html
<div class="sa" data-sa-threshold="400"></div>
```

_Default value is: 250._

</details>

<br>

## ⏭️ Durations

Controls how long an animation plays

<details>
<summary><strong>View Duration Syntax</strong></summary>
<br>
**sa-duration{time}**
``` html
<div class="sa sa-duration0_1"></div>
```

Time format: {second}\_{millisecond}

MIN: 0_1s

MAX: 15s

_The underscore is substituted for a dot._

</details>

<br>

## 🛑 Delays

Controls the amount of time before an animation plays

<details>
<summary><strong>View Delay Syntax</strong></summary>
<br>

**sa-delay{time}**

```html
<div class="sa sa-delay0_4></div>
```

Time format: {second}\_{millisecond}

MIN: 0_1s

MAX: 15s

_The underscore is substituted for a dot._

</details>

<br>

## 〽️ Easing

Easing Controls how the animation plays throughout it's duration

<details>
<summary><strong>View Easing Syntax</strong></summary>
<br>

- **sa-easeinout**

```html
<div class="sa sa-easeinout"></div>
```

- **sa-easein**

```html
<div class="sa sa-easein"></div>
```

- **sa-easeout**

```html
<div class="sa sa-easeout"></div>
```

- **sa-ease**

```html
<div class="sa sa-ease"></div>
```

- **sa-easeincubic**

```html
<div class="sa sa-easeincubic"></div>
```

- **sa-easeoutcubic**

```html
<div class="sa sa-easeoutcubic"></div>
```

- **sa-easestrong**

```html
<div class="sa sa-easestrong"></div>
```

</details>

<br>

## 🔗 Animation Groups

Animation Grouping is a way to group scroll animations
so that they can trigger at the same breakpoint with no issues!
It applies to the parent element of a animation group

<details>
<summary><strong>View Animation Grouping Syntax</strong></summary>
<br>

- **sa-group**

```html
<div class="sa-group">
  <h3 class="sa">Some Head Text!</h3>
  <p class="sa">Some paragrapg text.</p>
</div>
```

**AG Nesting**

✅ Nesting Animation Groups is supported.
❗ AG nesting requires another sa-group class on the very next parent to work.

_See Usage below_!

```html
<div class="sa-group">
  <h2 class="sa">Side Head Text!/h2>
    <div class="sa-group">
      <h3 class="sa">Some Head Text!</h3>
    <p class="sa ">Some paragrapg text.</p>
  </div>
</div>
```

</details>

<br>
