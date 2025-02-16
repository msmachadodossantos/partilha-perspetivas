# About

**chroma-rio** is a Sass tool designed to simplify the process of generating color palettes based on the RGB color wheel.

With a focus on flexibility and ease of use, **chroma-rio** is ideal for web developers and designers who want to streamline the creation of visually appealing and harmonious color schemes **using only CSS variables**.

## Dependencies

Before using **chroma-rio**, ensure you have the following dependencies installed:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en) or [npm](https://www.npmjs.com/)
- [Sass](https://sass-lang.com/)
- [Gulp](https://gulpjs.com/)

## Installation

To get started, follow these steps:

1. Clone the repository to your local machine:
   - `git clone https://github.com/msmachadodossantos/chroma-rio.git`
2. Navigate to the project directory:
   - `cd chroma-rio`
3. Install the project dependencies:
   - `npm install`

## Configuration

To customize the color palette, modify the six primary colors in the `src/_variables.scss` file.

## Building

Once you've configured your color palette, it's time to build the project. Run the following command:

- `npm run build`
- This command not only compiles the Sass files but also build the included Bootstrap (v5.3.2, and v5.3.3) with the newly defined colors.

The resulting output can be found in the `dist` directory.

## How to use it

### Choosing CSS Files

Before integrating custom colors into your project, you need to decide which CSS files you want to attach. The available options are:

- rgb-wheel.css
- rgb-wheel-ten-variants.css
- rgb-wheel-twenty-variants.css
- rgb-wheel-fifty-variants.css
- rgb-wheel-hundred-variants.css
- brand-ten-variants.css
- brand-twenty-variants.css
- brand-fifty-variants.css
- brand-hundred-variants.css
- primary-ten-variants.css
- primary-twenty-variants.css
- primary-fifty-variants.css
- primary-hundred-variants.css
- secondary-ten-variants.css
- secondary-twenty-variants.css
- secondary-fifty-variants.css
- secondary-hundred-variants.css
- tertiary-ten-variants.css
- tertiary-twenty-variants.css
- tertiary-fifty-variants.css
- tertiary-hundred-variants.css
- quaternary-ten-variants.css
- quaternary-twenty-variants.css
- quaternary-fifty-variants.css
- quaternary-hundred-variants.css
- quinary-ten-variants.css
- quinary-twenty-variants.css
- quinary-fifty-variants.css
- quinary-hundred-variants.css
- shadow-ten-variants.css
- shadow-twenty-variants.css
- shadow-fifty-variants.css
- shadow-hundred-variants.css
- elevation.css

### Applying Colors to the Body

Once you've made your selection, you can apply the chosen color to the background of the body element using the following CSS rule:

```css
body {
  background-color: var(--cr-colorName-variation-quantity);
}
```

The shadow color doesn't have a variation. Example:

```css
p {
  color: var(--cr-shadow-quantity);
}
```

Here's a breakdown of the placeholders within the CSS rule:

- **colorName**: Choose from the following options:
  - Any of the 12 colors in the RGB color wheel
    - red
    - orange
    - yellow
    - chartreuseGreen
    - green
    - springGreen
    - cyan
    - azure
    - blue
    - violet
    - magenta
    - rose
  - brand
  - primary
  - secondary
  - tertiary
  - quaternary
  - quinary
  - shadow
- **variation**: Select from:
  - light
  - tone
  - dark
- **quantity**: An integer indicating the chosen variation of the color in the attached file. This should be between 0 and 100. Additionally, you can use steps of 2, 5, and 10 for more precise adjustments.

### Elevation Colors

For elevation colors, you have two modes:

- Light Mode
- Dark Mode

These colors only have 6 steps (0 to 5). To apply them, use the following CSS rule:

```css
body {
  background-color: var(--cr-elevation-mode-step);
}
```

Replace placeholders accordingly:

- **mode**: Choose from:
  - light
  - dark
- **step**: An integer indicating the chosen step of elevation color (0 to 5).
