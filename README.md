
# CSS: universal selector, body element and clip-path


1. **Universal selector**: universal selector is used to perform the basic reset in all of the element on the web page like heading element gets some marigin by default.

2. **Box-sizing**: Box sizing border box, what this does is to change the box model so that the borders and the paddings are no longer added to the total width or the total height that we specify for a box. Without this, any paddings and borders are added to the height or the width of an element which really isn't helpful for us, and so with this, we're getting rid of that behavior.

3. **Body-element**: body element is the parent element of all the other elemnent and the properties defined in the body element will get inherited in all the child element. and defining the properties in the body element that should be inherited in all the child element is more efficient and is best practice that defining in the universal element properties like: everything related to font-family.

4. **line-height**: line-height 1.7 means it's 1.7 times bigger than the predefined line height that we would have without this.

5. **background-size**: background-size: cover, what cover does is that whatever the width of the viewport, or the element, it will try to fit the element inside of the box.

6. **background images**: We can add two background images togeather in a element like a linerar gradient and a image and the color defined with rgba also include the opacity of the color and that is what 'a' defined in rgba.

```bash
  background-image: linear-gradient(
      to right bottom,
      rgba(126, 213, 111, 0.8),
      rgba(40, 180, 131, 0.8)
    ),
    url(../img/hero.jpg);
```

7. **background-position**:
background-position:top, will make position to stay stable on top and will crop the bottom position of the background image on zoom-in or zoom-out. 

8. **click-path**: use this website to create click-path 
it is used to create complex shapes by clipping elements. It allows you to define a clipping path for an element, which determines which parts of the element are visible and which parts are hidden or "clipped" away.
## 🔗 Links https://bennettfeely.com/clippy/
![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/click-path.png)


9. **Vh and percentage**: vh is always relative to the viewport's height, while percentage units are relative to the parent container or containing block. This makes vh particularly useful for creating elements that respond to the height of the viewport itself, making them more suitable for designing responsive layouts in certain situations.

10. **transform : translate()** 

- `transform: translate()` is a CSS property used for 2D transformations.
- It allows you to move an element along the X (horizontal) and Y (vertical) axes.
- The `translate()` function takes one or two values: `translate(tx)` for horizontal translation (X-axis) and `translate(tx, ty)` for both horizontal (X-axis) and vertical (Y-axis) translation.
- Positive values move the element to the right (X-axis) or down (Y-axis), while negative values move it to the left (X-axis) or up (Y-axis).
- Percentage values can also be used, which are relative to the element's dimensions.
- The transformation is relative to the element's current position, means it is relative to the elements itself not its parent element, allowing you to adjust an element's location without affecting its layout in the document flow.
- It's commonly used for creating animations, positioning elements precisely, and achieving responsive designs.

Remember that the direction of movement along the Y-axis may vary depending on the coordinate system, but in CSS and most screen contexts, positive values move elements downward.


11. **Animation in CSS**: There are generally two types of animations in CSS. The first one is to just set the transition property, and then change the properties that you want to animate on an event, like when we hover the element.
And the second one is a bit more advanced, and for that we use @keyframes rule. Now in here, I can specify what we want to happen in each moment of time of the animation. 0% is the before the animation actually starts and the 100%, which is when the animation finishes, and we can also put other steps in the middle as well.

12. For the browser performance, it's best to only ever animate two different properties. One is opacity, and the other one is the transform property. That's what the browsers are optimized for, for these two properties.

13. For applying an animation to an element we need to specify two things first: animation-name, second the animation-duration.

14. **CSS backface-visibility property**: If you face any shaking in your animation use backface-visibility : hidden; property in the parent element of the element to remove the shacking. basically backface-visibility property is used to hide the content from the back of the element when it gets rotated like 180 degree.

15. pseudo-classes are a special state of an element. so this link here is a state of the button selector. So like when a user hovers an element, or when a checkbox is clicked or if we want to select a last-child. We use pseudo classes to style an element under special conditions.

16. Use {display: inline-block} to set padding, height and width of an inline element like: anchor tag

17. Use of :link pseudo class on anchor element :
- a -> is for anchor tags with or without href attribute + visited links

- a:link = applies to anchor tags that have an href attribute and are not visited, active, or hovered.

- So you can for example have one style for anchors without href attribute, another style for anchors with href attribute and then different styles for :hover, :active and :visited states.

