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

18. **CSS Transition** : The transition property allows you to define / control the transition between two states of an element. When we choose to forgo the transition prop, we lose the ability to describe how we want our animation to run between the start and end states.
    ex: when we define certain properties like: box-shadow and transform etc properties to be applied in hover state of a button element and then we apply transition property to elements initial state then the values defined in transition property in the elements initial state will describe how your animation will have happen when you hover your element.
    look below code example:

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/CSS%20Transition.png)

19. ### CSS `box-shadow` Property

- The `box-shadow` property allows you to add a shadow effect to an element, creating depth and dimension in your web design.

- It can be applied to various HTML elements like divs, buttons, and text containers.

- Syntax:

  ```css
  box-shadow: [horizontal offset] [vertical offset] [blur radius] [spread
    radius] [color];
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

1. **`inline`**:

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

1. **`inline-block`**:

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

1. **Absolute positining**
   -Now remember that this absolute positioning needs to have a reference. And the reference is the first element with the relative position that it can find. Now in this case it would be the header because remember we did that before. But we don't want it to be the header. We want it to be hidden after the button. And so, the reference should be the button. Therefore, what we have to do is to set the position property of the button to relative.

1. **transform: scale()** : The scale() CSS function defines a transformation that resizes an element on the 2D plane. Because the amount of scaling is defined by a vector [sx, sy], it can resize the horizontal and vertical dimensions at different scales. Its result is a <transform-function> data type.

1. ## Pseudo class and Pseudo element

- In CSS, pseudo-classes and pseudo-elements are selectors that allow you to target and style specific parts of HTML elements that cannot be targeted using regular selectors alone. They provide a way to apply styles based on various conditions or to select parts of an element's content.

**Pseudo-Class:**

- A pseudo-class is used to define a special state or condition of an element. It begins with a colon (`:`) followed by the name of the pseudo-class. Pseudo-classes are used to style elements based on user interaction, such as hovering, clicking, or focusing.

- Common pseudo-classes and their usage:

1.  `:hover`: Selects an element when the user hovers their mouse pointer over it. Example:

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
  heading-primary-main and heading-primary-sub do not have animation-delay set, so the animation is immediately applied. To check, just add an animation-delay to those and you will see the same outcome as the button without animation-fill-mode: backwards;. The headings will be there for the duration of the delay, then the animation will start.

With the button, by default the docs describe we have animation-fill-mode: none; , which doesn't apply any animation code. So, for the duration of animation-delay , none of the animation css is used, only the original styling is applied. With animation-fill-mode: backwards; , the 0% animation css is applied for the duration of animation-delay.

## Section: 2 How CSS works

1. Now css can also come from different sources. The most common one is the css that we the developers write. These declarations that we put in our stylesheets are called the **author** declarations. Another source can be the user declarations, which is css coming from the **user**. For instance, when the user changes the default font size in the browser then that is user css, and last but not least there are the **default browser declarations**. For instance, if we put an anchor tag in our html for a link and then don't style it at all it will usually be rendered with blue text and underlined, right. That's called the user agent css, because it's set by the browser.

2. One thing that is really important to note is that the universal selector \* has **no specificity value** and so it's zero, zero, zero, zero, which means that all other selectors have a precedence over it.

3. In the below case one id and one class has higher priority over the only id
   ![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/priority%20over%20id.png)

4. The last block would win in this case, as they have the same specificity (0 0 0 3). Even though the child combinator (>) is stricter than the descendant selector (denoted by the space), this does not affect the specificity. In fact, no combinators affect specificity. The weight applied to a css declaration block is determined by the the number of each selector type (reviewed in the lecture) in the matching selector.

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

- the line-hieght pixels are resolved by percent\*currentelementfontsize. I guess there are exceptions to the rules presented in the first slides of this lecture.

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
- So thats why developers prefers using (%) percentages insted of "px" for root font-size in html tag, But we want to use 10px instead of 16px (browsers default font-size) so insted of 100% that is 16px on computed we can use 62.5% that is 10/16 \* 100 = 62.5%, means 62.5% of 16 = 10

- And if now when user changes suppose default font-size from 16px to 22px then the root font-size will be 62.5% of 22 = 13.75
  Now user can manipulate the root font-size.

- Specificity-wise, the universal selector has the lowest specificity, followed by the body selector, and the html selector has higher specificity.

9.

- Why to use rem instead of another unit, because it is only relative to root font-size and by changing root font-size on different break-points through media queries we can make our web page responsive.

- body is like parents and _ represents all children created inside the body. Thus, _ will inherit most of property from body such as font size, font family. Jonas moved "box-sizing: border-box" to body and he wanted all individual element inside body inherit it too. However, box-sizing is not an inherited property, so he wrote like below to make the inheritance happen.

```CSS
*{
box-sizing: inherit;
}
```

- The reason he moved "box-sizing: border-box" to body is to make it easier to change box-sizing in child element. In case we want to use a different property for box-sizing in some components, we can change it easily because style declarations that match an element within body can override the inherited style.

- Basically, all basic set up will be written in body in order to be inherited by child elements.

- Because not all properties can be inherited from body so we need to set up initial step for all element in \* such as box-sizing, margin, padding.. we need to set up in here.

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

## Section: 4 SASS and NPM

1. **FIRST STEP WITH SASS AND NESTING:-**

- Sass is an extention to CSS language, We would need to compile Sass code to back CSS code and for that we would have to need a compiler.

- "live sass compiler" to compile SCSS code.

- If we wanted to use SASS on our local computer right now, then we would first have to install and configure it and then compile the SASS code to CSS.

- Both Sass and SCSS syntax lead to Sass code but the differencse is only the curley brases, so we are gonna use SCSS.

SCSS::-

- In SCSS the variable name always written starting with the '$' sign.

- ampersand basically writes out the selector path at the current point in code.
- WHen using the pseudo classes in nesting SCSS file, use "&" ampharsand to write correct selector path.

2. **Kind of NPM packages**
   "Developer dependencies," often referred to as "devDependencies," is a term commonly used in the context of Node.js and JavaScript projects, specifically when working with the Node Package Manager (npm) or Yarn. Developer dependencies are packages or modules that are necessary for the development and testing of a project but are not required for its production runtime.

In a typical Node.js project, you have two types of dependencies:

1. **Production dependencies (dependencies)**: These are the packages that your application relies on to run in a production environment. These packages are essential for the core functionality of your application.

2. **Developer dependencies (devDependencies)**: These are packages that are necessary for development, testing, and building of your project. They are not included in the production build of your application. Developer dependencies often include tools for testing, transpilation, bundling, linting, and more.

Here's how you specify and manage developer dependencies in a `package.json` file, which is the configuration file for Node.js projects:

```json
{
  "name": "my-node-app",
  "version": "1.0.0",
  "dependencies": {
    "express": "^4.17.1" // Production dependency
  },
  "devDependencies": {
    "mocha": "^9.0.3", // Developer dependency for testing
    "babel": "^7.15.0", // Developer dependency for transpilation
    "webpack": "^5.51.1" // Developer dependency for bundling
  }
}
```

To install both types of dependencies, you can use the following npm commands:

- To install production dependencies only: `npm install --only=prod` or `npm install --production`
- To install both production and developer dependencies: `npm install` or simply `npm i`

By separating developer dependencies from production dependencies, you keep your production build leaner and avoid including unnecessary tools and libraries that are only needed during development and testing. This practice helps reduce the size of your final application bundle and keeps it more efficient for deployment.

- Now starting from npm version 5.0.0, you no longer need to use the --save-dev flag explicitly. When you install a package using npm install, npm automatically detects whether the package is a development dependency (based on the context in which it's installed) and places it in the appropriate section of your package.json file.

HTML file:
![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/HTML%20for%20SCSS%20code.png)

SCSS file:
![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/extends%20functions.png) 3. **Sass setup in local system**
Most important part of Sass is that it is only for developers not for browsers, We developer just use Sass for our ease, that is why we install a Sass compiler to convert Sass code back to CSS for the browsers

Now there are two ways to configure Sass in our local system

1. using npm package

- npm i node-sass
- Create **sass** named folder on upper level and inside that create **main.scss** file (in order to use scss syntax otherwise create **main.sass**)
- Add this script in your package.json file, **-w** flag here watch any changes in main.scss file and runs this script in terminal automatically.

```CSS
"scripts": {
    "compile:sass": "node-sass sass/main.scss css/style.css -w"
  },
