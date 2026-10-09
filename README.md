# Website Theming with Bootstrap, CSS, Sass, and Drupal

## Beginner-to-Intermediate Course Curriculum

Course Title: Introduction to Website Theming and Development Skill Level: Beginner to Intermediate Recommended Duration: 12 lessons, approximately 60–90 minutes each Primary Technologies: HTML5, CSS3, Bootstrap 5, Sass (SCSS), JavaScript, GitHub, Drupal, and Twig

## Course Overview

This course introduces students to website development and theming, beginning with fundamental HTML and progressing through CSS, Bootstrap customization, responsive design, Sass, and Drupal theme development.

Students will build and customize a website throughout the course, applying new concepts during each lesson. By the end, students will understand how to create a visually consistent website, customize Bootstrap components, and apply those same techniques to a Drupal-based website.

### Learning Objectives

Upon completing this course, students will be able to:

1. Understand the basic structure of an HTML website.
2. Create and maintain a static website using GitHub.
3. Apply CSS to customize colors, fonts, spacing, and layouts.
4. Understand and use Bootstrap components and utilities.
5. Customize Bootstrap styling without modifying its core files.
6. Understand basic Sass concepts, including variables and nesting.
7. Create responsive websites that adapt to different screen sizes.
8. Understand how Drupal generates HTML using themes and Twig templates.
9. Create and customize a Bootstrap-based Drupal theme.
10. Apply consistent branding across both static and Drupal websites.

# Part 1: Introduction to Static Website Development

## Lesson 1: Introduction to HTML, Bootstrap, and GitHub

Status: Completed — October 8, 2026

### Topics Covered

- What is a website?
- Understanding HTML and its purpose.
- Introduction to Bootstrap and frontend frameworks.
- Understanding HTML elements, tags, and attributes.
- Basic structure of an HTML document.
- Introduction to GitHub repositories.
- Hosting a static website using GitHub Pages.
- Including Bootstrap CSS and JavaScript.
- Introduction to Bootstrap components.
- Implementing a Bootstrap carousel.

### Hands-On Exercise

Exercise: Create Your First Website

Students will:

1. Create a simple `index.html` file.
2. Include Bootstrap using a CDN.
3. Add a heading and a paragraph introducing themselves.
4. Add a Bootstrap carousel containing three images.
5. Commit the changes to GitHub.
6. View their website using GitHub Pages.

Expected Result: A publicly accessible HTML website featuring a functioning Bootstrap carousel.

## Lesson 2: Understanding HTML Structure and Common Elements

Difficulty: Beginner

### Learning Objectives

Understand how HTML organizes content and how different HTML elements are used to create a webpage.

### Topics Covered

- Understanding `<head>` and `<body>`.
- Headings: `<h1>` through `<h6>`.
- Paragraphs and text formatting.
- Hyperlinks and navigation.
- Images and image attributes.
- Lists: ordered and unordered.
- Semantic HTML elements:
  - `<header>`
  - `<nav>`
  - `<main>`
  - `<section>`
  - `<footer>`
- Using `class` and `id` attributes.

### Hands-On Exercise

Exercise: Expand Your Website

Using the website from Lesson 1:

1. Add a header containing the website title.
2. Add a navigation area with three links.
3. Create an "About Me" section with a heading and paragraph.
4. Add a photograph or image.
5. Add a footer with copyright information.

Expected Result: A properly structured HTML website containing a header, navigation, main content, and footer.

# Part 2: Introduction to CSS and Website Styling

## Lesson 3: Introduction to CSS — Colors, Fonts, and Backgrounds

Difficulty: Beginner

### Learning Objectives

Understand how CSS controls the visual appearance of HTML elements.

### Topics Covered

- What is CSS?
- Inline CSS vs. internal CSS vs. external stylesheets.
- Creating and linking `style.css`.
- CSS selectors:
  - Element selectors
  - Class selectors
  - ID selectors
- Understanding CSS properties and values.
- Setting text colors.
- Setting background colors.
- Understanding hexadecimal and RGB color values.
- Changing font families and sizes.
- Using Google Fonts.
- Understanding CSS specificity and the cascade.

### Example CSS

```
body {
  background-color: #f5f5f5;
  color: #333333;
  font-family: Arial, sans-serif;
}

h1 {
  color: #0056b3;
  font-size: 36px;
}

.site-header {
  background-color: #003366;
  color: white;
}
```

