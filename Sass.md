Useful Info For SASS
======
  
Index  
[Compiling_From_CSS](#Compiling_From_CSS)  
[Breaking_Up_Files](#Breaking_Up_Files)  
[Nesting](#Nesting)  
[Variables](#Variables)  
[Functions](#Functions)  
[Responsive_Design](#Responsive_Design)  
  
  
  
Compiling_From_CSS
------  
##### Compiling can be done several ways these are:  
* **VS Code Extension `SASS Compiler` just create the .scss file and click watch at the bottom of the VS Code window to begin compiling.**    
* **Run `npm install sass --save` then create the .scss file and then use the following terminal command (assuming main.scss was the filename used for the scss file) STILL LINK THE .CSS FILE IN THE HTML FILE THE COMPILER TAKES CARE OF THE .SCSS:**  
```
sass main.scss main.css --watch
```  
* **Run `npm install node-sass --save` then add the following script (sass/main.scss are the directory/filename) to the `package.JSON` file (the -w tells the script to keep watch to autoupdate on save) STILL LINK THE .CSS FILE IN THE HTML FILE THE COMPILER TAKES CARE OF THE .SCSS:**  
```
"scripts": {
  "compile:sass": "node-sass sass/main.scss css/style.css -w"
}, 
```
  **Then run the following command from the terminal to initialise the script:**  
```
compile:sass
```  
  
[Index](#Index)  
  
  
Breaking_Up_Files
------
* **Files can be broken up to make organising the SASS file much easier. To simplify this and make it universal we use the 7-1 Pattern. We have *7 different Folders for Partial SASS Files* and *1 Main SASS File* to *Import* all the other Files into. These folders are as follows:**
  1. **Base/** *Basic Pproduct definitions*  
  2. **Components/** *One file for each component*    
  3. **Layout/** *Define the layout of the project*  
  4. **Pages/** *Styles for specific pages*  
  5. **Themes/** *To implement different themse*  
  6. **Abstract/** *Files that don't output CSS such as variables and mixins*  
  7. **Vendors/** *3rd party CSS*
* **Every new file we create must begin with an _(underscore) for example: `_functions.scss`  
* **For each file we create we have to import it into out main.scss file like this:**  
```
@import "abstracts/functions";
@import "abstracts/mixins";
@import "abstracts/variables";

@import "base/animations";
@import "base/base";
@import "base/typography";
@import "base/utilities";

@import "components/button";
@import "components/composition";

@import "layout/grid";
@import "layout/header";

@import "pages/home";
```  
  
[Index](#Index) 
  
Nesting
------  
* **Nesting is a great feature of SASS that allows you to nest selectors under parents by using the `&` operator. For example:**  
```
.composition {
  position: relative;

  &__photo {
    width: 55%;
    box-shadow: 0 1.5rem 4rem rgba($color-black, .4);
    border-radius: 2px;
    position: absolute;
    z-index: 10;
    transition: all .2s;
    outline-offset: 2rem;

    &--p1 {
      left: 0;
      top: -2rem;
    }

    &--p2 {
      right: 0;
      top: 2rem;
    }

    &--p3 {
      left: 20%;
      top: 10rem;
    }

    &:hover {
      outline: 1.5rem solid $color-primary;
      transform: scale(1.05) translateY(-.5rem);
      box-shadow: 0 2.5rem 4rem rgba($color-black, .5);
      z-index: 20;
    }
  }
  &:hover &__photo:not(:hover) {
    transform: scale(.95);
  }
}
```
  
[Index](#Index)  
  
Variables
------
* **Variables are handy for values that will be used repeatably such as colours. Example:**  
```
// COLOURS
$color-primary: #55c57a;
$color-primary-light: #7ed56f;
$color-primary-dark: #28b485;

$color-grey-light-1: #f7f7f7;

$color-grey-dark: #777;
$color-white: #fff;
$color-black: #000;

//FONT
$default-font-size: 1.6rem;

// GRID
$grid-width: 114rem;
$gutter-vertical: 8rem;
$gutter-horizontal: 6rem;
```
  **Variables are called by simply using `$variable-name` in place of the value.**

  
[Index](#Index) 
  
Functions
------  
  
#### Function for Media Queries  
  
```
@mixin respond($breakpoint)
{
  @if $breakpoint == phone{
    @media (max-width: 37.5em) { @content};    
  }
  @if $breakpoint == tab-port{
    @media (max-width: 56.25em) { @content};
  }
  @if $breakpoint == tab-land{
    @media (max-width: 75em) { @content};
  }
  @if $breakpoint == big-desktop{
    @media (min-width: 112.5em) { @content};
  }
}
```    
  
[Index](#Index)
  
Responsive_Design
------
* **It is important to design web pages and apps with reponsiveness in mind. This means that the page or app will display correctly on screens of any size. To achieve this we can use media queries. Here is a list of different screen sizes that media queries can be set to so that responsiveness can be achieved.**  
  
* **Bootstrap sizes in px:**  
```
X-S   Less than 768   768 max-width  
S     768 and up      768 min-width  
M     992 and up      992 min-width  
L     1200 and up     1200 min-width  
```  
* **Other sizes to consider:**  
```
375 X 667   - Mobile
1360 X 768  - Laptop
1920 X 1080 - Large Desktop
```  
* **OR:**  
```
max-width - 600px
maxwidth  - 1000px
```
* **OR:**
```
420px max-width
768px max-width
1200px max-width
```
* **OR:**
```
@media all and (max-width: 1690px){.....}
@media all and (max-width: 1280px){.....}
@media all and (max-width: 980px){.....}
@media all and (max-width: 736px){.....}
@media all and (max-width: 480px){.....}
```  
* **There is no exact size that is the standard it is generally best to experiment and decide where you will place your break points**  
  
[Index](#Index)
