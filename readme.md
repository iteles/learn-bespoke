#Using Bespoke.js, a presentation micro-framework

##What is Bespoke.js?

##Why use it?

##How to use Bespoke.js

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
