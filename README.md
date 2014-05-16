kit.sugar
=========

Add html syntax highlighting for [CodeKit's](http://incident57.com/codekit/index.html "CodeKit, the coolest app for web developers") .kit files in [Espresso.app](http://macrabbit.com/espresso/ "Espresso, the web editor").

Espresso automatically detects html syntax for .kit files when they have an opening `<html>` tag, but it does not for partials (ie. when `<html>` is not declared). This sugar solves the issue.

~~In the future I might add more functionality such as .kit statements detection and coloring (`@import`, `$variables`, etc), but not for now.~~

## Update: Syntax highlighting has come!
Now Espresso will recognize and color the following .kit statements:

- `@import` or `@include`
- variables in both in the `@` and in the `$` form, but not in the simple string form, so: `@variable` and `$variable` will be colored, but not `variable` (all three are valid .kit variables)
- and most importantly, comments `<!-- -->`

This sugar makes working with **.kit files in Espresso** a real pleasure. Up until now I had this terrible experience of trying to train my eye not to ignore code comments, which was driving me crazy. Now they are highlighted and beautiful.

I am still investigating an issue with the placeholder theme colors being inverted in some circumstances.

Here is a preview image:

![The CodeKit syntax highlighting for Espresso](http://gsv-general.s3.amazonaws.com/kit-espresso-syntax.png)


Please note that since CodeKit syntax is written inside html comment blocks, this sugar will also color standard html comment blocks that you might have in your .kit files (not in .html files, though). This behavior might be changed in the future. I still have to investigate if it is feasible.

Feel free to fork and contribute to this if you feel like it.

Hope you like this. I sure do.

(If you are wondering what theme I am using in Espresso, it is my personal fork of Railcasts, I will be adding it to my github profile soon)

## Instalation

1. Download and extract zip if the browser doesn't do this for you
2. Rename folder kit.sugar
3. Double click the .sugar file
4. Restart Espresso - magic!
