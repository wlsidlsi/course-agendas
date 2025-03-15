**I. Introduction to SCSS**

*   Understanding CSS Preprocessors
    *   Define preprocessors and their role in CSS development.
    *   Benefits: Maintainability, reusability, and organization.
*   Setting up SCSS Environment
    *   Installing a compiler (e.g., `dart-sass`).
        *   `npm install -g sass`
    *   Configuring build process.
        *   Using command-line tools.
        *   Integrating with task runners (e.g., Gulp, Webpack).
*   SCSS vs. CSS Syntax
    *   Similarities and differences.
    *   Basic SCSS file structure.

**II. SCSS Variables**

*   Declaring and Using Variables
    *   `$primary-color: #007bff;`
    *   Referencing variables in CSS properties.
        *   `color: $primary-color;`
*   Variable Scope
    *   Global vs. local variables.
    *   Understanding variable shadowing.
*   Data Types
    *   Numbers, strings, colors, booleans, nulls, lists, and maps.
    *   Example: `$font-size: 16px;` , `$font-family: Arial, sans-serif;`

**III. SCSS Nesting**

*   Basic Nesting of CSS Rules
    *   Nesting selectors for improved readability.
    *   Example:
        ```scss
        nav {
          ul {
            margin: 0;
            padding: 0;
            list-style: none;

            li {
              display: inline-block;
            }
          }
        }
        ```
*   Nesting with Pseudo-classes and Pseudo-elements
    *   Using `&:hover`, `&:active`, `&::before`, `&::after`.
    *   Example:
        ```scss
        a {
          color: blue;
          &:hover {
            color: darkblue;
          }
        }
        ```
*   The Parent Selector (&)
    *   Referencing the parent selector in complex scenarios.
    *   Example:
        ```scss
        .button {
          &-primary {
            background-color: blue;
            &:hover {
              background-color: darkblue;
            }
          }
        }
        ```

**IV. SCSS Mixins**

*   Defining Mixins
    *   Using the `@mixin` directive.
    *   Example:
        ```scss
        @mixin border-radius($radius) {
          border-radius: $radius;
          -webkit-border-radius: $radius;
          -moz-border-radius: $radius;
        }
        ```
*   Including Mixins
    *   Using the `@include` directive.
    *   Example:
        ```scss
        .box {
          @include border-radius(5px);
        }
        ```
*   Mixins with Arguments
    *   Passing arguments to mixins for customization.
    *   Example:
        ```scss
        @mixin box-shadow($x, $y, $blur, $color) {
          box-shadow: $x $y $blur $color;
        }

        .element {
          @include box-shadow(2px, 2px, 5px, rgba(0, 0, 0, 0.3));
        }
        ```
*   Advanced Mixin Techniques
    *   Using default values for arguments.
    *   Using content blocks with `@content`.

**V. SCSS Functions**

*   Defining Functions
    *   Using the `@function` directive.
    *   Example:
        ```scss
        @function double($number) {
          @return $number * 2;
        }
        ```
*   Using Functions
    *   Calling functions within SCSS expressions.
    *   Example: `width: double(10px);`
*   Built-in Functions
    *   Color manipulation functions (e.g., `lighten`, `darken`, `saturate`).
        *   `background-color: lighten(#007bff, 20%);`
    *   Math functions (e.g., `round`, `ceil`, `floor`, `percentage`).
    *   String functions (e.g., `quote`, `unquote`).

**VI. SCSS @extend (Inheritance)**

*   Basic Usage of `@extend`
    *   Inheriting CSS properties from another selector.
    *   Example:
        ```scss
        .message {
          border: 1px solid #ccc;
          padding: 10px;
          color: #333;
        }

        .success-message {
          @extend .message;
          border-color: green;
          color: green;
        }
        ```
*   Extending with Placeholders (`%`)
    *   Creating reusable styles without generating CSS for the placeholder itself.
    *   Example:
        ```scss
        %message-shared {
          border: 1px solid #ccc;
          padding: 10px;
        }

        .message {
          @extend %message-shared;
        }

        .success-message {
          @extend %message-shared;
          border-color: green;
        }
        ```