```

2. using live-sass vs-code extention

- install **live-sass** extention in vs-code editior.

```CSS
--replace this line in HTML--
  <link rel="stylesheet" href="css/style.css" />

--with this line--
  <link rel="stylesheet" href="sass/main.css" />

```

- start Sass extention by clicking on **Watch Sass** icon in vs-code footer.

## Section: 5

1. **The use of max-width**
   In CSS, the `max-width` property is used to set the maximum width that an element can have. It allows you to limit the width of an element so that it does not exceed a specified value, even if the container or viewport is wider. This is particularly useful for creating responsive designs that adapt to different screen sizes. And if the view-port/parent width is less than specified max-width then element will adjust itself in the given width.

Here's how `max-width` works:

1. **Element Width Restriction**: When you apply the `max-width` property to an element, you are essentially telling the browser that the element should not become wider than the specified value, regardless of its content or the size of its parent container.

2. **Content Adjustment**: If the content within the element is narrower than the specified `max-width`, the element will naturally adjust its width to match the content. In this case, the `max-width` property has no effect because the element's content determines its width.

3. **Container Consideration**: If the parent container of the element has a width that is less than the specified `max-width`, the element will be restricted by the parent's width. The `max-width` property only comes into play when the parent container's width is wider than the specified `max-width`.

Here's an example of how `max-width` is used in CSS:

```css
.container {
  max-width: 800px; /* Restrict the container's width to a maximum of 800 pixels */
}

