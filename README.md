# Gravity Forms SCSS

More controlled CSS output for the Gravity Forms plugin. Helpful for when you're creating custom WP themes for clients Up to date for GF v1.7.9

The current GF CSS output on the frontend consists of the following:

- formsreset.css
- datepicker.css
- formsmain.css
- readyclass.css
- browsers.css
- rtl.css (if RTL is enabled)

That's six HTTP requests and nearly 120K of CSS. Great for if you're using every featrue of GF but not so great when you only plan on using a few of its core form fields.

## How to Use

1. Drop the `gravityforms.scss` file and `gravityforms` folder into your current SCSS project
2. Open up the `gravityforms.scss` file and optionally enable/disable the partials
3. When you compile it should output a `gravityforms.css` in the CSS directory (defined in your compiler)
4. Under the GF settings in WordPress, disable the CSS output (Forms --> Settings)
5. Register and enqueue the `gravityforms.css` stylesheet in your `functions.php` like a good developer

## Benchmark

For a basic form that only uses text inputs, textareas, radio buttons and checkboxes and **not** any of GF's more advanced pricing, CAPTCHA or post fields:

Plugin Output:

- Five CSS Files
- 106K of CSS

Customised Output:

- One CSS File
- 30K of CSS

## What's Next

Ideally a future update will include some variables for colours, typography and gradients (etc) to customise the CSS in the compiled output.