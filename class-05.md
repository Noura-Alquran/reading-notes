# class-05 summary
## Images in HTML:
* If you are building a site from scratch, it is good practice to create a folder for all of the images the site uses.
* To add an image into the page you need to use an < img > element. This is an empty element (which means there is no closing tag). It must carry the following attributes:
  1. ***src*** : This tells the browser where it can find the image file( maybe relative url).
  2. ***alt*** : This provides a text description of the image which describes the image if you cannot see it.
  3. ***title*** : This provides additional information about the image. 
  4. ***height*** :This specifies the height of the image in pixels.
  5. ***width*** : This specifies the width of the image in pixels.
* Where to Place Images in Your Code ?
  + before a paragraph : The paragraph starts on a new line after the image.
  +  Inside the start of a paragraph : The first row of text aligns with the bottom of the image.
  + In the middle of a paragraph :The image is placed between the words of the paragraph that it appears in.
* The align attribute was commonly used to indicate how the other parts of a page should flow around an image.
 ***It has been removed from HTML5 and new websites should use CSS to control the alignment of images .***
* The align attribute can take these horizontal values: left /right.
* The align attribute can take these vertical values : top/middle/bottom.
* There are three rules to remember when you are creating images for your website which are :
   1. **Save images in the right format** : Websites mainly use images in jpeg, gif, or png format.
   2. **Save images at the right size.**
   3. **Use the correct resolution** : Computer screens are made up of dots known as ***pixels***. Images used on the web are also made up of tiny dots. ***Resolution*** refers to the number of dots per inch, and most computer screens only show web pages at 72 pixels per inch. So saving images at a higher resolution results in images that are larger than necessary and take longer to download.
   * When cropping images it is important not to lose valuable information. It is best to source images that are the correct shape if possible.
   * Vector images differ from bitmap images and are resolution-independent. Vector images are commonly created in programs such as Adobe Illustrator.
   * Animated GIFs show several frames of an image in sequence and therefore can be used to create simple animations.
   * Creating an image that is partially transparent (or "see-through") for the web involves selecting one of two formats: Transparent GIF / PNG.
   * HTML5 has introduced a new < figure > element to contain images and their caption so that the two are associated. You can have more than one image inside the < figur e> element as long as they all share the same caption. <figcaption> The <figcaption> element has been added to HTML5 in order to allow web page authors to add a caption to an image. Before these elements were created there was no way to associate an <img> element with its caption.

## Color in CSS:
*  The **color property** allows you to specify the color of text inside an element. 
* You can specify any color in CSS in one of three ways:
  1. ***rgb values*** :These express colors in terms of how much red, green and blue are used to make it up(Values for red, green, and blue are expressed as numbers between 0 and 255 ).
   + We can adds a fourth value to indicate opacity. This value is known as an alpha value and is a number between 0.0 and 1.0.
  2. ***hex codes*** : These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. ( in hexadecimal code.) 
  3. ***color names*** There are 147 predefined color names that are recognized by browsers. 
  4. Else way using: ***Hue***+ ***Saturation***(Saturation refers to the amount of gray in a color) + ***Brightness*** refers to how much black is in a color.

* CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names.

* It is important to ensure that there is enough contrast between any text and the background color (otherwise people will not be able to read your content).
* The ***opacity property*** which allows you to specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0 (so a value of 0.5 is 50% opacity and 0.15 is 15% opacity).
* CSS3 has introduced an extra value for RGB colors to indicate opacity. It is known as RGBA.
* CSS3 allows to specify colors as HSL values, with an optional opacity value. It is known as HSLA.

## Text :
* The properties that allow you to control the appearance of text can be split into
two groups:
  1. Those that directly affect the font and its appearance (including the typeface, whether it is regular, bold or italic, and the size of the text). 
  2. Those that would have the same effect on text no matter what font you were using (including the color of text and the spacing between words and letters)

* **Typeface Terminology**

![image](https://ingenexdigital.com/wp-content/uploads/ingenex-blog-classifications-1024x703.jpg);

* When choosing a typeface, it is important to understand that a browser will usually only display it if it's installed on that user's computer.

* ![imaged](https://slideplayer.com/slide/12853079/78/images/6/%3E%3E+Continue+%3A+Font+Selection+%26+Web+Design.jpg)
* The ***font-family property*** allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.
* The ***font-size property*** enables you to specify a size for the font. There are several ways to specify the size of a font (px ,percentage and ems).
* ***@font-face*** allows you to use a font, even if it is not installed on the computer of the person browsing, by allowing you to specify a path to a copy of the font, which will be downloaded if it is not on the user's machine.
* The ***font-weight property*** allows you to create bold text. There are two values that this property commonly takes:
   1. normal : This causes text to appear at a normal weight.
   2. bold :This causes text to appear bold.
* ***The font-style property***. There are three values this property can take:
   1. normal :This causes text to appear in a normal style (as opposed to italic or oblique).
   2. italic :This causes text to appear italic.
   3. oblique :This causes text to appear oblique.
* The ***text-transform property***is used to change the case of text giving it one of the following values:
    1. uppercase : This causes the text to appear uppercase.
    2. lowercase : This causes the text to appear lowercase.
    3. capitalize : This causes the first letter of each word to appear capitalized.
* The text-decoration property allows you to specify the following values:
    1. none  :This removes any decoration already applied to the text.
    2. underline :This adds a line underneath the text.
    3. overline : This adds a line over the top of the text.
    4. line-through : This adds a line through words.
    5. blink : This animates the text to make it flash on and off (however this is generally frowned upon, as it is considered rather annoying).
* Leading ***pronounced ledding*** is a term typographers use for the vertical space between lines of text. In a typeface, the part of a letter that drops beneath the baseline is called a *descender*, while the highest point of a letter is called the *ascender*. Leading is measured from the bottom of the descender on one line to the top of the ascender on the next.
* In CSS, the line-height property sets the height of an entire line of text, so the difference between the fontsize and the line-height is equivalent to the leading (as shown in the diagram above). Increasing the line-height makes the vertical gap between lines of text larger.
* **Kerning** is the term typographers use for the space between each letter. You can control the space between each letter with the ***letter-spacing property***.You can also control the gap between words using the ***word-spacing property***.
* The ***text-align property*** allows you to control the alignment of text. The property can take one of four values:
   1. left :This indicates that the text should be left-aligned.
   2. right :This indicates that the text should be right-aligned.
   3. center :This allows you to center text.
   4. justify : This indicates that every line in a paragraph, except the last line, should be set to take up the full width of the containing box.
* The ***text-indent property*** allows you to indent the first line of text within an element. The amount you want the line indented by can be specified in a number of ways but is usually given in pixels or ems.

* The ***text-shadow property*** used to create a drop shadow, which is a dark version of the word just behind it and slightly offset. It can also be used to create an embossed effect by adding a shadow that is slightly lighter than the text.
* You can specify different values for the first letter or first line of text inside an element using
  :first-letter and
  :first-line.
  Technically these are not properties. They are known as ***pseudo-elements***.
* :link  :This allows you to set styles for links that have not yet been visited.
* :visited  : This allows you to set styles for links that have been clicked on.

* ![image](https://www.programmersought.com/images/313/ddbc6cc6fc652ba2174f900ce2eedb09.png)