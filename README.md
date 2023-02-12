# carousel

HTML + CSS + JS carousel

## Usage

In your HTML file, link the CSS and JS files:

```html
<link rel="stylesheet" href="carousel.css">
<script src="carousel.js"></script>
```

Then, add the following HTML code:

```html
<div class="carousel">
    <button id="left" class="carousel-button"> <!-- You can customize buttons with your own SVG -->
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <path
                d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l160 160c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.2 288 416 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-306.7 0L214.6 118.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-160 160z" />
        </svg>
    </button>
    <div class="carousel-container">
        <div id="carousel" class="carousel-main slide-effect"> <!-- Change slide-effect to fade-effect to use fade effect -->
            <div class="carousel-item">Item 1</div>
            <div class="carousel-item">Item 2</div>
            <div class="carousel-item">Item 3</div>
            <div class="carousel-item">Item 4</div>
            <div class="carousel-item">Item 5</div>
            <div class="carousel-item">Item 6</div>
        </div>
        <div id="carousel-nav" class="carousel-nav"></div>
    </div>
    <button id="right" class="carousel-button"> <!-- You can customize buttons with your own SVG -->
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <path
                d="M438.6 278.6c12.5-12.5 12.5-32.8 0-45.3l-160-160c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L338.8 224 32 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l306.7 0L233.4 393.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l160-160z" />
        </svg>
    </button>
</div>
```

__Note:__ Ids can be changed, but the class names must be the same to work with the CSS and JS files.
__Note:__ If you don't want a navigation, remove the div with id "carousel-nav" and the parameter "carousel-nav" in the constructor.
__Note:__ If you don't want a left button, remove the button with id "left" and the parameter "left" in the constructor.
__Note:__ If you don't want a right button, remove the button with id "right" and the parameter "right" in the constructor.

The carousel.js defines a class called Carousel. You can create a new carousel by calling the constructor:

```js
new Carousel("carousel", "carousel-item", "carousel-nav", "left", "right", true, 5000, true, true);
```

The constructor takes 9 parameters:

1. The id of the carousel container
2. The class name of the carousel items
3. The id of the carousel navigation (optional, put null or false if you don't want a navigation)
4. The id of the left button (optional, put null or false if you don't want a left button)
5. The id of the right button (optional, put null or false if you don't want a right button)
6. Auto slide (optional, default is true)
7. Auto slide interval (optional, default is 5000ms)
8. Loop (optional, default is true)
9. Mobile swipe (optional, default is true)

## Effects

There are two effects: slide and fade. To use the slide effect, add the class "slide-effect" to the div with the "carousel-main" class. To use the fade effect, add the class "fade-effect" to the div with the "carousel-main" class.
