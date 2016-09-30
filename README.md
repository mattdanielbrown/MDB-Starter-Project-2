MDB Project Starter Template
=========

A basic template I use as a starting point when beginning a new web project that contains SASS / SCSS files.

## File Structure

![File-Structure](https://raw.githubusercontent.com/mattdanielbrown/MDB-Starter-Project-2/master/img/FileStructure.png)

## Workflow Reminder

### *This setup is meant to allow the user to manipulate styles in the project by __only__ editing SCSS partials.*

All of the SCSS partials are combined inside the parent SCSS file, **main.scss** (including all of the files that aren't intened to be edited directly, i.e., partials in the _vendor_ directory), which will then be compiled into either **main.css**, or **main.min.css** (depending on which is specified in the SASS compilation). Whichever one is chosen is the final stylesheet that is referenced in the index.html file.

This setup and workflow is meant to help ensure there is only **one** stylehseet referenced in the index.html file.

While it's not life or death, it is best practice and Google reccomends it as part of their fundamental site optimization guide. Not to mention the fact that it helps readibility.

#### So, to summarize, the following files are *__intended__* to be edited directly:

* index.html
* _variables.scss
* _mixins.scss
* _layout.scss
* (and anything else inside the _partials_ directory)
* main.js

#### ... And the following files are *__Not__* *__intended__* to be edited directly:

* main.css / main.min.css
* jQuery.js
* modernizr.js
* _reset.scss
