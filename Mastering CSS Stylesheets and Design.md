# Mastering CSS Stylesheets and Design
## **1. Introduction to CSS**
- **1.1 What is CSS?**
- **1.2 How CSS Works with HTML**
- **1.3 CSS Syntax**
- **1.4 Including CSS in HTML**
  - Inline Styles
  - Internal Stylesheets
  - External Stylesheets
  - @import Rule

---

## **2. Basic Selectors**
- **2.1 Type Selectors**
- **2.2 Class Selectors**
- **2.3 ID Selectors**
- **2.4 Universal Selector**
- **2.5 Grouping Selectors**
- **2.6 Combinator Selectors**
  - Descendant Selector
  - Child Selector
  - Adjacent Sibling Selector
  - General Sibling Selector

---

## **3. CSS Specificity and Inheritance**
- **3.1 Understanding Specificity**
- **3.2 The Cascade and Order of Precedence**
- **3.3 Inheritance in CSS**
- **3.4 The `!important` Declaration**

---

## **4. Basic Styling**
- **4.1 Colors and Backgrounds**
  - Color Names, Hex Codes, RGB, RGBA, HSL, HSLA
  - Background Colors
  - Background Images
  - Background Positioning and Repeating
  - CSS Gradients
- **4.2 Text Styling**
  - Font Families
  - Font Sizes and Units
  - Font Weights and Styles
  - Text Alignment and Justification
  - Text Decoration and Transformation
  - Line Height and Letter Spacing
- **4.3 List Styles**
  - Unordered and Ordered Lists
  - Custom List Markers
- **4.4 Link Styling**
  - Default Link Styles
  - Hover, Active, and Visited States
  - Removing Underlines and Adding Effects

---

## **5. The CSS Box Model**
- **5.1 Content Area**
- **5.2 Padding**
- **5.3 Borders**
  - Border Styles, Widths, and Colors
  - Border Radius for Rounded Corners
- **5.4 Margin**
- **5.5 Box Sizing (`content-box` vs `border-box`)**
- **5.6 Outline Property**

---

## **6. Layout Basics**
- **6.1 The `display` Property**
  - Block, Inline, Inline-Block
  - None, Visibility Hidden
- **6.2 Positioning Elements**
  - Static Positioning
  - Relative Positioning
  - Absolute Positioning
  - Fixed Positioning
  - Sticky Positioning
  - The `z-index` Property
- **6.3 Floating Elements**
  - Using Floats
  - Clearing Floats
  - The Clearfix Hack
- **6.4 Overflow and Clipping Content**

---

## **7. Advanced Selectors**
- **7.1 Attribute Selectors**
  - Presence and Value Selectors
  - Substring Matching Selectors
- **7.2 Pseudo-Classes**
  - Structural Pseudo-Classes (`:first-child`, `:nth-child()`, etc.)
  - UI Element States (`:enabled`, `:disabled`, `:checked`)
  - Negation Pseudo-Class (`:not()`)
- **7.3 Pseudo-Elements**
  - `::before` and `::after`
  - `::first-letter` and `::first-line`
  - `::selection`

---

## **8. Responsive Web Design**
- **8.1 Introduction to Responsive Design**
- **8.2 Viewport Meta Tag**
- **8.3 Media Queries**
  - Syntax and Usage
  - Breakpoints and Responsive Design Strategies
- **8.4 Responsive Units**
  - Percentages
  - `em`, `rem`
  - Viewport Units (`vw`, `vh`, `vmin`, `vmax`)
- **8.5 Responsive Images**
  - Using `srcset` and `sizes`
  - Picture Element

---

## **9. CSS Flexbox Layout**
- **9.1 Introduction to Flexbox**
- **9.2 Flex Container Properties**
  - `display: flex` and `display: inline-flex`
  - `flex-direction`
  - `flex-wrap`
  - `flex-flow`
  - `justify-content`
  - `align-items`
  - `align-content`
- **9.3 Flex Item Properties**
  - `order`
  - `flex-grow`
  - `flex-shrink`
  - `flex-basis`
  - `flex`
  - `align-self`
