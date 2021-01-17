$ npm init
$ sudo npm install -g webpack 
$ npm install --save-dev babel-loader - process es6 to es5
Create webpack.config.js 
module.exports = {
	entry: './<entryfilename>.js',
	output: {filename: '<outputfilename>.js'},
	module: {
		loaders: [
			{test: /\.js?/, loader: 'babel-loader', exclude: /node_modules/}  //test looks for js 
		]
	}
};
$ webpack 

$ npm install webpack@1.12.2 --save-dev
$ npm install babel-core@5.8.29 --save-dev
$ npm install babel-loader@5.3.2 --save-dev

