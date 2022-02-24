---
template: blog-post
title: What's Your Typeface?
slug: /whats-your-typeface
date: 2022-02-24 17:40
description: Typography
---


## How to Choose…
<p> Digital typography is essential to how your website will affect user interaction. Typography can influence the tone of your content.  Typography can make your message easier to grasp. Typography can increase or decrease a website’s user engagement. Overall, the typography you choose can negatively or positively impact the readability, accessibility, and message of your website.  Digital typography is altered by screen size, screen resolution, and screen brightness. Typography is all about the user. These general tips can help you pick a typeface with readability. Open forms improve readability. Open form typefaces will make sure letters such as “c” or “s” will be open enough for the reader to distinguish between where it begins and ends. Typefaces with distinct letters make it easier for users to read. For example, you want to find a typeface that doesn’t have the same exact styling on every letter but has subtle nuances to differentiate them. Another general rule is to limit the number of different fonts you use on a page to no more than three. Consistency makes the titles, subtitles, and paragraphs on your site more readable.  Ok you’ve picked your typefaces! Now what? Creating a great user experience through typography doesn’t just stop there. </p>


## How to Enhance…


<p> Several different aspects of typography can make your website readable and accessible. One of them is the thought process before. For example, developers should ask themselves “What piece of content is most important?” or “What will the viewer look at first?”.   This allows you to being grouping your content.  You want to separate non-related items on your website from related text. You can do this by communicating hierarchy with headings. Headings give your reader a preview of the text that is to follow. Once you determined this, you can influence what the user is drawn to by using font-weight, font-size and line height. The most important content you would want to have a distinct difference in font-size and weight than the rest of the body of text such as the title. A general rule of thumb is the smaller the typeface is the tighter the line height should be. Body line height can affect how light or heavy a paragraph looks on a page.  Usually, you want to decrease the line height of your title and increase the line height of your body. </p>
<p> Two other aspects of typography that can affect accessibility is color contrast and letter spacing. The font color use can make it difficult or easy to read your content. The background color is just as important.Background color and font color need to have a contrast. The color contrast you want is of 4.5:1 ratio. You can check your ratio using the ChromeLens extension on the Google Chrome Browser. Letter spacing can improve visual hierarchy. It is also a good idea to increase letter spacing when you have a small typeface or words in all capitalization to increase readability. Last but not least pay attention to your line length. From my various sources I got different ranges but typically you want to keep your line length to 45-75 characters per line. Wow! You have a great typeface and it’s laid out to perfection. You view your page on a mobile phone and… Yikes! Don’t worry though! I have some responsive typography tips to share with you.</p>



## How to Adapt…


<p> The general rule for font size on a website is 
•	12-16pt for a mobile screen
•	15-19pt for a tablet
•	16-20pt for a desktop computer
With different screens come different reading distances. People viewing your page on a smartphone are closer to your text than those reading your page from a desktop. This means your font needs to increase as the screen gets bigger. You can choose a base font and scale up 1x-2x as you create different media queries or clamp () functions. You can google and find a typeface scaling ratio as a reference. For large screens you want to have large side margins to keep the text center. While on small screens you want small margins so your line length can increase.  For small screens you need to increase the line height and vice versa for big screens. I hope this post helped you on your typography journey. Please reach out if you would like to share any tips that weren’t discuss in this topic.</p>

<p> <strong> Pro tip: </strong> Using vw units on typography impairs accessibility. When zooming in and out with a vw unit it could become to small on a mobile screen and to big on a desktop screen. To combat that use a clamp function like the one below:
``` css


--fs-xl: clamp (3.5rem,12vw +1rem,8rem)

```


</p>


