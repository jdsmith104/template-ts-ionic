# template-ts-ionic
Project used to standardise a template for my Ionic projects with a firebase backend
## Setup 
- ionic isntalled on command line
- yarn already installed
- Install boiler plate with types `ionic start demoApp blank --type=react typescript`
- Adding linter (prettier + esline) `yarn tidy`
- Add linting command (edit package.json) `yarn lint`
- Add unit tests (https://kulshekhar.github.io/ts-jest/docs/getting-started/installation)

## Debugging
- [Guide for VSCode](https://ionicframework.com/docs/troubleshooting/debugging)
- 'In the far-left vertical menu within VS Code, click on the run icon. If you are configuring this for the first time in your project, click on the option to create a launch.json file. Select Chrome from the environment options dropdown. This will automatically generate a launch.json file with configurations for launching Chrome against localhost.

Make sure that the **port used in the url property of your launch.json** file matches the port that you observed earlier when you ran ionic serve. Using an incorrect port number will not work.'

## Use
- Run server `ionic serve`

## Debugging
- Error 
````bash
[eslint] Plugin "react" was conflicted between ".eslintrc.json" and "BaseConfig » E:\Src\stop-procrastinating\front-end\node_modules\react-scripts\node_modules\eslint-config-react-app\base.js".
[react-scripts] webpack compiled with 1 error
````
- Solution
npm:
````
npm dedupe && npm i
````
yarn:
````
npx yarn-deduplicate && yarn
````
pnpm:
````
pnpm dlx pnpm-deduplicate && pnpm i
````
