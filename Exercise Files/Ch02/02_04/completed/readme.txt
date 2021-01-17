
$ npm install webpack@3.1.0 --save-dev
$ npm install babel-core@6.25.0 --save-dev
$ npm install babel-loader@7.1.1 --save-dev
$ npm install babel-presets-env@1.6.0 --save-dev // transpile javascript above ES6 
var webpack = require('webpack');

module.exports = {
	entry: './script.js',
	output: {
		filename: 'bundle.js'
	},
	module: {
		rules: [
			{
			  test: /\.js?/, 
			  loader: 'babel-loader', 
			  exclude: /node_modules/,
			  query: {
			  	presets: ['env']   //create .babelrc
			  }
			}
		]
	}
};

//if webpack not running
package.json 
  "scripts": {
    "build": "./node_modules/.bin/webpack"
  },

$npm run build