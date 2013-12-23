FormulaeView
============

The web technology framework behind the viewer in Formulae on iOS.

## Installation

To install the FormulaeView framework in an iOS application, download the zippped package from the GitHub main page. Unzip the package and insert the contents into a new folder called "FormulaeView" in the "Supporting Files" folder in the xCode project.

### System Files

```
core.html - this is the core of the framework (it displays an article)
viewbox.html - this is an extension of the framework (it only displays the first formula in an article)
/fonts - this directory contains fonts to be used in the framework
/mathjax - this directory contains the framework used for the displaying of mathematical equations
jquery.js - jQuery is an open source JavaScript framework which is used for efficiency purposes in FormulaeView
```

### Customisable Files

```
/articles - this directory will include all the articles
/images - this directory will contain all the images for the articles
/videos - this directory will contain all the videos for the articles
```

### Objective-C Implementation

The framework is simple to use. The different files have different purposes. The two files that can be used to display content are core.html and viewbox.html. A description on how these files can be utilised can be found below.

#### core.html
This file can be accessed through a webview. The webview can navigate to file at `FormulaeView/core.html`. For the file to display an article, the webview must navigate to the file at `FormulaeView/core.html?id=filepath` where `filepath` is replaced with the filepath (the id + the location) of the article. This filename does NOT include the `.xml` file extension. When the webview finishes loading, it will display the entire article saved at the location of `articles/[filepath].xml` in the FormulaeView folder.

#### viewbox.html
This file can be accessed in the same way as the core.html file and using the same id + location system. This file will display the first formula of the article saved at the location of `articles/[filepath].xml`. This will be useful for showing the preview equation of a particular article.

#### Examples
```
FormulaeView/core.html?id=Differential_Calculus/16285948294
```
When a webview navigates to the above address, it will display the article `16285948294.xml` in the `Differential_Calculus` directory inside the `articles` directory.

```
FormulaeView/viewbox.html?id=Differential_Calculus/16285948294
```
When a webview navigates to the above address, it will display the first formula in the article `16285948294.xml` in the `Differential_Calculus` directory inside the `articles` directory.
