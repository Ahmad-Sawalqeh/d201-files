# Transform

The transform CSS property lets you rotate, scale, skew, or translate an element.

> Syntax:

```
/* Keyword values */
transform: none; /* Specifies that no transform should be applied */

/* Function values */
transform: rotate(10deg);
transform: translate(12px, 50%);
transform: scale(2, 0.5);
transform: skew(30deg, 20deg);

/* Multiple function values */
transform: translateX(10px) rotate(10deg) translateY(5px);

/* Global values */
transform: inherit;
transform: initial;
transform: unset;
```

> Transform Origin:

The `transform-origin` property can accept one or two values. When only one value is specified, that value is used for both the horizontal and vertical axes. If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.<br>

+ Syntax:
```
transform-origin: right top;
transform-origin: top right;
transform-origin: 26% 30%;
transform-origin: 43px 60px;
```

> Perspective:

The `perspective` CSS property determines the distance between the z=0 plane and the user in order to give a 3D-positioned element some perspective.<br>

+ Syntax:
```
/* Keyword value */
perspective: none;

/* <length> values */
perspective: 200px;
```

> perspective-origin:

The perspective-origin CSS property determines the position at which the viewer is looking.<br>

+ Syntax:

```
/* One-value syntax */
perspective-origin: x-position;

/* Two-value syntax */
perspective-origin: x-position y-position;
```

> Transform Style:

The `transform-style` CSS property sets whether children of an element are positioned in the 3D space or are flattened in the plane of the element.<br>

+ Syntax:
```
/* Keyword values */
transform-style: flat;
transform-style: preserve-3d;
```

> backface-visibility:

The `backface-visibility` CSS property sets whether the back face of an element is visible when turned towards the user.<br>

+ Syntax:
```
/* Keyword values */
backface-visibility: visible;
backface-visibility: hidden;
```

# CSS Transitions

The `transition` CSS property is a shorthand property for `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`.<br>

Transitions enable you to define the transition between two states of an element. Different states may be defined using pseudo-classes like `:hover` or `:active` or dynamically set using JavaScript.<br>

+ Syntax:
```
/* Apply to 1 property */
/* property name | duration */
transition: margin-right 4s;

/* property name | duration | delay */
transition: margin-right 4s 1s;

/* property name | duration | timing function */
transition: margin-right 4s ease-in-out;

/* property name | duration | timing function | delay */
transition: margin-right 4s ease-in-out 1s;

/* Apply to 2 properties */
transition: margin-right 4s, color 1s;

/* Apply to all changed properties */
transition: all 0.5s ease-out;
```

# Animations

Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states.<br>

+ Animations Keyframes:
To set multiple points at which an element should undergo a transition, use the `@keyframes` rule. The `@keyframes` rule includes the animation name, any animation breakpoints, and the properties intended to be animated.<br>

- Syntax:
```
@keyframes slidein {
  from {
    transform: translateX(0%);
  }

  to {
    transform: translateX(100%);
  }
}
```

1. Animation Name:
`animation-name` property is used with the animation name, identified from the `@keyframes` rule, as the property value.<br>

+ Syntax:
```
/* Single animation */
animation-name: none;
animation-name: ani_name;
```

2. Animation Duration:
The `animation-duration` CSS property sets the length of time that an animation takes to complete one cycle.<br>

+ Syntax:
```
/* Single animation */
animation-duration: 6s;
animation-duration: 120ms;

/* Multiple animations */
animation-duration: 1.64s, 15.22s;
animation-duration: 10s, 35s, 230ms;
```

3. animation-timing-function:
The `animation-timing-function` CSS property sets how an animation progresses through the duration of each cycle.

* Syntax:
```
/* Keyword values */
animation-timing-function: ease;
animation-timing-function: ease-in;
animation-timing-function: ease-out;
animation-timing-function: ease-in-out;
animation-timing-function: linear;
animation-timing-function: step-start;
animation-timing-function: step-end;
```

4. Animation Iteration:
The `animation-iteration-count` CSS property sets the number of times an animation cycle should be played before stopping.<br>

+ Syntax:
```
/* Keyword value */
animation-iteration-count: infinite;

/* <number> values */
animation-iteration-count: 3;
animation-iteration-count: 2.4;
```

5. Animation Direction:
The `animation-direction` CSS property sets whether an animation should play forwards, backwards, or alternating back and forth.<br>

+ Syntax:
```
/* Single animation */
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;
```

6. Animation Play State:
The `animation-play-state` CSS property sets whether an animation is running or paused.<br>

+ Syntax:
```
/* Single animation */
animation-play-state: running;
animation-play-state: paused;
```

7. Animation Fill Mode:
The `animation-fill-mode` CSS property sets how a CSS animation applies styles to its target before and after its execution.<br>

+ Syntax:
```
/* Single animation */
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;
```

8. Animation delay:
The `animation-delay` CSS property sets when an animation starts. The animation can start later, immediately from its beginning, or immediately and partway through the animation.<br>

+ Syntax:
```
/* Single animation */
animation-delay: 3s;
animation-delay: 0s;
animation-delay: -1500ms;
```