### Hands-On Exercise

Exercise: Give Your Website a New Look

Students will:

1. Create an external `style.css` file.
2. Link the stylesheet to `index.html`.
3. Change the website background color.
4. Change the color and font of the main heading.
5. Change the header and footer background colors.
6. Commit the updated styling to GitHub.

Expected Result: Students understand how to customize a website's basic visual appearance using CSS.

## Lesson 4: CSS Spacing — Margin, Padding, Borders, and the Box Model

Difficulty: Beginner

### Learning Objectives

Understand how spacing affects layout and readability.

### Topics Covered

- Understanding the CSS Box Model.
- Difference between margin and padding.
- Using pixels, percentages, `rem`, and `em`.
- Adding borders and border-radius.
- Understanding element width and height.
- Centering content.
- Introduction to `max-width`.
- Understanding `box-sizing`.

### Visual Reference: CSS Box Model

Each HTML element occupies space defined by its content, padding, border, and margin.

### Example CSS

```
.content-box {
  background-color: #ffffff;
  padding: 20px;
  margin: 30px auto;
  border: 1px solid #cccccc;
  border-radius: 8px;
  max-width: 800px;
}
```

### Hands-On Exercise

Exercise: Improve Website Spacing

Students will:

1. Add padding to the header.
2. Add margins between page sections.
3. Place the About Me content inside a styled box.
4. Add a border and rounded corners.
5. Center the content area and limit its maximum width.

Expected Result: A cleaner, more organized website with consistent spacing.

# Part 3: Bootstrap Layout and Customization

## Lesson 5: Bootstrap Containers, Grid System, and Responsive Design

Difficulty: Beginner to Intermediate

### Learning Objectives

Understand how Bootstrap organizes page layouts and adapts to different devices.

### Topics Covered

- Bootstrap container classes.
- Difference between `.container` and `.container-fluid`.
- Understanding Bootstrap rows and columns.
- The 12-column grid system.
- Common grid classes:
  - `.row`
  - `.col`
  - `.col-md-6`
  - `.col-lg-4`
- Introduction to breakpoints.
- Responsive layouts for mobile, tablet, and desktop.
- Using browser developer tools to test screen sizes.

### Example Bootstrap Layout

```
<div class="container">
  <div class="row">
    <div class="col-md-6">
      <h2>Left Column</h2>
      <p>Content for the left column.</p>
    </div>

    <div class="col-md-6">
      <h2>Right Column</h2>
      <p>Content for the right column.</p>
    </div>
  </div>
</div>
```

### Hands-On Exercise

Exercise: Create a Two-Column Layout

Students will:

1. Add a Bootstrap container.
2. Create a row containing two columns.
3. Add a heading and paragraph inside each column.
4. Test the website at desktop and mobile widths.
5. Observe how columns stack on smaller screens.

Expected Result: A responsive two-column layout.

## Lesson 6: Styling Bootstrap Components and Using Utility Classes

Difficulty: Beginner to Intermediate

### Learning Objectives

Understand how to customize Bootstrap components and use utility classes to control appearance.

### Topics Covered

- Reviewing common Bootstrap components:
  - Navigation bars
  - Buttons
  - Cards
  - Carousels
  - Alerts
- Bootstrap background and text color utilities.
- Bootstrap spacing utilities:
  - `mt-*`, `mb-*`
  - `pt-*`, `pb-*`
  - `m-*`, `p-*`
- Bootstrap border and shadow utilities.
- Understanding how custom CSS overrides Bootstrap defaults.
- Importance of stylesheet loading order.
- Avoiding modifications to Bootstrap's source files.

### Example

```
<div class="card shadow-sm p-3 mb-4">
  <div class="card-body">
    <h3 class="card-title">Welcome!</h3>
    <p class="card-text">
      This is a customized Bootstrap card.
    </p>
    <a href="#" class="btn btn-primary">
      Learn More
    </a>
  </div>
</div>
```

### Hands-On Exercise

Exercise: Customize a Bootstrap Card

Students will:

1. Add a Bootstrap card to their website.
2. Change the card's background color.
3. Apply padding and margin utility classes.
4. Add a shadow and rounded corners.
5. Customize the button color using external CSS.

Expected Result: A Bootstrap component customized using utility classes and CSS.

