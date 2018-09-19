# making_emails

[more example](https://itnext.io/pug-js-to-make-your-life-easier-with-html-templates-9c62273626e0) here using [gulp](https://gulpjs.com/) to create emails  
[reference](https://templates.mailchimp.com/resources/email-client-css-support/) to what is **not supported** across different browsers  

modifying src/emails/index.pug will change the output file in dist/index which is served with npm; default at localhost:3000;

# npm build and watch

`npm run build`  
build complete HTML email template.  
compile sass (compileSass task) before running build

`npm run watch`  
watch source files for changes.  
run `build` task when anything inside `src` folder changes (except .css) and reload browserSync  
remove `'!src/**/*.css'` if you want to watch .css file changes in `/gulpfile.js` under `gulp.task('watch' ...`

# notes 
building email is challenging, there are limitations. 
To start you can only use `<table>`. Since modern web development have faded away from this practice, this might the first time you have used it (true for me).
If you have taken a look at **not supported** link above you can see that theres only a hand full of css you can use if you want the template to work across different email platform. 