.image {
  max-width: 100%; /* Restrict the image's width to a maximum of its parent container's width */
  height: auto; /* Maintain the image's aspect ratio while resizing */
}
```

In this example, the `.container` element has its maximum width set to 800 pixels, ensuring that it won't exceed that width, even if the viewport is wider. The `.image` element inside the container has its maximum width set to 100% of its parent container's width, which means it will resize proportionally with the container and maintain its aspect ratio.

The `max-width` property is commonly used in responsive web design to create layouts that adapt gracefully to different screen sizes, preventing elements from becoming too wide and ensuring readability and aesthetics on a variety of devices.

2. Custom GRID, attribute selector, :not() pseudo class and calc() function

- What is a grid: A grid is a design system which allows us to build consistent interfaces.

- The trick to centre a block element inside another block element::-
- set its width and then set the margin: 0 auto;

- :last-child{} selects the last-child of the element
- :not(:last-child{}) selects every element except the last-child

- CSS calc() function::-
  In CSS, there is an extremely powerful function which is called calc(). In here, you can do mathematical operations, and you can actually mix units in here.

Difference between calc() and Sass operator::-
Because in Sass, we can also do operations of course but we cannot do them with multiple units, so we cannot for example mix rem with pixels, with percentages. It's actually pretty logical why it is that way. It is so because we compile our sass file while we're developing the page, so even before the page is served of course to the user but this kind of calculation all depends on the layout, so it has to happen while the website is rendered using the visual formatting model. That's when these calculations can occur because it's only then that css and when the browser knows what the percentage is, what the rem is, and what all of that stuff is.

- In order to use Sass variables in the calc() function, You have to put them inside the #{Sass variable} curly braces and prefix that with a "#" symbol.

- Attribute selector [name of the attribute]{}
  ex:
  ![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/attribute%20selector.png)

3. **CSS text-align: center; property**
   "The text-align CSS property sets the horizontal alignment of the inline-level content inside a block element or table-cell box. This means it works like vertical-align but in the horizontal direction" can be broken down as follows:

- **Text-Align Sets Horizontal Alignment:** The `text-align` CSS property is used to control the horizontal alignment of content within an element. It affects how the text or inline-level content inside that element is positioned horizontally.

- **Inline-Level Content:** `text-align` primarily applies to inline-level content, such as text, inline elements (e.g., `<span>`), or inline-block elements, that is contained within a block-level element (e.g., `<div>`, `<p>`) or a table-cell box (used in tables).

- **Horizontal Direction:** `text-align` works in the horizontal direction, meaning it controls how content is aligned left or right within the block-level element or table-cell box. It determines whether the content is aligned to the left, right, centered, justified, etc., in relation to the element's container.

- **Comparison to Vertical-Align:** The statement draws a parallel between `text-align` and `vertical-align`. `vertical-align` is another CSS property, but it controls the vertical alignment of inline or inline-block elements within their line boxes or table cells. In essence, `vertical-align` adjusts the vertical positioning of content, while `text-align` adjusts the horizontal positioning.

In summary, `text-align` is used to set how inline-level content is horizontally aligned within a block-level element or table-cell box, while `vertical-align` is used for vertical alignment. These properties collectively enable precise control over the alignment of content within elements on a web page.

4. **Q In \_home.scss for .section-about we set margin-top: -20vh . Then the grey background of the about-section will be BELOW the green background image of the header (on the parts that overlap after applying the negative margin). Why is it below the green background image? Shouldn't it have a greater z-index as it appears later in the code?**

**Ans:**
Technically, there is no z-index on the element .section-about . In the context of your question "shouldn't it have a greater z-index as it appears later in the code", yes, the fact that the element appears later in the code is the reason .section-about should overlap the header. Now, you can see that this is not the case. Why is that? Well, it's because we created a stacking context (basically allowing us to use z-index values) when we set the position to relative on the .header element--we kind of created a stacking context twice, but I'll get to that in a second. Positioning the element, header, to relative, positioned the element according to its natural location in the document; but now, with a stacking context in place, positions the element above neighboring elements without an explicitly defined z-index.

Remember I said "we kind of created 2 stacking contexts?". Technically there is only one in effect here, but the clip-path property actually creates a stacking context as well as the position property. So, if you removed the relative positioning on the header, then the sibling element, .section-about , would still remain below the header.

5. **Can I Use z-index property on a non-positioned element?**

- No, the z-index property will have no effect on a non-positioned (i.e., an element with position set to its default value, which is usually static) element. z-index is designed to control the stacking order of positioned elements, such as those with position: relative, position: absolute, position: fixed, or position: sticky.

- If you apply z-index to a non-positioned element, it won't create a new stacking context, and the value you specify for z-index will be ignored. The element will follow the normal document flow and stacking order based on its position in the HTML structure.

6. **:not() Pseudo class**

- The :not() CSS pseudo-class represents elements that do not match a list of selectors. Since it prevents specific items from being selected, it is known as the negation pseudo-class.

7. **Direct child in HTML and CSS**
   In HTML, a direct child refers to an element that is nested directly inside another element, and there are no other elements in between them. The direct child is one level deep in the document structure and is a direct descendant of the parent element.

For example, consider the following HTML code:

```html
<div id="parent">
  <p>Direct child 1</p>
  <!-- This <p> element is a direct child of the <div> -->
  <span>Direct child 2</span>
  <!-- This <span> element is also a direct child of the <div> -->
  <div>
    <p>Nested child</p>
    <!-- This <p> element is not a direct child of the <div>, as it is nested inside another <div> -->
  </div>
