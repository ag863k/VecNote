# @repo/eslint-config

ESLint configurations for VecNote applications and packages.

## Configurations

- `base.js` - Base ESLint configuration for all JavaScript/TypeScript projects
- `next.js` - Next.js specific rules and configurations  
- `react-internal.js` - React component library configurations

## Usage

In your ESLint config file:

```javascript
// For Next.js apps
module.exports = {
  extends: ["@repo/eslint-config/next"],
};

// For React libraries
module.exports = {
  extends: ["@repo/eslint-config/react-internal"],
};

// For backend Node.js projects
module.exports = {
  extends: ["@repo/eslint-config/base"],
};
```

## Rules

These configurations include:
- TypeScript support
- React best practices
- Next.js specific optimizations
- Import/export linting
- Code formatting integration with Prettier