*   Differences Between `@extend` and Mixins
    *   Understanding when to use `@extend` vs. when to use mixins.
    *   `@extend` for sharing base styles; Mixins for generating dynamic or parameterized styles.

**VII. SCSS Modules and Partials**

*   Creating Partials
    *   Naming convention: `_filename.scss`.
    *   Purpose: Splitting SCSS code into manageable files.
*   Importing Partials
    *   Using the `@import` directive.
        *   `@import 'variables';`
        *   `@import 'mixins';`
*   Organizing SCSS Project Structure
    *   Example:
        ```
        /scss
          /_variables.scss
          /_mixins.scss
          /_base.scss
          /_layout.scss
          /_components.scss
          /style.scss
        ```
*   Using `!default` Flag
    *   Allowing variables to be overridden by the user.
    *   Example: `$primary-color: #007bff !default;`

**VIII. SCSS Operators**

*   Arithmetic Operators
    *   `+`, `-`, `*`, `/`, `%`.
    *   Example: `$width: 100px + 50px;`
*   Relational Operators
    *   `>`, `<`, `>=`, `<=`, `==`, `!=`.
    *   Example (within mixin logic): `@if $width > 100px { ... }`
*   Logical Operators
    *   `and`, `or`, `not`.
    *   Example (within mixin logic): `@if $width > 100px and $color == blue { ... }`
*   Color Operations
    *   Adding, subtracting, multiplying, and dividing colors.
    *   Example: `background-color: #007bff + #001f3f;`

**IX. Control Directives**

*   `@if` / `@else` Statements
    *   Conditional styling based on variables or expressions.
    *   Example:
        ```scss
        @if $theme == 'dark' {
          background-color: #333;
          color: #fff;
        } @else {
          background-color: #fff;
          color: #333;
        }
        ```
*   `@for` Loops
    *   Iterating over a range of numbers.
    *   Example:
        ```scss
        @for $i from 1 through 3 {
          .col-#{$i} {
            width: 100% / $i;
          }
        }
        ```
*   `@each` Loops
    *   Iterating over lists or maps.
    *   Example:
        ```scss
        $social-icons: (
          twitter: blue,
          facebook: darkblue,
          instagram: purple
        );

        @each $name, $color in $social-icons {
          .icon-#{$name} {
            background-color: $color;
          }
        }
        ```
*   `@while` Loops
    *   Looping while a condition is true.

**X. Advanced SCSS Techniques**

*   Creating Custom Functions for Complex Calculations
    *   Example: Calculating aspect ratios.
*   Using Maps for Configuration
    *   Storing related values in a map.
    *   Example:
        ```scss
        $theme-colors: (
          'primary': #007bff,
          'secondary': #6c757d,
          'success': #28a745
        );

        @function theme-color($key) {
          @return map-get($theme-colors, $key);
        }

        .btn-primary {
          background-color: theme-color('primary');
        }
        ```
*   Implementing Responsive Design with SCSS
    *   Using mixins for media queries.
    *   Example:
        ```scss
        @mixin respond-to($breakpoint) {
          @if $breakpoint == small {
            @media (max-width: 576px) { @content; }
          } @else if $breakpoint == medium {
            @media (min-width: 577px) and (max-width: 768px) { @content; }
          } @else if $breakpoint == large {
            @media (min-width: 769px) and (max-width: 992px) { @content; }
          } @else if $breakpoint == extra-large {
            @media (min-width: 993px) { @content; }
          }
        }

        .container {
          width: 100%;

          @include respond-to(medium) {
            width: 750px;
          }
        }
        ```

**XI. Best Practices and Optimization**

*   Writing Clean and Maintainable SCSS
    *   Following a consistent coding style.
    *   Commenting your code.
*   Avoiding Over-Nesting
    *   Balancing readability with performance.
*   Optimizing SCSS for Production
    *   Minifying CSS.
    *   Using Autoprefixer for vendor prefixes.
*   Using Linters and Style Guides
    *   Tools like Stylelint to enforce coding standards.
*   Performance considerations
    *   Keeping the compiled CSS file size small.
    *   Avoiding overly complex selectors.
