# laravel-mix-react
Easy alternative Laravel Mix configuration for projects using React. Includes the babel loaders and Webpack configuration file
you need to get started.

## Installation
Run `npm install --dev laravel-mix-react`

In your project's `package.json`, update all references to `--config="node_modules/laravel-mix/setup/webpack.config.js"` 
within the "scripts" to point to `node_modules/laravel-mix-react/setup/webpack.config.js`.

Finally, add a `.babelrc` file in your project's root with the following lines: 

```
{
  "presets": ["react", "es2015", "stage-1"]
}
```

## Advanced configuration

If you need to make further changes to Webpack, run `cp node_modules/laravel-mix-react/setup/webpack.config.js ./` in your 
terminal. This will copy the modified `webpack.config.js` into the root of your project. Modify your config as needed, and then
remove the `--config="node_modules/laravel-mix-react/setup/webpack.config.js"` lines from your `package.json` file. 
