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

For detailed documentation, including token reference, best practices, and examples, see our [Documentation](docs/README.md).

## Structure

- `tokens/` - Contains the token definitions in JSON format
- `dist/` - Contains the built CSS variables and other formats
- `scripts/` - Contains build scripts to generate different token formats
- `docs/` - Contains detailed documentation and usage examples

## How to Edit or Add Design Tokens (For Designers)

Follow these steps to update or add new design tokens:

1. **Locate the Token Files**
   - All design tokens are defined in JSON files inside the `tokens/source/` directory. Common files include:
     - `colors.json` for color tokens
     - `typography.json` for font and text tokens
     - `spacing.json` for spacing, sizing, and border radius tokens
     - `animation.json` for animation and timing tokens

2. **Edit or Add a Token**
   - Open the relevant JSON file in a text editor.
   - Each token follows this structure:
     ```json
     "token-name": {
       "value": "your-value-here",
       "type": "token-type-here"
     }
     ```
   - For nested tokens, follow the existing hierarchy. Example (from `colors.json`):
     ```json
     "primary": {
       "value": "#007AFF",
       "type": "color"
     }
     ```
   - To add a new token, copy an existing entry and update the name and value as needed.
   - **Be careful with commas and brackets to keep the JSON valid!**

3. **Save Your Changes**
   - After editing, save the file. Optionally, use a JSON linter/formatter to check for errors.

4. **Build the Tokens**
   - In your terminal, run:
     ```bash
     npm run build
     ```
   - This will generate the updated CSS and other formats in the `dist/` directory using [Style Dictionary](https://amzn.github.io/style-dictionary/).

5. **Preview and Test**
   - Check the output in `dist/design-tokens.css` to ensure your changes are reflected as CSS variables.
   - If you use the tokens in a project, import the updated CSS and verify the new/changed tokens work as expected.

6. **Commit and Push**
   - Once satisfied, commit your changes and open a pull request if required by your workflow.

For more details on token structure or best practices, see the [Documentation](docs/README.md).

## Development

1. Clone the repository
2. Install dependencies: `npm install`
3. Make changes to tokens in the `tokens/` directory
4. Build: `npm run build`

## Publishing to npm

To publish the design tokens package to npm, follow these steps:

1. **Build the Tokens**
   - Ensure your local changes are committed and the tokens are up to date:
     ```bash
     npm run build
     ```

2. **Update the Version**
   - Bump the version in `package.json` according to the changes (major, minor, or patch):
     ```bash
     npm version <patch|minor|major>
     ```

3. **Login to npm (if needed)**
   - If you haven't logged in before or your session expired:
     ```bash
     npm login
     ```

4. **Publish the Package**
   - Run the following command to publish:
     ```bash
     npm publish --access public
     ```
   - Ensure you have the necessary permissions for the `@smtv` scope.

5. **Verify**
   - Check the npm registry or your project to confirm the new version is available.

For more details, see the [npm publishing docs](https://docs.npmjs.com/cli/v10/commands/npm-publish).

## License

ISC 