18. **CSS Transition** : The transition property allows you to define / control the transition between two states of an element.  When we choose to forgo the transition prop, we lose the ability to describe how we want our animation to run between the start and end states.
ex: when we define certain properties like: box-shadow and transform etc properties to be applied in hover state of a button element and then we apply transition property to elements initial state then the values defined in transition property in the elements initial state will describe how your animation will have happen when you hover your element. 
look below code example:

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/CSS%20Transition.png)

19. ### CSS `box-shadow` Property

- The `box-shadow` property allows you to add a shadow effect to an element, creating depth and dimension in your web design.

- It can be applied to various HTML elements like divs, buttons, and text containers.

- Syntax:
  ```css
  box-shadow: [horizontal offset] [vertical offset] [blur radius] [spread radius] [color];
  ```

  - `[horizontal offset]` defines how far the shadow spreads to the right (positive value) or left (negative value).
  - `[vertical offset]` defines how far the shadow spreads downward (positive value) or upward (negative value).
  - `[blur radius]` controls the blurriness of the shadow. Larger values make it more diffuse.
  - `[spread radius]` increases (positive value) or decreases (negative value) the size of the shadow.
  - `[color]` specifies the shadow's color.

- Examples:
  ```css
  /* Basic shadow with horizontal and vertical offsets */
  box-shadow: 4px 4px #888;

  /* Shadow with blur radius and spread radius */
  box-shadow: 0 0 10px 2px rgba(0, 0, 0, 0.2);

  /* Inset shadow (inner shadow) */
  box-shadow: inset 2px 2px 3px rgba(0, 0, 0, 0.5);

  /* Multiple shadows (comma-separated) */
  box-shadow: 3px 3px #888, -3px -3px #888;
  ```

- Key Points:
  - The `box-shadow` property is used for decorative purposes, providing a 3D effect to elements.
  - Shadows can be inset (inner shadow) or outset (outer shadow).
  - You can use multiple shadows by separating them with commas.
  - To create a shadow on all sides of an element, set horizontal and vertical offsets to 0 and adjust blur, spread, and color as needed.
  - The `rgba()` color notation allows for transparency, making it useful for subtle shadow effects.

20. ## Use of `Display block, inline, inline-block` 

1. **`block`**:
   - Use `display: block;` for elements that should start on a new line and span the full width of their parent container.
   - Common use cases include:
     - Headings (`<h1>`, `<h2>`, etc.): Each heading typically starts on a new line and occupies the full width.
     - Paragraphs (`<p>`): Paragraphs are block-level, allowing text to flow from top to bottom.

   ```css
   h1 {
     display: block;
   }
   ```

2. **`inline`**:
   - Use `display: inline;` for elements that should flow within the content, taking up only as much width as necessary.
 Just like inline-block wraps around its content. But you can't apply transform property to it.
   - Common use cases include:
     - Links (`<a>`): Links are often inline to allow them to flow within text content.
     - Emphasized text (`<em>`) or strong text (`<strong>`): Text that should be styled inline without breaking the flow.

   ```css
   a {
     display: inline;
   }
   ```

3. **`inline-block`**:
   - Use `display: inline-block;` for elements that should flow within the content but also have block-level properties like margins and padding.
 wraps around its content. you apply transform property to it.
   - Common use cases include:
     - Buttons: Buttons often need to be inline with text but have padding and margins for styling.
     - Images with captions: Images are inline with text, but captions can be displayed next to them with `display: inline-block;`.

   ```css
   .button {
     display: inline-block;
     padding: 10px 20px;
     background-color: #3498db;
     color: #fff;
   }
   ```
21. **Absolute positining**
-Now remember that this absolute positioning needs to have a reference. And the reference is the first element with the relative position that it can find. Now in this case it would be the header because remember we did that before. But we don't want it to be the header. We want it to be hidden after the button. And so, the reference should be the button. Therefore, what we have to do is to set the position property of the button to relative.

22. **transform: scale()** : The scale() CSS function defines a transformation that resizes an element on the 2D plane. Because the amount of scaling is defined by a vector [sx, sy], it can resize the horizontal and vertical dimensions at different scales. Its result is a <transform-function> data type.

23. ## Pseudo class and Pseudo element
- In CSS, pseudo-classes and pseudo-elements are selectors that allow you to target and style specific parts of HTML elements that cannot be targeted using regular selectors alone. They provide a way to apply styles based on various conditions or to select parts of an element's content.

