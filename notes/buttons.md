# Styling Buttons

## Button Font Inheritance

**Buttons Don't Inherit Body Fonts.** Buttons (`<button>, <input type="button">`, etc.) do not automatically inherit font properties from the body element due to browser default styling. This is an important consideration when styling forms and interactive elements.

```css
/* Explicitly set font properties for buttons */
button, 
input[type="button"], 
input[type="submit"], 
input[type="reset"] {
  font-family: 'Your-Font', sans-serif;
  font-size: 16px;
  font-weight: 400;
}
```

Reasons for this behavior:

1. **Browser User Agent Stylesheets:** Each browser has its own default styles for form elements including buttons, which often override inheritance.

2. **Form Control Consistency:** Browsers aim to maintain a consistent look for form controls across different websites.

3. **Operating System Integration:** Buttons are typically styled to match the operating system's native UI controls.

4. **Historical Precedent:** Form elements predate many modern CSS capabilities and their styling behavior reflects earlier web standards.

To ensure consistent appearance across browsers, always explicitly specify font properties for buttons rather than relying on inheritance. This creates a more predictable and manageable.

---

## Button Sizing Guidelines

### Button Box Model Explanation

When discussing button sizes in CSS, we refer to the total visible size of the button including padding and border (the border-box).
This sizing approach follows the common CSS box-sizing: border-box model, where the specified dimensions include:

- The content area
- The padding
- The border

This is the most practical way to think about button dimensions since it represents what users actually see and interact with. Using border-box sizing also makes layout planning more intuitive since the dimensions you specify are the actual space the element takes up in your interface. If you're writing CSS for these buttons, you'd typically want to include:

```css
.button {
  box-sizing: border-box;
  width: 140px;
  height: 40px;
  /* Other styling properties */
}
```

This ensures that any padding or borders you add won't expand the button beyond your intended dimensions.

### When to Use 140px × 40px Buttons

This size range (130-150px × 35-45px) is particularly appropriate for:

- Primary action buttons (Submit, Continue, Next)
- Secondary action buttons (Cancel, Back, Previous)
- Form submission buttons
- Navigation buttons within multi-step processes
- Call-to-action buttons that need prominence without dominating the page
- Buttons in desktop applications or non-mobile-optimized websites
- Buttons containing text of moderate length (2-3 words)

These medium-sized buttons strike a balance between visibility and screen real estate efficiency, making them ideal for standard web applications and interfaces where button actions are important but not the sole focus of the design.

---
