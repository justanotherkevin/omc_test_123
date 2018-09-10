# making_emails

[more example](https://itnext.io/pug-js-to-make-your-life-easier-with-html-templates-9c62273626e0) here using gulp to create emails

modifying src/emails/index.pug will change the output file in dist/index which is served with npm; default at localhost:3000;

# npm build and watch

`npm run build`  
build complete HTML email template.  
compile sass (compileSass task) before running build

`npm run watch`  
watch source files for changes.  
run `build` task when anything inside `src` folder changes (except .css) and reload browserSync  
remove `'!src/**/*.css'` if you want to watch .css file changes in `/gulpfile.js` under `gulp.task('watch' ...`
