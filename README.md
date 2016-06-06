# Node.JS template engines benchmark

## Engines

- [CoffeeKup](https://github.com/mauricemach/coffeekup) v0.3.1 ([website](http://coffeekup.org/))
- [doT](https://github.com/olado/doT) v1.0.1 ([website](http://olado.github.com/doT/))
- [Dust](https://github.com/linkedin/dustjs) v1.2.1 ([website](http://linkedin.github.com/dustjs/))
- [Eco](https://github.com/sstephenson/eco) v1.1.0-rc-3
- [ECT](https://github.com/baryshev/ect) v0.4.8 ([website](http://ectjs.com/))
- [EJS](https://github.com/visionmedia/ejs) v0.8.3
- [Fest](https://github.com/mailru/fest) v0.5.4
- [Gaikan](https://github.com/Deathspike/gaikan) v1.3.4
- [Handlebars.js](https://github.com/wycats/handlebars.js/) v1.0.9 ([website](http://handlebarsjs.com/))
- [Hogan.js](https://github.com/twitter/hogan.js) v2.0.0 ([website](http://twitter.github.com/hogan.js/))
- [Jade](https://github.com/visionmedia/jade) v0.28.1 ([website](http://jade-lang.com/))
- [Swig](https://github.com/paularmstrong/swig) v0.13.5
- [Underscore](https://github.com/documentcloud/underscore) v1.4.4 ([website](http://underscorejs.org/))

## Test environment

- CPU: Intel core i7-3632QM CPU @ 2.20GHz x 8, SSD 250G
- OS: 64-bit Ubuntu 16.04 LTS
- Node.JS version: v6.21

## Results

Rendering 100000 templates:

Gaikan
  Escaped   : 1514ms
  Unescaped : 60ms
  Total     : 1574ms

ECT
  Escaped   : 1437ms
  Unescaped : 96ms
  Total     : 1533ms

fTE.js
  Escaped   : 1414ms
  Unescaped : 79ms
  Total     : 1493ms

doT
  Escaped   : 2001ms
  Unescaped : 47ms
  Total     : 2048ms

Dust
  Escaped   : 1834ms
  Unescaped : 412ms
  Total     : 2246ms

Hogan.js
  Escaped   : 1746ms
  Unescaped : 328ms
  Total     : 2074ms

Fest
  Escaped   : 1641ms
  Unescaped : 249ms
  Total     : 1890ms

EJS without `with`
  Escaped   : 3764ms
  Unescaped : 644ms
  Total     : 4408ms

Swig
  Escaped   : 3767ms
  Unescaped : 282ms
  Total     : 4049ms

Underscore
  Escaped   : 2179ms
  Unescaped : 1270ms
  Total     : 3449ms

EJS
  Escaped   : 5825ms
  Unescaped : 2116ms
  Total     : 7941ms

Eco
  Escaped   : 4249ms
  Unescaped : 1123ms
  Total     : 5372ms

Handlebars.js
  Escaped   : 4485ms
  Unescaped : 2398ms
  Total     : 6883ms

Jade without `with`
  Escaped   : 6521ms
  Unescaped : 2594ms
  Total     : 9115ms

CoffeeKup
  Escaped   : 3147ms
  Unescaped : 6280ms
  Total     : 9427ms

Jade
  Escaped   : 15158ms
  Unescaped : 11153ms
  Total     : 26311ms

## Usage

	git clone git://github.com/baryshev/template-benchmark.git
	cd template-benchmark
	npm install
	node ./benchmark.js
