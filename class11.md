# class-11 summary
## Images:
* We can control the size of animage using the **width** and **height** properties in CSS, just like we can for any other box.
* Aligning an image means to position the image at center, left and right. We can use the **float property** and **text-align property** for the alignment of images.Also , we can add a **margin** to the image to ensure that the text does not touch their edges.In addition,we can use the margin property and set the values of the left and right margins to auto to position the image at center.
* By default, images are *inline elements*. This means that they flow within the surrounding text. In order to *center an image*, it should be turned into a blocklevel element using the **display property** with a value of *block*.
* The **background-image property** allows you to place an image behind any HTML element. By default, a background image will repeat to fill the entire box.The path to the image follows the letters url, and it is put inside parentheses and quotes.
* The background-repeat property can have four values:
   1. repeat : The background image is repeated both horizontally and vertically (the default way it is shown if the backgroundrepeat property isn't used).
   2. repeat-x : The image is repeated horizontally only .
   3. repeat-y : The image is repeated vertically only.
   4. no-repeat : The image is only shown once.
* The **background-attachment** property specifies whether a background image should stay in one position or move as the user scrolls up and down the page. It can have one of two values:
   1. **fixed** :The background image stays in the same position on the page.
   2. **scroll** The background image moves up and down as the user scrolls up and down the page.
* When an image is not being repeated, you can use the **background-position** property to specify where in the browser window the background image should be placed. This property usually has a pair of values. The first represents the horizontal position and the second represents the vertical: left top / left center/ left bottom / center top / center center / center bottom / right top / right center / right bottom.
   + **Notes**:If you only specify one value, the second value will default to center.You can also use a pair of pixels or percentages.
* The background properties must be specified in the following order, but you can miss any value if you do not want to specify it.
    1. background-color
    2.  background-image
    3.  background-repeat
    4.  background-attachment
    5. background-position
* **Rollover** : Using CSS, it is possible to create a link or button that changes to a second style when a user moves their mouse over it and a third style when they click on it.This is achieved by setting a background image for the link or button that has three different styles of the same button (but only allows enough space to show one of them at a time).
*  When a single image is used for several different parts of an interface, it is known as a **sprite**.The advantage of using sprites is that the web browser only needs to request one image rather than many images, which can make the web page load faster.
* If you want to overlay text on a background image, the image must be low contrast in order for the text to be legible.

## Practical Information
* **Search Engine Optimization (SEO)**: is the practice of trying to help your site appear nearer the top of search engine results when people look for the topics that your website covers.
* **On-page techniques**:  are the methods you can use on your web pages to improve their rating in search engines.
* **Off-Page Techniques**: Search engines help determine how to rank your site by looking at the number of other sites that link to yours.
* In every page of your website there are seven key places where keywords (the words people might search on to find your site) can appear in order to improve its findability.
  1. Page Title
  2. URL / Web Address
  3. Headings
  4. Text
  5. Link Text 
  6. Image Alt Text
  7. Page Descriptions (specified using a <meta> tag.)
* Determining which keywords to use on your site can be one of the hardest tasks when you start to think about SEO. There are six steps that will help you identify the right keywords and phrases for your site.
  1. **Brainstorm** : List down the words that someone might type into Google to find your site.
  2. **Organize**  : Group the keywords into separate lists for the different sections or categories of your website.
  3. **Research**  : There are several tools that let you enter your keywords and then they will suggest additional keywords you might like to consider, such as: adwords.google.co.uk/select/KeywordToolExternal
  4. **Compare**: is very unlikely that your site will appear at the top of the search results for every keyword. Some of the keyword research sites can tell you how many people have searched for a specific keyword to help you know how much competitionthose terms have.  This will help you to determine how many sites have that keyword in the title of their pages. 
  5. **Refine** : pick which keywords you will focus on. These should always be the ones that are most relevant to each section of your site.
  6. **Map** : start picking which keywords you will use for each page.
* As soon as people start coming to your site, you can start analyzing how they found it, what they were looking at and at what point they are leaving. One of the best tools for doing this is a free service offered by Google called **Google Analytics**.
 ![image](https://mk0zofoqaluvgdskgvsb.kinstacdn.com/photos/landing-page-analytics-overview.png)
  + The overview page gives you a snapshot of the key information you are likely to want to know. In particular, it tells you how many people are coming to your site.
  + The content link on the left-hand side allows you to learn more about what the visitors are looking at when they come to your site.
  + The traffic sources link on the left hand side allows you to learn where your visitors are coming from.
* In order to put your site on the web you will need a **domain name** and **web hosting**.The domain name is your web address.
* **Disk space** This refers to the total size of all of the files that make up your site (all of the HTML and CSS files, images and scripts).
* **Bandwidth** : This is the amount of data the hosting company will send to your site's visitors.
* **Backups** : to restore your website in the event of a server breaking.
* To transfer your code and images from your computer to your hosting company, you use something known as **File Transfer Protocol FTP**.
* Many companies provide platforms for blogging, email newsletters, e-commerce and other popular website tools (to save you writing them from scratch).

## Video and Audio APIs:
* The < video > and < audio > elements allow us to embed video and audio into web pages.You need to set **src attribute** to identify the media source and include a **controls attribute** so the user can play and pause the media.
* You can use <source> tag to specify media along with media type and many other attributes. A video element allows multiple source elements and browser will use the first recognized format.
* The HTML5 video tag can have a number of attributes to control the look and feel and various functionalities of the control:
  1. **autoplay** : This Boolean attribute if specified, the video will automatically begin to play back as soon as it can do so without stopping to finish loading the data.
  2. **autobuffer** :This Boolean attribute if specified, the video will automatically begin buffering even if it's not set to automatically play.
  3. **controls**:  allow the user to control video playback, including volume, seeking, and pause/resume playback.
  4. **height**  :This attribute specifies the height of the video's display area, in CSS pixels.
  5. **loop** : This Boolean attribute if specified, will allow video automatically seek back to the start after reaching at the end.
  6. **preload** : This attribute specifies that the video will be loaded at page load, and ready to run. Ignored if autoplay is present.
  7. **poster** : This is a URL of an image to show until the user plays or seeks.
  8. **src** : The URL of the video to embed. This is optional; you may instead use the < source > element within the video block to specify the video to embed.
  9. **width** : This attribute specifies the width of the video's display area, in CSS pixels.
*  the HTMLMediaElement API provides features to allow you to control video and audio players programmatically — for example HTMLMediaElement.play(), HTMLMediaElement.pause(), etc.
* For controls we can use < button >tag   with  data-icon attribute for defining what icon should be shown on each button  and aria-label attribute to provide an understandable description of each button. We lay out the buttons inside the control bar using Flexbox (CSS display properity: flex), to make things easier.
* The **visibility CSS property** shows or hides an element without changing the layout of a document. T
* We can use CSS **visibility properity** of the custom controls set to *hidden*.But, In our JavaScript later on, we will set the controls to *visible*, and remove the controls attribute from the < video > element. This is so that, if the JavaScript doesn't load for some reason, users can still use the video with the native controls.
* The **opacity**CSS property sets the opacity of an element. Opacity is the degree to which content behind an element is hidden, and is the opposite of transparency.
* In CSS, **::before** creates a pseudo-element that is the first child of the selected element. It is often used to add cosmetic content to an element with the content property. It is inline by default.
* Implementing the JavaScript :first we use the **querySelector() method** which returns the first element that matches a specified CSS selector(s) in the document.then we use **removeAttribute('controls')** and set the controls to visible using **controls.style.visibility = 'visible';**
then use **addEventListener** and create functions to each button.

## Flash, Video & Audio
* Since the late 1990s, Flash has been a very popular tool for creating animations, and later for playing audio and video in websites.
*  Flash is not supported on iPhone or iPad.

