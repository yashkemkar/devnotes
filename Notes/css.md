# CSS Notes

Steps to becoming a CSS God:
1. Time & Practice - just continuous practice over an extended period of time.
2. Think of every website you ever make as tetris - just nested rows and columns. 
3. Responsive Web Design (IMPORTANT) - adjust the design and dimensions of your website with varying screen sizes. Always design for mobile first.
4. Memorise your break points (widths/dimensions) at which styling changes to mantain responsivity. Use (640px, 768px, 1024px).
5. Use jankcss.com to play around with different styles and see how it looks (quick feedback on design).
6. Try to replicate beautiful websites (or atleast one key element of it). This way you can develop a library of many different types of web pages, effects, designs to be used in the future. Try to find beautiful websites with cool effects and just try to make it yourself.

## HOW IT WORKS

CSS stands for cascaded style sheets. The code in CSS assigns styling to particular classes or elements within an HTML doc. You can change almost anything visually through CSS.


## Pre-programmed effects
Here is a big compilation of precoded effects that you have seen elsewhere and thought might be useful for the future. You just have to put them in your code and assign a class to the relevant item. There will be a title, description, image and CSS code for each one.

### Background Grid Effect
This effect creates a bit of a grid background that can provide a cool effect for a landing page. You can change the colours around if you feel like creating something unique, but this thickness is very faint which makes it non-obtrusive.

```
.bgGrid {
    background-size: 40px 40px;
    background-image: linear-gradient(to right, #eef2ff 1px, transparent 1px), linear-gradient(to bottom, #eef2ff 1px, transparent 1px);
 } 
 ```

![Grid Background Effect](<Grid Background Effect.png>)

### Blue Shadow Effect (Static)
This effect creates a sort of shadow behind an element such as a box or a button that can provide a sort of 3-D popping out of the screen effect which is pretty cool. Obviously the colour of the shadow can be changed if need be, however the effect itself is quite nice. Especially for buttons.

```
.blueShadow {
    box-shadow: 0px 14px 55px rgba(106, 96, 255, 0.35);
}
```

![Blue Shadow Effect](<Blue Shadow Effect.png>)

### Light Shadow Effect (Hover)
This effect creates an animation that brings a shadow above the button or box, but it doesnt do this instantaneously. This does a transition through the x axis from left to right like the shadow travelling across it. You could do the same for y-axis as well. Again very nice for buttons.

```
        .lightShadow {
            position: relative;
            overflow: hidden;
        }

        .lightShadow p {
            position: relative;
            z-index: 2;
        }

        .lightShadow::after {
            position: absolute;
            content: '';
            background: navy;
            opacity: 0.04;
            width: 100%;
            height: 100%;
            top: 0;
            right: 100%;
            transition-duration: 200ms;
            z-index: 0;
        }

        .lightShadow:hover::after {
            transform: translateX(100%);
        }
```

![Light Shadow Effect](<Light Shadow Effect.gif>)