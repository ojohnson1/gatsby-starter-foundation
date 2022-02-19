---
template: blog-post
title: Its All About The Layer
slug: -all-about-the-layer
date: 2022-02-18 20:27
description: |
  Cascade Layers
---
Cascade Layers is a new feature to the Cascading stylesheet architecture. This feature allows web developers to have more control over specificity and order of appearance in their author stylesheets. 

## What Is It?

Why do I mention more control? Different techniques, such as BEM (Block Element Modifier), have been used to assert control over element specificity. Although, BEM solved the specificity issue by using classes. It did not solve the order of appearance issue with individual elements. This could then result in developers using overly specified identifiers for elements in an event to regain control. Cascade Layers can change all of this! 

Prior to cascade layers, Author stylesheets were the highest layer. The cascading sort order would then  determine declaration in this order:
•	Origins and importance
•	Context
•	Element-attached styles
•	Specificity
•	Order of Appearance
Cascade Layers will add a sixth determination layer for the cascade above specificity. When in use, cascade layers allow a developer to create new sublayers within their stylesheet. These sublayers can be listed at the top of the of the stylesheet with the order they should be applied. They specificity can also be applies by order of appearance on the stylesheet. Why is this so useful?

 With the use of cascade layers, it doesn’t matter an element’s individual specificity if it is competing with an element’s specificity in another layer. What matters is the layer’s specificity! This will help developers avoid frustrating CSS collisions.
 
Do you want to allow order of appearance to determine the specificity of your layers? Well, guess what? The first time you declare a layer is where its specificity lies. So, if you would like to declare that layer again somewhere else on your stylesheet it will not change its layer priority.  For example, you can add a layer to another at-rule such as @media. This flexibility allows you to update styles and media queries without effecting the overall CSS structure. Layers can also be nested in layers. They can then be referred to with a dot notation instead of the @layer selector. You can add anonymous layers to your stylesheet. This enhances your CSS’s reusability, readability, and modifiability.

## How it Works

The way that CSS works normally the selector specificity hierarchy is as follows (Weakest to Strongest):
•	Universal
•	Type 
•	Class 
•	ID

<br>
**Hello World**


```css
@layera {
  .cascade p {
    font-weight: bold;
    color: green;
  }
}

@layerb {
  p {
    color: blue;
    font-weight: bold;
  }
}

```

 As shown, a class selector has more specificity than a type selector. A text editor would display the below example selector’s specificity of “This is a test 1” as (0,0,1) and “This is a test 2” as (0,1,1).  Because the “. cascade p” has a higher specificity it will override the type selector styling of p. As you can see in the image the text displays green. Now this is when cascade layers come in handy. However, with the @layer selector all styling in the second layer would take precedent over styling in the first layer. So, a simple selector can override a stronger selector if its layer specificity is higher. Element specificity has met its match! 

## What to Watch out for…

It’s important to note that the cascade layers do not work when the important! tag is applied to an element. Important! surpasses layer specificity. This means if an important! is applied on a user agent stylesheet it will override your author agent styling. More important if an important! is applied to your CSS’s framework, such as Bootstrap, it will override it as your author styling. Keep in mind: Importance! has an inverted order of precedence. This means that an important! in one of your specified Cascade Layers will override a site normal importance!

Another important note to make is unlayered styling has a higher specificity than anything in a layer. With this logical in mind, what if you style an element both in a nested layer and in a parent layer? The parent layer styling will win. You can solve this by adding a more specific selector.

## What We Have to Look Forward To…

Stephanie Eckles predicts in her article “Getting Started with CSS Cascade Layers” that they become more popular frameworks will included layer versions. She also notes the same author of CSS Cascade Layers has a new spec on the way called “Native CSS Scoping” that will solve issues Cascade Layers can’t. Well what are you waiting for? Go try out Cascade Layers for yourself and let us know what you think. As of now, Cascade Layers can be experimented with in the Google Chrome Canary, FireFox Nightly, and Safari Technical Preview browsers. According to a twitter source however, Cascade Layers will have browser support by Firefox, Chrome, and Edge no later than March 2022. 





