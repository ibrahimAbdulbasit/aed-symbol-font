# NewAED Font

A custom font for displaying the AED (UAE Dirham) currency symbol, based on the Inter font.

## About

This font was created to provide a clean, consistent way to display the AED currency symbol that matches the style of Inter, a popular sans-serif typeface. This approach follows a similar solution used for the Saudi Riyal symbol.

**This implementation is inspired by Dom Monhardt's approach** detailed in his blog post ["🇸🇦🪙 The New Saudi Riyal Symbol and the Future of GCC Currencies"](https://www.one-fs.com/p/the-new-saudi-riyal-symbol-and-the), where he developed a custom font solution for the Saudi Riyal symbol.

**NewAED is a derivative work based on Inter**, with modifications focused on providing a dedicated AED currency symbol. The font has been modified from the original Inter typeface created by Rasmus Andersson.

The font contains a subset of characters, focusing specifically on the AED symbol while maintaining typographic consistency with the Inter font family.

## How It Works

The solution follows a similar approach to the Saudi Riyal symbol implementation:
- The font is a modified version of Inter where the letters 'a' and 'e' were removed, and 'd' was edited to create the AED symbol
- When applied to text displaying "AED", it renders the custom AED symbol instead
- If the font fails to load, "AED" remains as a readable fallback
- This approach ensures seamless integration while avoiding the need for image assets or vector graphics

## Usage

### Web Usage

1. Include the font in your project:
   ```
   /your-project
   ├── font/
   │   └── Newaed-Regular.ttf
   ├── css/
   │   └── styles.css
   └── index.html
   ```

2. Add the font-face declaration in your CSS:
   ```css
   @font-face {
     font-family: 'NewAED';
     src: url('../font/Newaed-Regular.ttf') format('truetype');
     font-weight: normal;
     font-style: normal;
   }
   ```

3. Apply the font to your AED symbols:
   ```css
   .aed-symbol {
     font-family: 'NewAED', sans-serif;
   }
   ```

4. Use it in your HTML:
   ```html
   <span class="aed-symbol">AED</span> 199.99
   ```

### CSS Fallback

For better compatibility, consider using a font stack:

```css
.aed-symbol {
  font-family: 'NewAED', 'Arial Unicode MS', 'Arial', sans-serif;
}
```

## Demo

Open `index.html` in your browser to view a demonstration of the font in action.

## License

This font is a derivative work based on Inter, which is licensed under the SIL Open Font License, Version 1.1.

### Important Licensing Notes

According to the SIL Open Font License:

1. This modified font has been renamed (NewAED) to avoid confusion with the original Inter font, as required by the license.
2. This font may be used freely for both personal and commercial projects.
3. This font may be distributed with the same SIL Open Font License.
4. This font may not be sold by itself, but can be included as part of a larger project or software package.

### Original Font

The original Inter font is Copyright (c) 2016-2020 The Inter Project Authors and is available at:
https://github.com/rsms/inter

### Full License

The full SIL Open Font License text is included in the `LICENSE` file in this repository.

## GitHub Repository

This project is available on GitHub at: https://github.com/ibrahimAbdulbasit/aed-symbol-font

## Credits

- Original Inter font designed by Rasmus Andersson
- AED symbol implementation by [Ibrahim Abdulbasit](https://www.ibrahim-abdulbasit.com)
- Implementation approach inspired by Dom Monhardt's Saudi Riyal symbol solution 