- **9.4 Practical Flexbox Layouts**

---

## **10. CSS Grid Layout**
- **10.1 Introduction to CSS Grid**
- **10.2 Grid Container Properties**
  - `display: grid` and `display: inline-grid`
  - Defining Columns and Rows (`grid-template-columns`, `grid-template-rows`)
  - Grid Lines and Tracks
  - Grid Gaps (`grid-gap`, `row-gap`, `column-gap`)
  - Grid Template Areas
  - Implicit vs. Explicit Grids
  - Alignment (`justify-items`, `align-items`, `place-items`)
- **10.3 Grid Item Properties**
  - Placing Items (`grid-column`, `grid-row`)
  - Spanning Items Across Tracks
  - Layering Grid Items
  - Item Alignment (`justify-self`, `align-self`, `place-self`)
- **10.4 Advanced Grid Techniques**
  - Named Grid Lines
  - The `minmax()` Function
  - Auto-Fit and Auto-Fill
  - Responsive Grids with Media Queries

---

## **11. CSS Transitions and Animations**
- **11.1 CSS Transitions**
  - Transition Properties (`transition-property`, `transition-duration`, etc.)
  - Timing Functions (`ease`, `linear`, `ease-in-out`)
  - Transition Delays
- **11.2 CSS Animations**
  - Defining Animations with `@keyframes`
  - Animation Properties (`animation-name`, `animation-duration`, etc.)
  - Iteration Counts and Direction
  - Animation Fill Modes
  - Chaining and Sequencing Animations

---

## **12. CSS Transforms**
- **12.1 2D Transforms**
  - Translation (`translateX()`, `translateY()`)
  - Rotation (`rotate()`)
  - Scaling (`scale()`)
  - Skewing (`skewX()`, `skewY()`)
  - Transform Origin
- **12.2 3D Transforms**
  - 3D Translation and Rotation
  - Perspective and Transform Style
- **12.3 Combining Transforms**

---

## **13. Advanced Styling Techniques**
- **13.1 Shadows and Glows**
  - Box Shadows
  - Text Shadows
- **13.2 Advanced Backgrounds**
  - Multiple Backgrounds
  - Background Blend Modes
- **13.3 Gradients**
  - Linear Gradients
  - Radial Gradients
  - Conic Gradients
  - Repeating Gradients
- **13.4 Filters**
  - Applying Filters (`blur()`, `brightness()`, `contrast()`, etc.)
  - Backdrop Filters

---

## **14. CSS Variables (Custom Properties)**
- **14.1 Defining and Using Variables**
- **14.2 Variable Scope**
- **14.3 Variable Fallbacks**
- **14.4 Dynamic Updates with JavaScript**

---

## **15. CSS Functions and Calculations**
- **15.1 The `calc()` Function**
- **15.2 The `min()`, `max()`, and `clamp()` Functions**
- **15.3 Trigonometric Functions**
- **15.4 Practical Uses in Layouts**

---

## **16. Advanced Responsive Design**
- **16.1 Responsive Typography**
  - Fluid Type with `calc()` and Viewport Units
- **16.2 CSS Grid and Flexbox in Responsive Design**
  - Creating Adaptive Layouts
- **16.3 Responsive Navigation Menus**
  - Hamburger Menus
  - Dropdowns and Mega Menus
- **16.4 Responsive Tables and Data Visualization**

---

## **17. Accessibility in CSS**
- **17.1 Understanding Web Accessibility**
- **17.2 Accessible Color Contrast**
- **17.3 Focus States and Keyboard Navigation**
- **17.4 Screen Reader Friendly CSS**
- **17.5 Using ARIA Attributes**

---

## **18. CSS Preprocessors**
- **18.1 Introduction to Preprocessors**
  - Advantages and Use Cases
- **18.2 SASS (Syntactically Awesome Style Sheets)**
  - Variables and Nesting
  - Mixins and Functions
  - Extends and Inheritance
  - Control Directives and Expressions
