---
template: blog-post
title: CSS Tricks of the Trade
slug: /css-tricks-of-the-trade
date: 2022-02-27 14:09
description: CSS Properties and Functions
---

# :Is and :Where Properties
<p>The :is and :where selectors allows you to apply styles to the elements you want in a puesdo-class property. Similar to Sass preprocessor nesting, when using the :is or :where selector you can target multiple child and elements with the same styling properties without a cumbersome selector. 
```css
 .header :is(p,.btn) {
  color:red;
} 
```

You can also declare: is or :where first and choose different elements to apply the styling to.
```css
:where(p,.btn){
  color:yellow;
}
:is(header,.title){
  color:blue;
}
```
 One thing to keep in mind is that these selectors themselves do not have a specificity. However, for the :is selector the specificity is set by the most specific element it is targeting in parenthesis. The pseudo class where allows you to do the same thing. The difference with using the :where selector is that it negates the specificity of the elements you are targeting. This means the styling in the :where class will always have the lowest specificity. Another benefit to using these selectors is if you misidentify one element it doesn’t impact the styling taking effect on the rest of the selectors.</p>


 In this example, the first declaration will be declared. This is because the header :is (p, .btn) has a specificity of (0,1,1) and the header p declaration has a (0,0,1) specificity All the selector in the parenthesis take on the specificity of the most specific element.
``` css
 .header :is(p,.btn) {
  color:red;
} 

.header p {
  color:green;
}
```

Look at this example although .btn is a class selector it has the same specificity of the element selectors. Hopefully, using these selectors will make your code less cumbersome and more legible.

``` css
:where(p,.btn){
  color:yellow;
}
```

# Fluid Typography


Fluid typography allows your typography to dynamically change according to the screen size. This can help reduce the amount of code needed to adjust code in media queries. 

It can also make the transition between media queries less jarring. The typography of the page will simple grow or shrink with the page. The function that allows you to do this is clamp (). The clamp function allows developers to set three parameters. 

The minimum sets the smallest the text can get on the screen. The growth rate sets how much the text will grow depending on the vary screen size before it reaches the maximum. The maximum is the largest the text can get on the screen. Take a look at this example:
        ```css
   --fs-xl: clamp (3.5rem,12vw +1rem,8rem)
```

For any text set to the CSS variable –fs-xl this will be its parameters. The font size will not get lower than 3.5rem and will not get higher than 8rem. When the screen is not at the max or min screen sizes the text will adjust according to the viewport specified. The vw unit is equal to 1% of the viewport-width. Notice in this example it also has a “+ 1rem”. This allows you as the developer to have more control over how the text will grow as the screen size increases.  Using rem units when using clamp will allow your site to adopt to user browser preferences. The custom properties you can use with this function is –fluid-type-min, --fluid-type-target, and –fluid-type-max.




<p> Logical properties make it easier for developers to code in different languages. The traditional physical properties left,right,top bottom work well when coding English. However, it gets complicated when writing languages that are written right to left or vertically. Logical properties fix this issue. Logical properties pay attention to the writing-mode property of the element. The writing mode properties are :

1. horizontal-tb,
2. vertical-lr
3. vertical-rl.

 <br> The inline controls the left and right of an object and the block controls the top and bottom of an element. Inline and block can be added to margin, padding and border properties. I will use margin for my example to show how logical properties work. </p>

1. Margin-inline targets the right and left.
2.  Margin-inline-start targets the left 
3. margin-inline-end targets the right.
4. Margin-block targets the bottom and the top 
5. Margin-block-start targets the top
6. Margin-block-end targets the bottom

The direction of the -start and -end properties change depending on if you are writing left to right or right to left . Logical properties can control size. Inline and block can control the size of an element. 
1:Inline-size targets the width.
2. Max-inline-size targets the max-width
3. Min-inline-size targets the min-width
4. Block-size targets the height
5. Max-block-size targets the max-height
6. Min-block-size targets the min-height

The logical properties can also be used with positioning an element on a page
