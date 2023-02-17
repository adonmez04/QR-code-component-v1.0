# Frontend Mentor - QR code component

- [Frontend Mentor - QR code component](#frontend-mentor---qr-code-component)
  - [Welcome! 👋](#welcome-)
  - [Links](#links)
  - [My Questions](#my-questions)
  - [Feedbacks](#feedbacks)
  - [Good Implementations](#good-implementations)
  - [Useful Resources](#useful-resources)
  - [Acknowledgments](#acknowledgments)
  - [Author](#author)

## Welcome! 👋

Welcome to my solution page. I hope you'll find some good implemantions for this project here.

![QR code component](./design/desktop-preview.jpg)

## Links

- [The Live Site](https://adonmez04.github.io/QR-code-component-v1.0/)

- [My Solution Page](https://www.frontendmentor.io/solutions/1qrcodecomponent-v11-DCyBcnh7oW)

- [The Challenge Page](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H)

## My Questions

> I've changed my very first project according to some good advice. This time, I can't understand why my text area is higher than the design file's text area. I checked my elements positions and they are in the same positions as the figma files. What should I do? Thanks.
>
> Also, are the nested structure of the semantic containing elements and BEM notation correct?
>
> Thanks again.

## Feedbacks

This is my very first project and I used some standard properties that I already know. And the community gave me some perfect advice to improve my coding skills.

The first time, I created a project where I can get some feedback and I didn't know what I should expect. I got some good feedback and it motivated me. I should focus on these fundamental recommendations to improve my code step by step.

These are some good feedback about my project:

**1. From Melvin Aguilar:**

- Figure elements `<figure>` should only be used when captions are required with `<figcaption>`, you can directly use the image tag in this solution.

- The `alt` attribute should explain the purpose of the image. Uppon scanning the QR code, the user will be redirected to the frontendmentor.io website, so a better `alt` attribute would be QR code to frontendmentor.io

- The images have a default bottom space of around 3px, you can remove it using `display: block` on the image, which might be why it's not exactly the same as the Figma. Even so, it's a very similar solution to the designs.

- The issue with the BEM naming convention in your code is that the block name (or the top-level element) is missing and the class names `qr-code__img-area` and `qr-code__text-area` do not have a block name to indicate which component or feature they belong to.

- In this case, the class name should be like this:
  `qr-code`
  `qr-code__img-area`
  `qr-code__text-area`

**2. From Hassia Issah:**

- Give the img a `max-width` of `100%` instead of a `width` and `height` value.

- This challenge does not require a box-shadow. To center the main on the page, add those:

```css
/* to center the main on the page using flexbox: */
() body {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

```css
/* to center the main on the page using grid: */
body {
  min-height: 100vh;
  display: grid;
  place-items: center;
}
```

**3. From Grace Snow:**

- You should never use any of the code generated by Figma or any other design programme.
  They can’t write code the way it needs to be written.

- Instead, inspect the properties of elements and use their values as a guide.
  Note you will need to

      - change units - e.g. Font size must never be in px and should use rem; Overall you won’t want to use px much as you progress

      - avoid setting widths or heights. Instead opt for a max-width on your component and let the browser calculate the height needed

- Remember, designs are static. But we build fluid solutions that must adapt to the screen, device and settings from those accessing them (edited)

**4. From Rostyslav Nazarenko:**

- please read more about semantic HTML and how to use `article` and `section`. I, myself, still don't understand how to use them correctly. Here is a great [article](https://www.smashingmagazine.com/2022/07/article-section-elements-accessibility/#what-the-html-spec-say). That is why HTML validation report have 2 unresolved issues

- don't set html `{ font-size: 16px; }` because it destroys your later use of relative units. By default in most browsers font size is 16px and setting it to absolute units prevents people from setting their own font size.

- Mostly the same issues read my comment on your previous challenge. I noticed only one thing. Don't set width and height to card element. Right now it is completely fine because you have a fixed font size and a card with a fixed size. But later on, when you will work on bigger challenges or projects it might create problems, like overflows, text on top of another text. As a quick fix, use `rem` units for `width` and don't use `height` at all.

## Good Implementations

```css
/* To center the main on the page, add those: */

/* to center the main on the page using flexbox: */
body {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* to center the main on the page using grid: */
body {
  min-height: 100vh;
  display: grid;
  place-items: center;
}
```

```css
.qr-code__img-area img {
  /* Give the img a `max-width` of `100%` instead of a `width` and `height` value.*/
  max-width: 100%;

  /* The images have a default bottom space of around 3px, you can remove it using `display: block` on the image, which might be why it's not exactly the same as the Figma. Even so, it's a very similar solution to the designs. */
  display: block;
}
```

```html
<!--the class name should be like this for BEM notation: -->
<div class="qr-code">
  <div class="qr-code__img-area"></div>
  <div class="qr-code__text-area"></div>
</div>
```

## Useful Resources

- [Semantic HTML: What It Is and How to Use It Correctly](https://www.semrush.com/blog/semantic-html5-guide/)

  - This helped me to understand the position of the semantic elements.
  - There is a clear table of semantic elements here.

- [How can I use alt attribute effectively?](https://webaim.org/techniques/alttext/)

- [hould I use pixels or ems/rems?!](https://www.joshwcomeau.com/css/surprising-truth-about-pixels-and-accessibility/)

- [`<article>` vs. `<section>`: How To Choose The Right One](https://www.smashingmagazine.com/2022/07/article-section-elements-accessibility/#what-the-html-spec-say)

- [Div divisiveness](https://www.scottohara.me/blog/2022/01/20/divisive.html)

- [Building websites for Safari Reader Mode and other reading apps](https://medium.com/@mandy.michael/building-websites-for-safari-reader-mode-and-other-reading-apps-1562913c86c9)

## Acknowledgments

- Thanks Grace Snow for your helpful comment. [@grace-snow](https://www.frontendmentor.io/profile/grace-snow)
- Thanks Hassia Issah for your helpful comment. [@Hassiai](https://www.frontendmentor.io/profile/Hassiai)
- Thanks Melvin Aguilar for your helpful comment. [@MelvinAguilar](https://www.frontendmentor.io/profile/MelvinAguilar)
- Thanks Rostyslav Nazarenko for your helpful comment. [@rostyslav-nazarenko](https://www.frontendmentor.io/profile/rostyslav-nazarenko)

## Author

- My Frontend Mentor Profile Page - [@adonmez04](https://www.frontendmentor.io/profile/adonmez04)
- For those of you reading this, have a nice day!