- **18.3 LESS (Leaner Style Sheets)**
  - Variables and Mixins
  - Operations and Functions
- **18.4 Stylus**
- **18.5 Setting Up a Preprocessor Workflow**

---

## **19. CSS Methodologies and Architecture**
- **19.1 BEM (Block Element Modifier)**
- **19.2 OOCSS (Object-Oriented CSS)**
- **19.3 SMACSS (Scalable and Modular Architecture for CSS)**
- **19.4 ITCSS (Inverted Triangle CSS)**
- **19.5 Choosing the Right Methodology**

---

## **20. Advanced CSS Features**
- **20.1 CSS Shapes**
  - Wrapping Content Around Shapes
- **20.2 Clipping and Masking**
  - The `clip-path` Property
  - SVG Masks and Clip Paths
- **20.3 CSS Custom Fonts and Font Loading**
  - Using `@font-face`
  - Font Formats and Performance
- **20.4 Variable Fonts**
  - Understanding Variable Fonts
  - Implementing Variable Font Axes

---

## **21. CSS Frameworks**
- **21.1 Introduction to Frameworks**
  - Benefits and Drawbacks
- **21.2 Bootstrap**
  - Grid System
  - Components and Utilities
- **21.3 Tailwind CSS**
  - Utility-First CSS
  - Customization and Theming
- **21.4 Materialize CSS**
- **21.5 Bulma**
- **21.6 Using Frameworks vs. Writing Custom CSS**

---

## **22. Modern CSS Workflow**
- **22.1 CSS Resets and Normalization**
- **22.2 PostCSS and Autoprefixer**
- **22.3 Linting CSS with Stylelint**
- **22.4 CSS Modules**
- **22.5 CSS-in-JS**
  - Styled-Components
  - Emotion
- **22.6 Integrating CSS with Build Tools**
  - Webpack
  - Parcel
  - Gulp

---

## **23. Performance Optimization**
- **23.1 Critical CSS and Above-the-Fold Content**
- **23.2 Minimizing Repaints and Reflows**
- **23.3 CSS Minification and Compression**
- **23.4 Content Delivery Networks (CDNs)**
- **23.5 Browser Rendering and the Paint Process**
- **23.6 Efficient Use of Selectors**

---

## **24. Browser Compatibility and Feature Detection**
- **24.1 Vendor Prefixes**
  - When and How to Use Them
- **24.2 The `@supports` Rule**
  - Feature Queries
- **24.3 Polyfills and Graceful Degradation**
- **24.4 Tools for Testing and Debugging**
  - Can I Use
  - Browser DevTools

---

## **25. The Future of CSS**
- **25.1 Upcoming CSS Features**
  - Subgrid in CSS Grid
  - Container Queries
  - CSS Houdini and the Extensible Web
  - New Pseudo-Classes and Elements
- **25.2 Staying Updated with CSS Specifications**
- **25.3 Experimental Features and Flags**

---

## **26. Best Practices and Professional Tips**
- **26.1 Organizing CSS Code**
  - File Structure and Naming Conventions
- **26.2 Commenting and Documentation**
- **26.3 CSS Debugging Techniques**
  - Common Issues and Solutions
- **26.4 Writing Maintainable and Scalable CSS**
- **26.5 Naming Conventions and Style Guides**

---

## **27. Projects and Case Studies**
- **27.1 Building a Responsive Layout from Scratch**
- **27.2 Creating Interactive Elements with CSS**
- **27.3 Designing Complex Grid and Flexbox Layouts**
- **27.4 Styling Forms and Inputs**
- **27.5 Implementing Dark Mode with CSS**

---

## **28. Resources and Further Learning**
- **28.1 Recommended Books and Tutorials**
- **28.2 Online Courses and Workshops**
- **28.3 CSS Specifications and Documentation**
  - MDN Web Docs
  - W3C CSS Specifications
- **28.4 Community and Support**
  - Forums and Discussion Groups
  - Blogs and Newsletters
- **28.5 Practice Projects and Challenges**
  - CodePen
  - CSSBattle

#software/webdev/css