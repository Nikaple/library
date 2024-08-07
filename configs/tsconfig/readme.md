# `@nikaple/tsconfig 🥷🎯`

[![discord-image]][discord-url]
[![workflow-image]][workflow-url]
[![npm-image]][npm-url]

> **Latipun TypeScript Configuration**
>
> 🥷 Nerdy Ninja's shareable TypeScript [configuration](https://www.typescriptlang.org/tsconfig/) 🎯

## Getting Started

```sh
yarn add -D @nikaple/tsconfig typescript
```

- NodeJS ESModule target

  ```json
  // tsconfig.json
  {
    "extends": "@nikaple/tsconfig/esm",
    "include": ["src/**/*", "**/*.config.ts"],
    "exclude": ["**/node_modules", "**/dist"],
    "compilerOptions": {}
  }
  ```

- NextJS apps

  ```json
  // tsconfig.json
  {
    "extends": "@nikaple/tsconfig/next",
    "include": ["src/**/*", "**/*.config.ts"],
    "exclude": ["**/node_modules", "**/dist"],
    "compilerOptions": {}
  }
  ```

- NodeJS CommonJS target

  ```json
  // tsconfig.json
  {
    "extends": "@nikaple/tsconfig/cjs",
    "include": ["src/**/*", "**/*.config.ts"],
    "exclude": ["**/node_modules", "**/dist"],
    "compilerOptions": {}
  }
  ```

**Note**: Since typescript's `extends` has behavior that properties with relative paths found in the configuration file, which aren't excluded from inheritance, will be resolved relative to the configuration file they originated in.

This means, `files`, `include`, `exclude`, and other properties that accept relative path like `compilerOptions.baseUrl`, `compilerOptions.paths`, etc, you need to specify it yourself.

## Hacking to the Gate~! 🧑‍💻🎶

[MIT License][license-url] © Nikaple

<!-- Variables -->

[discord-image]: https://img.shields.io/discord/758271814153011201?label=Developers%20Indonesia&logo=discord&style=flat-square
[discord-url]: https://discord.gg/njSj2Nq "Chat and discuss at Developers Indonesia"
[workflow-image]: https://img.shields.io/github/workflow/status/nikaple/library/%E2%9A%99%F0%9F%9A%80?label=CI%2FCD&logo=github-actions&style=flat-square
[workflow-url]: https://github.com/nikaple/library/actions "GitHub Actions"
[npm-image]: https://img.shields.io/npm/v/@nikaple/tsconfig?label=package&logo=npm&style=flat-square
[npm-url]: https://npmjs.org/package/@nikaple/tsconfig "@nikaple/tsconfig on NPM"
[license-url]: https://github.com/nikaple/library/blob/main/license "MIT License"
