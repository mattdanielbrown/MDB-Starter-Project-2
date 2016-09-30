MDB Project Starter Template
=========

A basic template I use as a starting point when beginning a new web project that contains SASS / SCSS files.

## Installation

There is no 'installation' exactly - assuming you have npm and sass installed.

## Get the starter project

#### Either

1. Download directly as a zip, extract it and you're ready to go.  

  **Or**

2. Use __terminal__ to clone the repository.  

    1. in terminal, move to whatever directory you'd like the template to be downloaded into  
    2. run  
            `git clone https://github.com/mattdanielbrown.com/MDB-Starter-Project-2   `   
    3. move into in the _MDB-Starter-Project-2_ directory (run `cd MDB-Starter-Project-2`), and go nuts.

## Setup

The following are suggestions of what to do following downloading the project starter in order to get everything setup and ready for development.

  * Choose (or add) fonts via the *scss/vendor/_google-fonts.scss* partial (see [Fonts](https://github.com/mattdanielbrown/MDB-Starter-Project-2#fonts) below)
  * Edit the partials, *scss/partials/_variables.scss, -mixins.scss, and -layout.scss* to suit project's needs
  * Add partials to the *partials* directory
    * ...and update *scss/main.scss* (see [Adding Partials](https://github.com/mattdanielbrown/MDB-Starter-Project-2/blob/master/README.md#adding-partials) below)


## Fonts

This starter template attempts to provided an easy way to get up and running quickly and effeciently.

Thus, to handle fonts, there is a SCSS partial that offers a few of the most common typefaces on Google Fonts.

However, they are all disabled by default, as not doing so could severly impact perfomrance.

To select a font, there are 2 steps:

  1. Open *scss/vendor/_google-fonts.scss*, and either
    * uncomment the reference for the desired google font
    * add a google font reference for the desired font
  
  2. Open *scss/partials/_variables.scss*, and update the *base-font-family* varialbe to the new font.
  
#### Contents of the */scss/vendor/_google-fonts.scss* partial

```scss
// Google font references
// –––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––

// * NOTE:
//          - Choose carefully... These impact page performance...
//          - Also, even though all weights of each font are included,
//          - BE SURE TO SELECT ONLY A FEW of the chosen font.
//
//          - If desired font isn't included, import new fonts into this file.
//
//          - DON'T FORGET to go into ./scss/partials/_variables.scss
//          - and specify the new chosen font as the $base-font-family variable.

// Lato Font
//@import url(https://fonts.googleapis.com/css?family=Lato:100,300,400,700,900);

// Source Sans Pro Font
//@import url(https://fonts.googleapis.com/css?family=Source+Sans+Pro:200,300,400,600,700,900);

// Roboto Font
//@import url(https://fonts.googleapis.com/css?family=Roboto:400,100,300,500,700,900);

// Montserrat Font
//@import url(https://fonts.googleapis.com/css?family=Montserrat:400,700);
```

## Adding Partials


## File Structure

![File-Structure](https://raw.githubusercontent.com/mattdanielbrown/MDB-Starter-Project-2/master/img/FileStructure.png)

### Workflow Reminder

#### *This setup is meant to allow the user to manipulate styles in the project by __only__ editing SCSS partials.*

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