## Lesson 7: Creating a Consistent Website Theme

Difficulty: Intermediate

### Learning Objectives

Understand how reusable CSS styles establish consistent branding across a website.

### Topics Covered

- What is a website theme?
- Selecting a consistent color palette.
- Choosing primary and secondary colors.
- Typography and font hierarchy.
- Consistent spacing and button styles.
- Introduction to CSS custom properties (variables).
- Designing reusable CSS classes.
- Customizing Bootstrap navigation and carousel appearance.
- Using browser developer tools to inspect and troubleshoot styles.

### Example CSS

```
:root {
  --primary-color: #003366;
  --secondary-color: #e7b645;
  --text-color: #333333;
  --background-color: #ffffff;
}

body {
  color: var(--text-color);
  background-color: var(--background-color);
}

.site-header {
  background-color: var(--primary-color);
}

.btn-primary {
  background-color: var(--primary-color);
  border-color: var(--primary-color);
}

.btn-primary:hover {
  background-color: #005599;
  border-color: #005599;
}
```

### Hands-On Exercise

Exercise: Create Your Own Website Branding

Students will:

1. Select two primary website colors.
2. Define them using CSS variables.
3. Apply those colors to the header, buttons, and footer.
4. Choose a consistent font family.
5. Customize the Bootstrap carousel captions and navigation styling.

Expected Result: A website with consistent branding and reusable style definitions.

# Part 4: Introduction to Sass and Advanced Theming

## Lesson 8: Introduction to Sass (SCSS)

Difficulty: Intermediate

### Learning Objectives

Understand how Sass extends CSS and makes theme development easier to maintain.

### Topics Covered

- What is Sass?
- Difference between CSS and SCSS.
- Why developers use CSS preprocessors.
- Sass variables.
- Nesting CSS rules.
- Understanding Sass partials.
- Compiling SCSS into CSS.
- Introduction to the Sass command-line compiler.
- Organizing styles into multiple files.

### Example SCSS

```
$primary-color: #003366;
$secondary-color: #e7b645;

.site-header {
  background-color: $primary-color;
  padding: 20px;

  h1 {
    color: white;
    font-size: 32px;
  }

  a {
    color: $secondary-color;

    &:hover {
      color: white;
    }
  }
}
```

### Hands-On Exercise

Exercise: Convert CSS into SCSS

Students will:

1. Create a `style.scss` file.
2. Define variables for primary and secondary colors.
3. Convert a few existing CSS rules into nested SCSS.
4. Compile the SCSS into CSS.
5. Confirm their website still renders correctly.

Expected Result: Students understand that Sass is compiled into standard CSS that browsers can interpret.

## Lesson 9: Customizing Bootstrap with Sass

Difficulty: Intermediate

### Learning Objectives

Understand how Bootstrap's Sass variables can be used to create a customized Bootstrap build.

### Topics Covered

- Understanding Bootstrap's Sass architecture.
- Difference between overriding Bootstrap with CSS and compiling a customized Bootstrap build.
- Introduction to Bootstrap theme variables.
- Modifying primary and secondary colors.
- Modifying typography variables.
- Modifying border-radius and spacing variables.
- Compiling customized Bootstrap CSS.
- Organizing custom theme source files.
- Maintaining Bootstrap upgrade compatibility.

### Example SCSS

```
// Customize Bootstrap variables
$primary: #003366;
$secondary: #e7b645;
$border-radius: 10px;

// Import Bootstrap Sass
@import "bootstrap/scss/bootstrap";
```

Instructor note: This example assumes Bootstrap 5.3.x with its Sass source installed and resolvable by the compiler. The course should standardize on one Bootstrap version and build process.

### Hands-On Exercise

Exercise: Customize Bootstrap's Colors

Students will:

1. Change Bootstrap's primary color to a color of their choice.
2. Change Bootstrap's secondary color.
3. Recompile Bootstrap's CSS.
4. Update a button to use `.btn-primary`.
5. Confirm that the button reflects their custom Bootstrap color.

Expected Result: A customized Bootstrap stylesheet built from Sass variables.

# Part 5: Introduction to Drupal Website Theming

## Lesson 10: Understanding Drupal Themes and Twig Templates

Difficulty: Beginner Drupal / Intermediate HTML and CSS

### Learning Objectives