</div>
```

In CSS, you can target direct child elements using the child combinator (`>`) in your selector. The child combinator selects elements that are direct children of a specified parent element. Here's the syntax:

```css
parent > child {
  /* CSS styles for direct child elements */
}
```

- `parent` represents the parent element.
- `child` represents the direct child element you want to target.

For example, if you have an HTML structure like this:

```html
<div class="parent">
  <p>Direct child 1</p>
  <span>Direct child 2</span>
</div>
```

You can target the direct children of the `.parent` element like this in CSS:

```css
.parent > p {
  /* CSS styles for direct <p> children of .parent */
}

.parent > span {
  /* CSS styles for direct <span> children of .parent */
}
```

In this example, the `>` combinator ensures that the styles apply only to the `<p>` and `<span>` elements that are direct children of the `.parent` element, and not to nested elements further down in the hierarchy.

- with (\*) you can target all the direct children

```CSS
parent > * {
// code for all the direct children
}
```

8. **Icons in HTML**

- When using icons on your webpage use icon-vector or SVG but do not use PNG as icons. because images become blur when gets scaled.

- it has become the convention to use (<i> </i>) tag for icons in HTML, In reality (<i> </i>) tag was used to make the text italic but it is no longer used to make text italic. So we use it for icons.

- To increase the size of the font-icon brought from the internet, we use font-size instead of width.

- icon-fonts is just a text.

9. CSS `perspective` property:

1. **3D Transformations:** The `perspective` property is used to create a 3D rendering effect in CSS, allowing you to add depth to elements on a web page.

1. **Applied to Parent Elements:** It is typically applied to a parent container element, and it defines the distance between the viewer and the 3D-transformed elements within that container.

1. **Measuring Depth:** The value of `perspective` is a length measurement, which represents the distance from the viewer to the elements. Common values are in pixels (e.g., `100px`) or any valid CSS length unit.

1. **Greater Values Create More Depth:** A larger `perspective` value results in a stronger 3D effect, making transformed elements appear further away from the viewer. Large values of perspective cause a small transformation; small values of perspective cause a large transformation.

1. **Only Affects Child Elements:** The `perspective` property doesn't change the perspective of the parent element itself; it affects the child elements within the container.

1. **Combined with `rotateX`, `rotateY`, and `rotateZ`:** To achieve 3D transformations, you often pair the `perspective` property with the `rotateX`, `rotateY`, and `rotateZ` functions to control how an element is transformed in 3D space.

1. **CSS backface-visibility**

- **Hidden Faces:** The `backface-visibility` property controls whether the backside (the side facing away from the viewer) of an element during 3D transformations is visible or hidden.

- **Applied to Child Elements:** It is applied to the child elements that are subject to 3D transformations, such as `rotateX`, `rotateY`, and `rotateZ`. It determines if the backside of these transformed elements should be visible or hidden.

- **Values:** It accepts two values:

  - `visible`: The backside of the element is visible during 3D transformations.
  - `hidden`: The backside of the element is hidden during 3D transformations.

- **Child Elements:** The `backface-visibility` property is applied to individual child elements and can be set differently for each element based on your design needs.

- **Combined with `perspective`:** It is often used in conjunction with the `perspective` property to create immersive 3D effects, such as card flips or spinning objects.

- **CSS Transforms:** To achieve 3D transformations and utilize `backface-visibility`, you typically combine it with CSS transform functions like `rotateX`, `rotateY`, and `rotateZ`.

11. Theory of positioned element

- When we give an element absolute position, what the elements do is that they basically start fitting to their width. This means if we don't explicitly specify width then they will only cover the width of their content.

- When we take the child elements of an element out of their natural flow (by float or by positioning(absolute)) then their parent's height tends to get collapsed. But in the case of float, we have clear-fix, but in positioning, we can't do much then also give the same height to their parent as the child.

12. **CSS Overflow:** The `overflow` property is used to control how content that overflows the bounds of an element is displayed.

- . **Values:** The property can be set to one of the following values:

  - `visible` (default): Content is not clipped, and it may overflow the element's box.
  - `hidden`: Overflowing content is clipped, and it's not visible.
  - `scroll`: A scrollbar is added to the element, allowing users to scroll and access the overflowing content.
  - `auto`: A scrollbar is added only if the content overflows the element.

- . **X and Y Axes:** The `overflow` property can be set separately for the horizontal (overflow-x) and vertical (overflow-y) axes.

  **Use Cases:** It's commonly used in elements with fixed dimensions (such as a container with a fixed height) to manage the display of overflowing content.

- **Scrollbars:** When using `overflow: auto` or `overflow: scroll`, scrollbars appear if the content overflows the element, allowing users to scroll through the content.

- **Hidden Overflow:** Setting `overflow: hidden` is useful for hiding content that exceeds the element's dimensions, which can be helpful in creating tooltips or dropdown menus.

- **Accessibility:** Be mindful when using `overflow: hidden` or `overflow: scroll` as it can hide content from users without clear indications of the hidden content.

- **Content Clipping:** `overflow: hidden` clips the content, making it inaccessible to users. Use this property with caution to ensure the content isn't vital for the user experience.

- **Inheritance:** The `overflow` property is not inherited from parent elements. It must be applied directly to the element you want to control.

13. **the CSS `background-blend-mode` property:**

- blend means "to mix"
- **Blend Backgrounds:** The `background-blend-mode` property is used to specify how multiple background images or colors should blend together within an element.

- **Values:** It accepts various blending modes that determine how the backgrounds interact with each other. Some common values include `normal`, `multiply`, `screen`, `overlay`, and `color-dodge`.

- **Applied to Backgrounds:** `background-blend-mode` is applied to the element's `background` property, and it affects the blending of background images and colors but doesn't apply to the content of the element.

- **Fallback Value:** If the specified blending mode is not supported by the browser, it will fall back to the `background-color` or the last specified background image.

- **Stacking Order:** The order of background layers (defined with `background-image`) and their corresponding blend modes affects the final result. The top layer is blended with the layers beneath it.

14. **The CSS `box-decoration-break` property:**

- **Multi-Line Elements:** The `box-decoration-break` property is used to control how the styles and decorations (such as backgrounds, borders, and padding) are applied to a multi-line block-level element, such as text with line breaks.

- **Values:** It accepts two values:

  - `slice` (default): The element's styles and decorations are applied to each line individually, creating a "sliced" appearance.
  - `clone`: The element's styles and decorations are applied as if the element were one continuous block, creating a "cloned" appearance across lines.

- **Usage:** This property is particularly useful for styling elements like headings and paragraphs when text content spans multiple lines.

- **`slice` Value:** When `box-decoration-break` is set to `slice`, each line of the element is styled individually, potentially leading to visual inconsistencies where styles, such as borders, don't carry across line breaks.

- **`clone` Value:** When set to `clone`, the element is treated as a single continuous block, and styles and decorations are consistent across line breaks.

- **Example Use Cases:** It can be applied to elements like headings, paragraphs, blockquotes, and other multi-line text elements to control how borders, backgrounds, and other styles span line breaks.

15. BEM (Block, Element, Modifier) and utility classes are two different approaches to naming and organizing CSS classes, each serving specific purposes in web development:

**1. BEM (Block, Element, Modifier):**

- **Purpose:** BEM is a naming convention designed to provide a structured and organized way to name CSS classes for components and elements in your web application.

- **Structure:** BEM divides class names into three categories:

  - **Block (B):** The highest-level component or container in the naming structure. Blocks are self-contained and encapsulate a piece of functionality or a specific part of the UI.
  - **Element (E):** Elements are the components or parts that make up a block. They are denoted by two underscores (`__`) after the block name.
  - **Modifier (M):** Modifiers are used to change the appearance or behavior of blocks or elements. They are denoted by two hyphens (`--`) and come after the block or element name. Modifiers help create variations of blocks and elements.

- **Benefits:** BEM helps create maintainable and scalable styles by providing a clear and consistent structure for class names. It encourages independent and isolated components and promotes self-explanatory class names.

**2. Utility Classes:**

- **Purpose:** Utility classes, also known as utility-first or atomic classes, are a different approach to CSS class naming. They involve creating small, single-purpose classes that directly apply specific styles to an element.

- **Structure:** Utility classes are typically named based on the specific style they provide. For example, you might have classes like `.text-center`, `.bg-primary`, or `.border-rounded`.

- **Benefits:** Utility classes offer flexibility and efficiency. They allow you to apply styles directly to elements without having to write custom CSS for every element. This can speed up development and make it easier to manage styles.

**Key Differences:**

- **Structure:** BEM provides a structured and hierarchical approach to class naming, focusing on components and elements, whereas utility classes are more direct and serve specific styling purposes.

- **Isolation:** BEM promotes independent and isolated components and discourages reliance on parent elements. Utility classes can be used to apply styles directly to elements but may not encourage isolation.

- **Maintainability:** BEM offers maintainability through structured class names that are self-explanatory. Utility classes can lead to shorter HTML, but it may be less clear what styles are being applied.

- **Scalability:** BEM is well-suited for large projects where components are reused and consistency is essential. Utility classes are useful for quickly styling elements but may lead to a proliferation of classes in the HTML.

Both BEM and utility classes have their strengths, and the choice between them depends on the specific needs of a project. Some projects may even use a combination of both approaches to address different styling requirements.

16. Centering an element inside a parent container

**1. Cenetr horizontally**
-To centre an element horizontally inside a parent container::-

```css
.block__element {
  width: some-value;
  margin: 0 auto;
}
```

**2. Center both Horizontally and Vertically**

- But to centre an element both horizontally and vertically use positioning, also set the position on the parent element to relative::-

```css
.block__element {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

17. **1. shape-outside:**

- The shape outside, all it does is to define where the content floats around the element in this case, a circle, and if we actually want the element to look like that circle, we can then use the clip-path property

- To use the shape-outside property on an element, first, you have to define the element's dimensions (height and width) and then float the element.
  secondly: the shape-outside property doesn't give shape to your element, to give shape to your element like a circle, ellipse etc. you still have to use clip-path property, and the shape-outside property only wraps the content around your floated element.
- use transform: translate(some value) to add gap between the shaped element and wrapped content, if you use padding and margin then it will mess up with the shape-outside property.

**2. HTML <figure> </figure> element**,

- The <figure> HTML element represents self-contained content, potentially with an optional caption, which is specified using the <figcaption> element. The figure, its caption, and its contents are referenced as a single unit.

**3. HTML <video> </video> element**,

- The <video> HTML element embeds a media player which supports video playback into the document. You can use <video> for audio content as well, but the <audio> element may provide a more appropriate user experience.

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/HTML%20video.png)

