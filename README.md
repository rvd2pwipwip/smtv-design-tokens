# SMTV Design Tokens

This repository contains the design tokens used across the SMTV component library and TV app prototype. It serves as the single source of truth for design tokens in the form of CSS variables.

## Installation

```bash
npm install @smtv/design-tokens
```

## Usage

Import the CSS variables in your project:

```css
@import '@smtv/design-tokens/dist/tokens.css';
```

## Structure

- `tokens/` - Contains the token definitions in JSON format
- `dist/` - Contains the built CSS variables and other formats
- `scripts/` - Contains build scripts to generate different token formats

## Development

1. Clone the repository
2. Install dependencies: `npm install`
3. Make changes to tokens in the `tokens/` directory
4. Build: `npm run build`

## License

ISC 