Understand how Drupal generates HTML and how themes control the website's appearance.

### Topics Covered

- What is Drupal?
- Difference between static HTML websites and content management systems.
- Understanding Drupal's frontend rendering process.
- Introduction to Drupal themes.
- Base themes and subthemes.
- Drupal theme directory structure.
- Introduction to Twig templating.
- Understanding important theme files:
  - `.info.yml`
  - `.libraries.yml`
  - `.theme`
  - `page.html.twig`
  - `node.html.twig`
  - `html.html.twig`
- How Drupal attaches CSS and JavaScript.
- Enabling and setting a Drupal theme as default.
- Understanding theme cache rebuilding.

### Example Theme Structure

```
themes/
└── custom/
    └── mytheme/
        ├── mytheme.info.yml
        ├── mytheme.libraries.yml
        ├── css/
        │   └── style.css
        ├── js/
        └── templates/
            └── page.html.twig
```

### Hands-On Exercise

Exercise: Explore a Drupal Theme

Students will:

1. Log into a preconfigured Drupal development website.
2. Navigate to Appearance.
3. Identify the currently active theme.
4. Explore the theme's folder structure.
5. Identify where the theme's CSS and Twig files are located.
6. Change a simple style in a custom theme's stylesheet.
7. Rebuild Drupal's cache and observe the change.

Expected Result: Students understand where Drupal theme files are located and how changes affect the website.

## Lesson 11: Building a Bootstrap-Based Drupal Theme

Difficulty: Intermediate

### Learning Objectives

Apply HTML, CSS, Bootstrap, and Sass skills to a Drupal theme.

### Topics Covered

- Creating a custom Drupal theme.
- Configuring the theme's `.info.yml` file.
- Registering CSS and JavaScript using `.libraries.yml`.
- Including Bootstrap in a Drupal theme.
- Understanding Twig templates and Drupal regions.
- Creating reusable header and footer styling.
- Overriding Twig templates.
- Using Bootstrap containers and grid classes within Twig.
- Applying Sass-generated CSS to Drupal.
- Understanding Drupal cache rebuilds during theme development.

### Example Drupal Theme Configuration

mytheme.info.yml

```
name: My Custom Theme
type: theme
description: 'A custom Bootstrap-based Drupal theme.'
core_version_requirement: ^11
base theme: false

libraries:
  - mytheme/global-styling

regions:
  header: Header
  content: Content
  footer: Footer
```

mytheme.libraries.yml

```
global-styling:
  css:
    theme:
      css/bootstrap.min.css: {}
      css/style.css: {}
  js:
    js/bootstrap.bundle.min.js: {}
```

Instructor note: This example assumes the compiled Bootstrap assets have been placed in the indicated theme directories. For this exercise, the theme includes Bootstrap directly rather than inheriting from a Bootstrap base theme.

### Hands-On Exercise

Exercise: Create a Simple Drupal Theme

Students will:

1. Create a custom theme directory.
2. Add a theme `.info.yml` file.
3. Add a `.libraries.yml` file.
4. Include Bootstrap and a custom CSS stylesheet.
5. Enable the theme in Drupal.
6. Apply custom colors to the header and footer.
7. Rebuild Drupal's cache.

Expected Result: A functioning custom Drupal theme using Bootstrap and custom CSS.

# Part 6: Final Project and Practical Application

## Lesson 12: Theming a Complete Website — Final Project

Difficulty: Intermediate

### Learning Objectives

Demonstrate the ability to apply the techniques learned throughout the course to a cohesive website design.

### Topics Covered

- Reviewing HTML page structure.
- Using Bootstrap for responsive layout.
- Applying a consistent color palette.
- Applying fonts and typography.
- Using margin and padding appropriately.
- Customizing Bootstrap components.
- Maintaining reusable styles in SCSS.
- Applying the same visual theme to Drupal.
- Testing desktop and mobile layouts.
- Basic troubleshooting using browser developer tools.

### Final Student Project

Exercise: Create a Branded Website

Students will create a small website for a fictional business, organization, or personal portfolio.

### Project Requirements

- A header displaying the website name or logo.
- A Bootstrap navigation bar.
- A Bootstrap carousel containing at least three images.
- An About section.
- A two- or three-column Bootstrap layout.
- At least one customized Bootstrap card.
- A footer containing contact or copyright information.
- Consistent colors and typography.
- Appropriate margins and padding.
- Responsive display on mobile and desktop.
- A custom CSS or compiled SCSS stylesheet.
- A GitHub repository containing the website code.
- A Drupal theme or Drupal page incorporating the same branding.