- autoplay to auto start video on when page loaded, muted to mute the sound of the video, loop is used to loop the video again and again
- two <source> is used of different video format, because there are some broweser that do not support mp4 and there are some that do not support webm
  **4. CSS filter property**
- The filter CSS property applies graphical effects like blur or color shift to an element. Filters are commonly used to adjust the rendering of images, backgrounds, and borders.

**5. CSS object-fit**

- The object-fit CSS property sets how the content of a replaced element, such as an <img> or <video>, should be resized to fit its container.

- You can alter the alignment of the replaced element's content object within the element's box using the object-position property.
- it is similar to background-size: cover ; property but background-size property only works with background-img, and object-fit works with HTML elements like video, img

18. Solid color gradient

```css
background-image: linear-gradient(
    105deg,
    rgba(white, 0.9) 0%,
    rgba(white, 0.9) 50%,
    (transparent 50.1%)
  ), url(../img/nat-10.jpg);
```

The provided CSS code sets the `background-image` property of an element, creating a background with a linear gradient and an image. Here's a breakdown:

1. **Linear Gradient Background**:

   - `linear-gradient(105deg, rgba(white, 0.9) 0%, rgba(white, 0.9) 50%, transparent 50.1%)`: This defines a linear gradient background.
   - `105deg`: Specifies the angle of the gradient, which is set to 105 degrees, creating a gradient that slants at a 105-degree angle from the horizontal (counter-clockwise).
   - `rgba(white, 0.9) 0%`: At the start (0%), the gradient begins with a semi-transparent white color with an opacity of 0.9. Note that it seems to use `white` as a color variable, which would need to be defined somewhere in your CSS or preprocessor like Sass.
   - `rgba(white, 0.9) 50%`: At the halfway point (50%), the gradient maintains the same semi-transparent white color.
   - `transparent 50.1%`: Slightly after 50%, the gradient becomes fully transparent. This creates a smooth transition from the semi-transparent white to transparency.