**Pseudo-Class:**

- A pseudo-class is used to define a special state or condition of an element. It begins with a colon (`:`) followed by the name of the pseudo-class. Pseudo-classes are used to style elements based on user interaction, such as hovering, clicking, or focusing.

- Common pseudo-classes and their usage:

 1. `:hover`: Selects an element when the user hovers their mouse pointer over it. Example:

   ```css
   a:hover {
     color: red;
   }
   ```

2. `:active`: Selects an element when it's being activated, such as when a button is clicked. Example:

   ```css
   button:active {
     background-color: green;
   }
   ```

3. `:focus`: Selects an element when it has keyboard focus, typically used for form elements. Example:

   ```css
   input:focus {
     border-color: blue;
   }
   ```

**Pseudo-Element:**

- A pseudo-element is used to style a specific part of an element's content. It begins with a double colon (`::`) followed by the name of the pseudo-element. Pseudo-elements allow you to style elements' content that cannot be selected with regular selectors.

- Common pseudo-elements and their usage:

1. `::before` and `::after`: Inserts content before or after the content of an element and styles it. Example:

   ```css
   p::before {
     content: "Before: ";
     font-weight: bold;
   }
   ```

2. `::first-line` and `::first-letter`: Selects the first line or first letter of text within an element. Example:

   ```css
   p::first-line {
     font-weight: bold;
   }

   p::first-letter {
     font-size: 150%;
   }
   ```

**How to Use Pseudo-Classes and Pseudo-Elements:**

- To use pseudo-classes and pseudo-elements, follow these steps:

1. Select the target element or elements using a regular CSS selector (e.g., `a`, `button`, `input`, `p`).

2. Add a colon (`:`) followed by the name of the pseudo-class or a double colon (`::`) followed by the name of the pseudo-element.

3. Define the styles you want to apply within curly braces `{}`.

Here's a simple example applying pseudo-classes and pseudo-elements:

```css
/* Apply styles when hovering over a link */
a:hover {
  color: red;
}

/* Insert content before every paragraph */
p::before {
  content: "Important: ";
  font-weight: bold;
}
```
**Important notes**
- Pseudo-elements allow us to style certain parts of elements. For example, the after pseudo-element that we're gonna use adds like a virtual element right after the element that we're selecting. And we can then style that element.

- First, in order for an after pseudo-element to actually appear on the page, we need to specify its content property. So that's always necessary. It doesn't matter what the content is. It can even be empty like we're gonna do here, but we have to specify it. Otherwise it's not going to appear. And the same thing with the display property. So we have to specify the display property. And in this case, we're gonna say it's an inline block because the button that we have is also an inline block. And so, again, we want it to be exactly the same. We want it to look the same. So we want to have a height of 100%. And we want to have a width of 100% as well. And this works because the after pseudo-element is basically treated like a child of the button. And so if we say that we want the height to be 100%, that's 100% of the width of the button. And so suppose that the button has 100 pixels of height and 50 pixels of width. And so this after pseudo-element will have the exact same dimensions if we set it to 100%.

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/after%20Pseudo%20element.png)

24. Use of `{ animation-fill-mode: backwords }`

- Accourding to w3School: The element will get the style values that is set by the first keyframe (depends on animation-direction), and retain this during the animation-delay period.
- {animation-fill-mode: backwords} this property comes to use when we are using the animation-delay property. 
Ex:-
heading-primary-main and heading-primary-sub do not have animation-delay set, so the animation is immediately applied. To check, just add an animation-delay to those and you will see the same outcome as the button without animation-fill-mode: backwards;.  The headings will be there for the duration of the delay, then the animation will start.

With the button, by default the docs describe we have animation-fill-mode: none; , which doesn't apply any animation code. So, for the duration of animation-delay , none of the animation css is used, only the original styling is applied. With animation-fill-mode: backwards; , the 0% animation css is applied for the duration of animation-delay.

## Section: 2 How CSS works
1. Now css can also come from different sources. The most common one is the css that we the developers write. These declarations that we put in our stylesheets are called the **author** declarations. Another source can be the user declarations, which is css coming from the **user**. For instance, when the user changes the default font size in the browser then that is user css, and last but not least there are the **default browser declarations**. For instance, if we put an anchor tag in our html for a link and then don't style it at all it will usually be rendered with blue text and underlined, right. That's called the user agent css, because it's set by the browser.

