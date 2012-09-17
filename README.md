# Thap CSS Style

Thap CSS Style is a small, concise style guide for writing CSS that scales.  It contains the bare essentials: The rules, the reasoning and the sources.

The style guide takes inspiration a few sources, which it tries to credit.  These sources will provide more reasoning on the rule than this document contains.

## General

### Minimise the use of element selectors 

Selectors that contain elements tightly coupled the CSS to specific markup. It is not a safe assumption that the semantics of the content will never change so authors should prefer classes which exist independent of markup and create more flexible CSS.

Source: [SMACSS on modules](http://smacss.com/book/type-module)

### Do not use ID's in CSS Selectors

It is never safe to assume there will only ever be one of something on a page so do not use ID's for CSS.  Id's are much better used as javascript hooks so use them for this instead.

Source: [SMACSS on layout](http://smacss.com/book/type-layout)

### Animate an interface using classes not inline styles

Inline styles added by javascript are harder to update and maintain, prefer to add classes using javascript.  CSS3 transitions can then handle any animations and if CSS3 transitions are not supported the state will still be updated.

Source: [SMACSS on state](http://smacss.com/book/type-state)

### Selectors should be 4 or less levels deep

Long complex selector chains spawn specificity wars and are slower for the browser to evaluate.  Its unlikely you _need_ to use a selector more than 4 levels deep.  If it is, consider adding additional classes to the markup to enable a shorter  selector length.

### Don't use a Preprocessor to produce bloated CSS

A preprocessors features should never produce CSS that is longer than it would have been without the preprocessor.  That just sucks.

Source: [SMACSS on preprocessors (members only)](https://smacss.com/book/preprocessors)

### Minimise HTTP requests

HTTP Requests are expensive and slow the rendering of a page, so minimise them. Ideally a HTML page should contain just one CSS file with extra CSS being loaded as the page changes.

### Always Minimize CSS

Minifying code can save up to 60% on a files size.  Use a tool like [CodeKit](http://incident57.com/codekit/) to manage this and its easy-peasy.

Source: [Google Page Speed on Minifying CSS](https://developers.google.com/speed/docs/best-practices/payload#MinifyCSS)

### Use Single line formatting

CSS Architecture is more difficult to do well than it is difficult to understand CSS Properties.  Putting a declarations rules on one line allows easy scanning of class names and can put more code on one screen.  These factors combined make it easier to understand the overall architecture of a CSS file.

### Use dashes to separate words

CSS properties do not use underscores or camel case, they use dashes.  Do the same with classes 

## Cross Browser

### Use browser prefixes correctly & Painlessly
### Use Conditional classes for Internet Explorer
### Group IE Conditional classes with the code they alter

## Architecture

### Split CSS into Normalise, Layout, Module & Icon files
### Keep CSS files under 500 lines of code
### Order properties: box, border, background, text & other (smacss)

## Normalisation

### Normalise Don't Reset
### Don't be over-zealous when normalising

## Layout

### Separate Layout and Module rules
### Layout classes should be prefixed with l (smacss)

## Modules

### A Module should flexible width
### Comment a module thoroughly
### Ensure modules are self contained and reusable (smacss)
### Keep module names short 
### Module Specific Classes should be module name prefixed (smacss)
### Use a nested selector to group module rules
### Use immediate child selectors to contain modules (smacss)
### Split Modules into default, state, & subclass groups
### Subclass a module to create different module versions (smacss)
### Module Subclasses should follow the pattern: module--subclass
### Module Subclasses should be prefixed with the module class
### State classes should be prefixed with is (smacss)
### Only State rules may use !important (smacss)

## Icons

### Split icon styles into ico, ico-size & ico-img classes (smacss)
### Optimise icon images into sprites late in the project 
### Sprited Icons should be added to empty elements (smacss)
