2. **Image Background**:
   - `url(../img/nat-10.jpg)`: This part of the `background-image` property specifies a URL to an image file (`nat-10.jpg`) to be used as the background. It uses the `url()` function to reference the image file.

So, with this CSS, the element's background will have a linear gradient that starts with a semi-transparent white color at a 105-degree angle and gradually transitions to transparency. This gradient effect is then overlaid with the image located at the specified URL. The result is a background that combines a gradient with an image.

19. Transparent is a color, that is created in the absence of all the other colors.

::-webkit-input-placeholder

- Use it to style the placeholder inside the input element.

CSS :placeholder-shown property

- The :placeholder-shown CSS pseudo-class represents any <input> or <textarea> element that is currently displaying placeholder text. We can use it for example to style the label of the input element when the placeholder is still present in the input box(until the user hasn't started typing yet).

input (:invalid) state

- We can add styling to our form input element when they are invalid with the help of (:invalid) state

Next-sibling combinator(+)

- The next-sibling combinator (+) separates two selectors and matches the second element only if it immediately follows the first element, and both are children of the same parent element.

- in the Next-sibling selector(+), the element that we want to target should be immediately after the first selected element otherwise (if there are other elements in between them ) then use the general sibling selector(~)

Subsequent-sibling combinator(~)

- The subsequent-sibling combinator (~) separates two selectors and matches all instances of the second element that follow the first element (not necessarily immediately) and share the same parent element.

- form input elements don't inherit font, color styling etc, so we have to explicitly inherit them.

- Now one particular thing about the sibling selector is that the sibling that we have to select always has to be after the first element.

- Now the focus state styling on inputs is actually essential for people who use a webpage without a mouse, but only with a keyboard, and so when they move around with a keyboard on the webpage, they need to know which form elements are actually focused. So for accessibility reasons, we should never just do input focus, and then set the outline to none and call it a day. So we should always make the form elements that are focused visible.

20. We can't style radio buttons or checkboxes through the CSS if we want to style the radio button or checkbox then we have to make our own radio button/checkbox.

21. We can't use anchor tags as a button to submit the form, To submit a form we have to use the actual button element.

22. The `display: table;` and `display: table-cell;` properties in CSS are used to create layouts that mimic the behavior of HTML tables without using actual `<table>` elements. They are part of the CSS display property values that allow you to control the layout and formatting of elements on a web page.

23. **`display: table;`**:
    - When applied to an element, it makes that element act as a table element.
    - The element becomes a block-level container, and its direct children become table-row elements.
    - These children can further have child elements styled as table-cell elements.
    - It is useful for creating grid-like structures where you need to control the alignment and layout of elements.

Example:

```css
.table {
  display: table;
}
.row {
  display: table-row;
}
.cell {
  display: table-cell;
}
```

```html
<div class="table">
  <div class="row">
    <div class="cell">Cell 1</div>
    <div class="cell">Cell 2</div>
  </div>
</div>
```

2. **`display: table-cell;`**:
   - When applied to an element, it makes that element act as a table cell.
   - Table cells can be used within table structures created using `display: table;` and `display: table-row;`.
   - It allows you to style individual cells in a table-like layout, controlling their alignment, background, borders, and other CSS properties.

These properties are useful for creating complex layouts when you want to control the positioning and alignment of elements without using traditional HTML tables. They are particularly handy when you need to create responsive, grid-based designs in CSS, and you want to take advantage of the flexibility of CSS while still achieving table-like layouts.

24. column-count: 2;

- The column-count CSS property breaks an element's content into the specified number of columns.

25. column-gap: 4rem;

    - The column-gap CSS property sets the size of the gap (gutter) between an element's columns.

26. column-rule: 1px solid variables.$color-grey-light-2;

    - The column-rule shorthand CSS property sets the width, style, and color of the line drawn between columns in a multi-column layout.

27. hyphens: auto;

- The hyphens CSS property specifies how words should be hyphenated when text wraps across multiple lines. It can prevent hyphenation entirely, hyphenate at manually-specified points within the text, or let the browser automatically insert hyphens where appropriate.

![App Screenshot](https://raw.githubusercontent.com/Ajaydwivedi2/Advance-css/master/column-count.png)
