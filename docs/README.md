# SMTV Design Tokens Documentation

This documentation provides detailed information about the SMTV design tokens system, how to use it, and best practices.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Token Categories](#token-categories)
- [CSS Variables Reference](#css-variables-reference)
- [Best Practices](#best-practices)
- [Contributing](#contributing)

## Installation

```bash
npm install @smtv/design-tokens
```

## Usage

### Basic Usage
Import the CSS variables in your project:

```css
@import '@smtv/design-tokens/dist/design-tokens.css';
```

### Using in Components
Example usage in a React component:

```jsx
const Button = styled.button`
  background-color: var(--color-primary);
  color: var(--color-text-primary);
  padding: var(--component-button-padding);
  border-radius: var(--component-button-radius);
  height: var(--component-button-height-medium);
  min-width: var(--component-button-min-width-default);
  
  &:hover {
    background-color: var(--color-primary-dark);
  }
  
  &:focus {
    outline: var(--focus-outline-width) var(--focus-ring-style) var(--color-focus-ring);
    background-color: var(--color-focus-bg);
  }
`;
```

## Token Categories

### Colors
- Primary colors
- Background colors
- Text colors
- Status colors (success, warning, error)
- Focus states

### Typography
- Font families
- Font sizes
- Font weights

### Spacing
- Consistent spacing scale (xs to xxl)
- Component-specific spacing

### Components
- Button dimensions and properties
- Card properties
- Input field properties
- Header dimensions

### Animation
- Transition durations
- Timing functions
- Focus animations

### TV-specific
- TV dimensions
- Base font size

## CSS Variables Reference

### Colors
```css
--color-primary: #007AFF;
--color-primary-dark: #0056B3;
--color-background: #121212;
--color-surface: #1E1E1E;
--color-text-primary: #FFFFFF;
--color-text-secondary: #B3B3B3;
--color-success: #34C759;
--color-warning: #FFD60A;
--color-error: #FF3B30;
```

### Typography
```css
--font-family-primary: 'Inter', sans-serif;
--font-family-secondary: 'SF Pro Display', sans-serif;
--font-size-h1: 48px;
--font-size-h2: 36px;
--font-size-h3: 28px;
--font-size-body: 24px;
--font-size-small: 16px;
--font-weight-regular: 400;
--font-weight-medium: 500;
--font-weight-bold: 700;
```

### Spacing
```css
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 32px;
--spacing-xxl: 48px;
```

### Components
```css
--component-button-height-small: 36px;
--component-button-height-medium: 48px;
--component-button-height-large: 64px;
--component-button-padding: 16px 24px;
--component-button-radius: 8px;
--component-card-size: 300px;
--component-card-padding: 24px;
--component-card-radius: 24px;
```

## Best Practices

1. **Always Use Variables**
   - Never use hardcoded values
   - Use the provided CSS variables for consistency

2. **Component Development**
   - Use component-specific tokens when available
   - Fall back to general tokens when needed

3. **TV-Specific Considerations**
   - Use TV-specific tokens for layout
   - Consider focus states for TV navigation
   - Use appropriate font sizes for TV viewing distance

4. **Accessibility**
   - Maintain color contrast ratios
   - Use focus indicators consistently
   - Consider text readability at different sizes

## Contributing

### Adding New Tokens
1. Add new tokens to the appropriate JSON file in `tokens/source/`
2. Follow the existing structure and naming conventions
3. Run `npm run build` to test
4. Update documentation if needed

### Modifying Existing Tokens
1. Update the token in the appropriate JSON file
2. Consider the impact on existing components
3. Update the version number appropriately
4. Update documentation

### Version Control
- Use semantic versioning
- Document breaking changes
- Update the changelog

## Support

For issues or questions, please create an issue in the GitHub repository:
https://github.com/rvd2pwipwip/smtv-design-tokens/issues 