2. One thing that is really important to note is that the universal selector * has **no specificity value** and so it's zero, zero, zero, zero, which means that all other selectors have a precedence over it.

3. In the below case one id and one class has higher priority over the only id
![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/priority%20over%20id.png)

4. 
The last block would win in this case, as they have the same specificity (0 0 0 3).  Even though the child combinator (>) is stricter than the descendant selector (denoted by the space), this does not affect the specificity.  In fact, no combinators affect specificity.  The weight applied to a css declaration block is determined by the the number of each selector type (reviewed in the lecture) in the matching selector.

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/child%20combinator%20and%20descendent%20selector.png)

5. Hover state also gets affected with the specificity of the targated element, if(On a normal state) you are targetting a element with a specific specificity then use the same specificity to target that element on hover state otherwise if you used a single less specificity then the normal state then the hover state will not work at all.
![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/hover%20specificity.png)

6. **Same specificity but of `different type`**

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/same%20specificity.png)

7. 
- Each time we use a unit other than pixels, like rem or vh or some other relative unit, it will ultimately be converted to pixels.

- Each element of the page, each and every css property needs to have a value even if you don't even declare it at all.

- rem unit is always relative to the root font-size.

- The percentage is technically not a unit, but to make things easier, we'll simply treat it as one.

- When we express a length measurement in percentages, like height, a padding, a margin, or something else, the reference is always the parent element's width.

- It's different to use ems for fonts or for length so both ems and rems are font-based, but the difference between them is that ems use the parent or the current element as a reference while rems use the root font-size as the reference.

- You may ask, "why should we actually size stuff with ems and rems if they are based on font-size? It seems a bit strange, right?" and the answer is that by doing so, we can build more request responsive layouts because just by changing font sizes, we will automatically change length since it depend on a font size and that gives us a lot of flexibility, and it's just a great technique.

- inheritance of a property of course only works if no one, neither the developer nor the browser, declares a value for that property.

- the line-hieght pixels are resolved by percent*currentelementfontsize. I guess there are exceptions to the rules presented in the first slides of this lecture.

- for (%) percentage there are few exception cases where parent's width is not considered for getting the actual value (for length property)and we should refer to the documentation to make sure what is being used to get the actual value. And for 'em' and 'rem' there were no exceptions and if em is used for line-height (which is a length property) I will get actual value based on current element's font-size.

- Inheritance, is simply the mechanism that allows certain properties, not all of them, to be passed from parent to child elements, if we don't specify a value for a certain (inheritable) property on a certain element.

- Not all CSS properties are inherited from parent to the child element, only the properties that are inheritable by the CSS documentation.

8. 
- We will change all the absolute pixel units to relative rem units, okay? And why are we gonna do that? Well, it's quite simple actually. It's because we want an easy way to change all the measurements on our page with one simple setting, for example, when we hit a break point to display our page on a mobile device. When that happens we want a way to decrease all the measurements in our site at the same time, and instead of writing hundreds of lines of code and in media queries, we can just change one global setting, and that is the global font size.


- We know that rem unit is always in relation to the root font-size.

- root font-size is set in the "html" selector
ex:

```CSS
html {
font-size: 10px;
}
```
- So 1 rem is equal to root font-size, means if root font-size is 16px then 1 rem is equal to 16px, And usually we root font size 10px to make conversertion from px to rem easier.

- Why Jonas prefer to define root font-size 10 px instaed 16px:-
- Because remember, 1 rem is exactly the root font size, so if 10 pixels is now the root font size, then 1 rem is 10 pixels, and so now it's really easy to replace all the pixel units with rem, because all we have to is to divide all the pixels by 10 and that's our rem, right? Now, if it was 1 rem is 16 pixels, then we would have to make a lot of calculations, and we don't want to do that, of course, so this is a pretty common technique to avoid that.

- start using "rem" unit from the start of the project. using em to define units is a lot of work so Jonas always uses "rem" to define units in his projects.

- if you want to use values below 1, in that case you don't need write 0 before the dot like: .5 is good than 0.5 , its just all about coding practice.

- if we define root font-size in the html tag like:

```CSS
html {
font-size: 10px;
}
```
- in this case we are overwriting the root font-size property from the browser. and we are also using the absolute unit "px" means now if user want to increase font-size of our web-page then it is not possible because we have hard-coded it.
- So thats why developers prefers using (%) percentages insted of "px" for root font-size in html tag, But we want to use 10px instead of 16px (browsers default font-size) so insted of 100% that is 16px on computed we can use 62.5% that is 10/16 * 100 = 62.5%, means 62.5% of 16 = 10

