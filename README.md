# advice to road of storybook mastering

first advice

 go to  [site](https://www.learnstorybook.com/intro-to-storybook/)


# Getting Started with StoryBook in React

install storybook
```
npx -p @storybook/cli sb init
```

you don't need use that last command
 describe in  [docs](https://github.com/storybookjs/presets/tree/master/packages/preset-create-react-app)

only
````
npm install -D @storybook/preset-create-react-app
````
to specify the type of project 
```
npx -p @storybook/cli sb init --type react
```
run 
```
npm run storybook
```
## for use typeScript 
 
 describe in  [docs](https://storybook.js.org/docs/react/configure/typescript#gatsby-focus-wrapper)

the minimal config 
```
// .storybook/main.js

module.exports = {
  typescript: {
    check: false,
    checkOptions: {},
    reactDocgen: 'react-docgen-typescript',
    reactDocgenTypescriptOptions: {
      shouldExtractLiteralValuesFromEnum: true,
      propFilter: (prop) => (prop.parent ? !/node_modules/.test(prop.parent.fileName) : true),
    },
  },
};
```

----------- or -------------------

describe in  [docs](https://github.com/storybookjs/presets/tree/master/packages/preset-typescript)

install

````
npm install -D @storybook/preset-typescript ts-loader fork-ts-checker-webpack-plugin
````



## for use Scss
 
 describe in  [docs](https://github.com/storybookjs/presets/tree/master/packages/preset-scss)

 adding 
 ````
npm add -D @storybook/preset-scss css-loader sass-loader style-loader
```

the minimal config 
```
// .storybook/main.js

module.exports = {
  addons: ['@storybook/preset-scss'],
};
```