Expected Result: A fully themed, responsive website demonstrating the student's ability to use Bootstrap, CSS, Sass, and Drupal.

# Recommended Course Schedule

| Lesson | Topic                                       | Difficulty            | Duration |
| ------ | ------------------------------------------- | --------------------- | -------- |
| 1      | Introduction to HTML, Bootstrap, and GitHub | Beginner              | 90 min   |
| 2      | HTML Structure and Elements                 | Beginner              | 60 min   |
| 3      | CSS Colors, Fonts, and Backgrounds          | Beginner              | 90 min   |
| 4      | CSS Margin, Padding, and Box Model          | Beginner              | 60 min   |
| 5      | Bootstrap Grid and Responsive Design        | Beginner–Intermediate | 90 min   |
| 6      | Bootstrap Components and Utilities          | Beginner–Intermediate | 90 min   |
| 7      | Creating a Consistent Website Theme         | Intermediate          | 90 min   |
| 8      | Introduction to Sass                        | Intermediate          | 90 min   |
| 9      | Customizing Bootstrap with Sass             | Intermediate          | 90 min   |
| 10     | Drupal Themes and Twig Templates            | Intermediate          | 90 min   |
| 11     | Building a Bootstrap-Based Drupal Theme     | Intermediate          | 90 min   |
| 12     | Final Website Theming Project               | Intermediate          | 90 min   |

Total instructional time: Approximately 17 hours.

# Recommended Teaching Methodology

Each lesson should follow the same predictable structure to help beginning students learn without becoming overwhelmed.

| Phase                    | Duration      | Activity                                         |
| ------------------------ | ------------- | ------------------------------------------------ |
| Review                   | 10 minutes    | Review the previous lesson and answer questions  |
| Explanation              | 15–20 minutes | Introduce new concepts with practical examples   |
| Instructor demonstration | 15–20 minutes | Demonstrate the concepts using the class website |
| Student exercise         | 20–30 minutes | Students perform the same or a similar task      |
| Review and questions     | 5–10 minutes  | Review student results and troubleshoot problems |

For lessons involving Sass compilation or Drupal setup, reserve additional time for installation and environment-related issues.

## Recommended Class Project Structure

Rather than creating an entirely new website during every lesson, students should continuously improve the website established in Lesson 1.

By Lesson 9, the static project could have the following structure:

```
my-website/
│
├── index.html
├── about.html
├── contact.html
│
├── css/
│   ├── bootstrap.min.css
│   └── style.css
│
├── scss/
│   ├── _variables.scss
│   ├── _components.scss
│   └── style.scss
│
├── js/
│   └── bootstrap.bundle.min.js
│
└── images/
    ├── slide1.jpg
    ├── slide2.jpg
    └── slide3.jpg
```

For Lessons 10–12, students transition to a preconfigured Drupal 11 development environment where they can reproduce their static website's styling.

## Recommended Instructor Resources

- Bootstrap 5 Documentation
- Bootstrap Utilities
- MDN HTML Guide
- MDN CSS Guide
- Sass Documentation
- Drupal Theming Guide
- Twig Documentation
- GitHub Pages Documentation

# Student Assessment and Course Completion

The course should prioritize practical experience over formal examinations.

| Assessment                                 | Weight |
| ------------------------------------------ | ------ |
| Participation and class exercises          | 30%    |
| Static website HTML and CSS implementation | 20%    |
| Bootstrap and Sass customization           | 20%    |
| Final project including Drupal theming     | 30%    |
| Total                                      | 100%   |

### Course Completion Goals

A successful student should be able to independently take a basic HTML or Bootstrap website and change its visual identity by modifying its colors, fonts, spacing, components, and layouts.

Students should also understand how those techniques translate into Drupal theme development, including the relationship between HTML, Twig templates, Bootstrap components, CSS, and compiled Sass.

Recommended instructional priority: Spend the first nine lessons building confidence in HTML, CSS, and Bootstrap before introducing Drupal. This allows students to understand frontend theming independently of Drupal's rendering and configuration systems, making the transition into Drupal significantly easier.
