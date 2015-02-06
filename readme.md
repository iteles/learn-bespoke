#Using Bespoke.js, a presentation micro-framework

##What is Bespoke.js?


##Why use it?

##Setting up Bespoke.js

###Using the Yeoman Generator
![smurf_sleepy](https://cloud.githubusercontent.com/assets/4185328/6004739/d98d407a-aafc-11e4-9521-c82fe8e51c97.jpg)
The _fastest_ (not specifically the best) way to set up a Bespoke.js presentation is to use [@markdalgleish](https://twitter.com/markdalgleish)'s [Bespoke.js Generator](https://github.com/markdalgleish/generator-bespoke).  

Assuming you have [Node.js](http://nodejs.org/) and [npm](http://blog.npmjs.org/post/85484771375/how-to-install-npm), you should then make sure you have [Bower](http://bower.io/) and [Gulp](http://gulpjs.com/):
`npm install -g bower`
`npm install -g gulp`

Then [install the Bespoke Generator](https://github.com/markdalgleish/generator-bespoke) following the instructions.

After you've run `yo bespoke`, the generator will take you through a number of questions to determine which base plugins you will need and then put together the main files for you.
![learn-bespoke-generator-screen](https://cloud.githubusercontent.com/assets/4185328/6004729/c48bc7be-aafc-11e4-9843-ffa7b599a3be.png)

At this point, you should be able to set up a local server to display your template presentation by typing `gulp serve` into your command line. If this doesn't work, try running `npm install && bower install` first before trying `gulp serve` again.

###From scratch (no generators)

##Using Bespoke.js after setup

####Changing themes
There are a number of different themes [available through npm](https://www.npmjs.com/browse/keyword/bespoke-theme). Let's choose to use the [Greeny theme](https://www.npmjs.com/package/bespoke-theme-greeny) for illustrative purposes.

1. Install the theme package using npm on the command line - make sure you're in the directory that you are building your presentation in.
```
npm install bespoke-theme-greeny
```
(remember to use `sudo` if you end up with permission issues in the installation)

2. In your `main.js` file, add the theme as a variable right at the top of the file after `bespoke`
```javascript
//this is where you require your Node.js modules
var bespoke = require('bespoke'),
       greeny = require('bespoke-theme-greeny'),
       //other modules here
```
_and also_ to the `bespoke.from` block:
```javascript
bespoke.from('article', [
      greeny.theme(),
      //other modules here
]);
```

**That should be it!** Run
```
gulp serve
```
to check - it should start up your presentation in a (debatably) pretty shade of green.
