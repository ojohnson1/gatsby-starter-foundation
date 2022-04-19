---
template: blog-post
title: Math is Modern....CSS
slug: /math-is-modern
date: 2022-04-18 20:18
description: modern css
---

## The Calc Function

Calc function allows you to do addition, subtraction, multiplication and division on length units. You can use different units within calc functions. You have to have a space on both sides of your calc function for it to work. Calc can be combined with CSS variables. You can define a variable and modify it with the function. This particularly comes in handy when utilizing the hsl () function to create a color palette for your site.  The hsl function defines a color according to its hue, saturation, and lightness. First you define the hue, saturation, and lightness as CSS custom properties. You then can use the calc function to change these three aspects of the resulting color. Creating a site that is cohesive can increase user activity. It can also save time because as a developer you know the colors you are using are automatically similar. For example, usually to find complementary colors I would visit Adobe Color Wheel. However, using this function would make it a lot easier. This can also help you to create a color palette without using mixins from a preprocessor. As CSS custom properties  and logical functions gain more support in browsers I believe the above described technique of color palette will be really popular.

## The Min and Max Function
The min function also uses math operations. The min function chooses the smallest unit specified to be applied to elements. You can use this to ensure the padding around your container elements also resize when your site is being viewed from different screen sizes. The min function can also be used to incorporate a background color and a background image on your site. By doing this you would not need to use the cover property. You can set the size for the image so both the image and the color can be viewed. Similar to the landing page we did as a class project. We needed our gradient background and image to show and resize on different screen sizes. The min function can allow us to do that with ease. 

The max function also makes modern CSS easier. Max can be used to allow the viewer to zoom but keep the clarity of the content on the page. With the max function set the viewer will zoom but the font size of text will not increase or decrease after the set units specified are reached.  Max can also help create accessible target areas.  This will make it easier for people to click the buttons or areas they need no matter what device they are on. Another trick you can use can help you create margins that don’t distort the page when zoomed in. In “Practical Uses of CSS Math Functions: calc,clamp,min,max”  Stephanie Elckles recommends using rem units Both min and max can be use to create less padding on small screens and more padding or big screens. Max can also be used instead of aspect ratio or as a substitute in case a browser does not support aspect ratio to set image height. 

## The Clamp Function
The clamp function allows you to set a minimum value, an ideal value, and a maximum value. The ideal value is set with math operations. Clamp is often used to create fluid typography. Fluid typography allows viewers to read content on your site with clarity on different screen sizes. The clamp function can gradually increase or decrease the font size on your site. However, clamp can be used for much more.  Clamp can enable you to create a responsive site while reducing the amount of media queries you need. It also has added functionality over media queries. For example, when using the percent unit on the ideal value of an element padding it is relative to the element’s width. For this reason, the element’s width will remain between the minimum and maximum values specified.  Without the use of media queries, it allows your website to resize in a more dynamic way instead of static. You can save your media queries for accessible options like reduce motion or a dark mode option.  What’s also useful about the clamp function is as outline in the article “min (), max () and clamp (): three logical CSS functions to use today” you can create a clamp similar to the one shown below.

```css
p {
  width: clamp(45ch, 50%, 75ch);
}
```


 This well allow your sentences on the site not to exceed the recommended 40 to 75 characters.  You do not need to write the word “calc” in your min,max,and clamp functions. Providing just the math operation as shown below will suffice. 

