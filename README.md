# Typescript-Express-GCP_Serverless-Starter

A boilerplate for using Express with Typescript for GCP serverless functions.

## Getting started

First run `npm install`

- To run the function locally, set the name of the function you want to test in `package.json` ->
  `functionVars` -> `localFunc`
- To run the function locally, run `npm start`
- To deploy a function, run `npm run-script deploy_helloWorldHTTP`. Make sure
  gcloud CLI is set up to the correct project.

## Testing

- Run `npm test` to run unit and integration tests
- Run `npm run-script test:system` to test live functions. Make sure to create a
  .env file in the root and add your GCP url like so: `GCP_SERVERLESS_URL=https://us-central1-<appID>.cloudfunctions.net`

## Tsconfig files

There are multiple tsconfig files, all of which extend `tsconfig.json` as the base configuration. The `tslint` extension (see below) only looks for `tsconfig.json` (as of the time of writting this there is no config option to change that), so all of the linting is done based off of what is in `tsconfig.json`.

## Dev Tooling

The following is a list of optional dev tooling that I included to help my workflow:

- TSLint: A linter for Typescript. My linting settings are checked into the repo under `tslint.json`. (Can either be run with `npm run lint` or use the VSCode extention for in editior linting)
- Prettier: A formatter to autostyle my code. You need the `prettier` VSCode extention. Prettier uses `.prettierrc.json` to set autoformatting style. Make sure your prettier seetings match your tslint settings, for example, `tslint.json` is set up to never allow semicolons unless necessary, so my `.prettierrc.json` auto removes semicolons unless necessary.
