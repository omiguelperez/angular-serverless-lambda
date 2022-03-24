# App

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.29.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

## Deploying to AWS Lambda using Serverless Framework

Commands:

Init project with Angular CLI 8:

```shell
npx @angular/cli@8 ng new [app_name]
```

Installing dependencies:


```shell
yarn ng add @ng-toolkit/universal

yarn ng add @ng-toolkit/serverless

yarn add serverless-api-compression
```

Install serverless (if you don't have it installe yet)

```shell
npm i -g serverless
```

Configure AWS credentials:

```shell
aws configure
```

Finally, deploy it:

```shell
yarn build:serverless

sls deploy
```
## Don't forget 

Replace the express instance as:

```typescript
// Express server
export const app = express.default();
```

And, add that line to `serverless.yml` file:

```yml
package:
  exclude:
    # ...
    - '!node_modules/@vendia/**'
```