- And if now when user changes suppose default font-size from 16px to 22px then the root font-size will be 62.5% of 22 = 13.75 
Now user can manipulate the root font-size.

- Specificity-wise, the universal selector has the lowest specificity, followed by the body selector, and the html selector has higher specificity.

9. 
- Why to use rem instead of another unit, because it is only relative to root font-size and by changing root font-size on different break-points through media queries we can make our web page responsive.

- body is like parents and * represents all children created inside the body. Thus, * will inherit most of property from body such as font size, font family. Jonas moved "box-sizing: border-box" to body and he wanted all individual element inside body inherit it too. However, box-sizing is not an inherited property, so he wrote like below to make the inheritance happen.

```CSS
*{
box-sizing: inherit;
}
```
- The reason he moved "box-sizing: border-box" to body is to make it easier to change box-sizing in child element. In case we want to use a different property for box-sizing in some components, we can change it easily because style declarations that match an element within body can override the inherited style.

- Basically, all basic set up will be written in body in order to be inherited by child elements.

- Because not all properties can be inherited from body so  we need to set up initial step for all element in * such as box-sizing, margin, padding.. we need to set up in here.

- In specific class selector, we can write a special style properties applied for this selector. For example: in header, font-size can be different from what it is inherited from body. Besides that, we can add more for class header such as background image, position...

- First, we talked about the cascade and so now it's time to talk about how values are processed in a CSS parsing phase.

- Each time we use a unit other than pixels, like rem or vh or some other relative unit, it will ultimately be converted to pixels.

- Each element of the page, each and every css property needs to have a value even if you don't even declare it at all.

- rem unit is always relative to the root font-size.

- The percentage is technically not a unit, but to make things easier, we'll simply treat it as one.

- When we express a length measurement in percentages, like height, a padding, a margin, or something else, the reference is always the parent element's width.

- It's different to use ems for fonts or for length so both ems and rems are font-based, but the difference between them is that ems use the parent or the current element as a reference while rems use the root font-size as the reference.

- You may ask, "why should we actually size stuff with ems and rems if they are based on font-size? It seems a bit strange, right?" and the answer is that by doing so, we can build more request responsive layouts because just by changing font sizes, we will automatically change length since it depend on a font size and that gives us a lot of flexibility, and it's just a great technique.

- The fill area. Remember how the text content and images go inside the content box? The same does actually not apply for background images or the background color of the box. These properties will be applied not only to the content box but to the entire fill area, which also includes the padding and the border, but not the margin.

- In the default value of the box-modal when we define width or height of a element/box the padding and border get added to what we defined.

- If we set box sizing to border box, the height and the width will be defined for the entire box including the padding and the border and not just for the content area. What this means, at the same time is that the paddings and borders that we specify, will of course reduce the inner width of the content area, instead of adding them to the total height or width of an element.

- height and width only applies to the block-level boxes.
- The type of boxes is determined by the display property.

- A common misconception is that only the z index property creates new stacking contexts, but that's not the case. An opacity value different from one, a transform, a filter or other properties, will also create new stacking contexts. That's why sometimes, even with the z index set on a positioned element, the stacking order doesn't work as expected.

- So after thinking about your design, we need to code the design using html and css, and in this step, it's important to have a consistent strategy and structure for naming our classes. There are many approaches for naming classes. Things like object-oriented css or s max but the one i like the most is bem, which is becoming more and more popular by developers around the world. It's a nice clean system for marking up our layouts. So, bem stands for block element modifier.

- The base folder where we put the basic product definitions, the components folder where we have one file for each component, the layout folder, where we define the overall layout of the project, the pages folder where we have styles for specific pages of the project, the themes folder if you want to implement different visual themes, the abstracts folder where we put code that doesn't output any css, such as variables or mix-ins, and finally, the vendors folder where all third party css goes.

 Having low specificity is a good thing :-
- Because high-specificity selectors get in the way of controlling your code; you have to dig through multiple layers of specificity to over-ride any given style, which is bad for maintenance and scalability; and your code can quickly become a dis-organized mess that just slaps more and more specific selectors for every tiny change to your code, because neither you nor your colleagues want to dig-through those layers to find out the original code.
- Having high specificity makes you forget what selectors control what element over time; not the other way around.
