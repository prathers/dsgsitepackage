# dsgsitepackage
TYPO3 sitepackage extension with https://github.com/daCyberpunk/dead-simple-grid and some basic configurations and content elements

## DEMO
https://www.roeder-webdesign.berlin

## What it does
* adds a simple flexbox grid CSS to your page
* Content Elements can have a flexbox basic width
* includes three gridelements using flexbox grid
* adds a field for sources/References to sys File Metadata, You can add the indication of source for your images there and use it in templates
* adds two Content Elements made only with TYPO3 Core functionality: ToTop Button and Cookie Consent Element
* does a lot of basic configurations in pageTS and TypoScript
* page Template gets a simple responsive menu with minimal JavaScript
* provides a ready to use configuration for cs_seo extension, means sitemaps, metadata etc, everything works fine out of the box I think
* adds a basic Backend Layout
* enables the ckeditor without making special configurations on it

### All written with
* -out usage of jQuery or any other framework
* BEM for my css as far as it wasnt provided from third party like the cookie consent.
* using sass for CSS and Browserify for JS (provided my gulp file)

> It's basically a work-in-progress extension even works already! That means it can be there some unused code, I let it there for later development, like the FileReference Model f.e.

### Why using it?
Basically I believe in content-driven-design. In a CMS World thats a difficult approach as we want the option that content changes.
If we design a page around a given content, then the design can be obsolete when content changes.
But I think we can find a way between the design-first and the content-first approaches. To say it with the perspective to TYPO3: Dont use Backend Layouts anymore, as they are fixing everything.
With flexible containers the editors can be enabled to adapt the layout of any page very individually to the content they add.
Now somebody can argue, that an editor shouldn't have the permission to change layouts and designs. But in my experience I would say: Say allready do every day.
If they set a special class for Content Element, a ruler before or even changing Backend Layouts...they always need to know what they are doing in context of frontend layout and design.
Now they need to know maybe a little bit more especially about flexible Elements, how the flex grid works. The job of a content editor isn't just to insert text and images anymore.


## Requirements

* TYPO3 8.7
* gridelements 8
* cs_seo
* realUrl (recommended)


## How Flexbox Grid is used
Each GridElement gets some flexform configurations. There is always one for the row and one for each column. There you make the basic configuration how the flexbox model should be used in Frontend.
> If you dont know what Flexbox is, you should read about first to understand the behavior of elements in Frontend. https://css-tricks.com/snippets/css/a-guide-to-flexbox/

Each Content Element can get a Flex Basis Size. If you pput it in a gridelement it gets it right flexbox behavior based on that size.

## Whats missing
Right now I do not know how to integrate the following features without overloading the grid and content element preferences for the editors.
But these points would make the usage of flexbox grids much more powerful:

* media queries for each flex option so it can be adapted by the editor to the different devices.
* flex-grow and flex-shrink

## You're free ...
* to contribute, fork, use as you want..
* to go in discussions with me about this approach
* to develop ideas for the "Whats Missing" part above


## credits
Most of the code I wrote by myself but still there are some pieces from other people. So credits to

* Benjamin Kott, I've re-used some of his bootstrap_package stuff like a viewhelper and Backend Layout Icons.
* https://cookieconsent.insites.com for ... cookieconsent. :-)
* TYPO3 Team and Community... you all are the reason I could do that!
