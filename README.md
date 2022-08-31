# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)


## Overview
This solution is a mock, or copy, of the desktop & mobile design files using HTML & CSS.

### Links

- Solution URL: https://github.com/KylesTech95/qr-code-component/blob/main/index.html
- Live Site URL: https://kylestech95.github.io/qr-code-component/

## My process
1. Planning:
a. Gathered resources (color-palette, font-sizes, font-families, content, etc...).
b. Studied the enemy (Design) in order to better understand which tags & landmarks would be used as well as to know which CSS styles to set in place.

2. Included Html & CSS in one HTML file.

3. Added a [:root] CSS tag where all of the colors and font-families were programmed to represent different names. [:root] is advantageous because it selects HTML elements with higher priority. In addition, this process is more organized versus changing a color manually within each class selector.

4. All of the content was wrapped within a [div] element with the class of "container wrapper".

5. Navigated to the styles and utilized flexbox for the mentioned [div] class above. Ensure that column is used in order to read the content from top to bottom. I noticed that the spaces between each [div] seemed to be similar in length, leading me to use the [gap] property. 
```css
div.container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
```
In addition, this reduces the number of lines used if one was to change the margins & paddings of each element.

6. I manipulated the [img] html size to match the size of the width of the container by setting it's width to 100%. Please view the example below:
```html
<img src="images/image-qr-code.png" width="100%" alt="qr code" id="img" class="qrCode">
```
7. Once the size looked just right, i felt confident enough to continue styling the remaining elements. 

8. Media query was established to give the design some mobile compatability. 
Modifications made within the query were the position coordinates, the width size, and the h3 font-size.
```css
@media (max-width: 375px) {
    body {
    width: 375px;
  }
  div.container {
    width: 265px;
    position: relative;
    top: 100px;
  }
  h3 {
    font-size: 20px;
  }
  .attribution {
    position: relative;
    top: 120px;
  }
}
```

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://fonts.google.com/) (https://fontawesome.com/)- For styles

### What I learned

With this specific project, I was happy to acknowledge how off the width and height was in my original mobile design. Oh my goodness, haha. The content was all the way at the bottom. 
So with this, I learned how to palce the content where it needed to be in order to be viewed correctly by viewers:

```css
 @media (max-width: 375px) {
    body {
    width: 375px;
  }
  div.container {
    width: 265px;
    position: relative;
    top: 100px;
  }
 }
```
A key takeaway here are the minor details. Notice the difference between the original & Media Query [body] & [div.container] css selectors. The only properties modified are the [width] 7 [top] properties. Keep It Simple (K.I.S.).
