MDB Project Starter Template
=========

A basic template I use as a starting point when beginning a new web project that contains SASS / SCSS files.

## File Structure

![File-Structure](https://raw.githubusercontent.com/mattdanielbrown/MDB-Starter-Project-2/master/img/FileStructure.png)

## Workflow Reminder

### This setup is meant to allow the user to manipulate styles in the project by *__only__* editing SCSS partials.

All of the SCSS partials are combined inside the parent SCSS file, **main.scss**, which will then be compiled into **main.css**, or **main.min.css**.

Either **main.css** or **main.min.css** is the final stylesheet that is referenced in the index.html file.

###### So, to summarize, the following files are *__intended__* to be edited directly:

* index.html
* _variables.scss
* _mixins.scss
* _layout.scss
* (and anything else inside the _partials_ directory)
* main.js
