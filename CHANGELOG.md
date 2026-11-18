# Changelog

## Unreleased

- `pnpm run build` passes: `tsconfig.json` names the Node.js types,
  which TypeScript 6 no longer loads by itself
- Move the repository to the GitHub organization `cars-world` and
  rename the package to `@cars-world/cars-custom-master`
- Build the image into the registry `crcars`, tagged with the version
- Name the stages `dev`, `test` and `prod` in the README
- Add the hello world after the setup of `cars-master`: the HTTP server with `GET /`, `GET /api/hello` and `GET /health`, `start()` and the Dockerfile
