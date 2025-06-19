# @repo/typescript-config

Shared TypeScript configurations for VecNote applications and packages.

## Configurations

- `base.json` - Base TypeScript configuration for all projects
- `nextjs.json` - Next.js specific TypeScript settings
- `react-library.json` - React component library configuration

## Usage

In your `tsconfig.json`:

```json
{
  "extends": "@repo/typescript-config/base.json",
  "compilerOptions": {
    "outDir": "./dist"
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules", "dist"]
}
```

### For Next.js apps:
```json
{
  "extends": "@repo/typescript-config/nextjs.json"
}
```

### For React libraries:
```json
{
  "extends": "@repo/typescript-config/react-library.json"
}
```

## Features

- Strict TypeScript settings for better code quality
- Path mapping support for clean imports
- React and JSX support
- ESNext features enabled
- Proper module resolution
- Source map generation for debugging
