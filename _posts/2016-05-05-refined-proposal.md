---
layout: post
title: Current Feature List and the Timeline
category: article
author: Yash Agarwal
---

Eli, Dave and I decided to move forwards with an Activity for the Sugar Desktop (in Python) because it has many more users today than Sugarizer. 
Using Python allows me to take advantage of the libraries that [Trufont](https://github.com/trufont/trufont/) uses.

This font editor Activity is planned to include the following features and follow the [Sugar Human Interface Guidelines](https://wiki.sugarlabs.org/go/Human_Interface_Guidelines):

1. Font Manager. 

  1. Show all the available fonts found in the system font directory
  2. Allow the user to install/uninstall fonts,  make 'collections' within the library  

  <https://wiki.sugarlabs.org/go/The_Undiscoverable/Fonts>
  
  <http://wiki.laptop.org/go/Font_considerations>

2. A glyph drawing interface similar to the one found proposed by Mark Simonson and available in FontForge and Glyphs: edit several glyph outlines side by side, allowing to draw and space them in the same window.

  ![Image of Glyph Editing Interface](https://raw.githubusercontent.com/sugarlabs/font-editor-activity/gh-pages/files/img/1.png)

3. A Testing interface

  1. A textbox in which the text is rendered using the font, to get visual feedback. 

  2. Provide predefined text templates eg. "the quick brown fox jumps over the lazy dog," and 

  3. Export image button, to save an image of the rendered textbox

4. All this will be accompanied with thorough documentation, and...

  1. code commenting, which will be done hand in hand with development as we develope a better idea of the end goals        

### Timeline

I have divided the project into measurable Milestones :12 weeks, 40 hours a week. 6 milestones of 2 weeks each:

#### Milestone 1: Font Manager

Basic UI Boilerplate design

Will use the [Sugar Human Interface Guidelines](https://wiki.sugarlabs.org/go/Human_Interface_Guidelines) to build basic GUI functionality like Toolbar(s), Navbar , Work Space, etc.
The entire activity will be made as a Sugar Activity in Python

![Image of Activity Interface](https://raw.githubusercontent.com/sugarlabs/font-editor-activity/gh-pages/files/img/2.PNG)

1. Activate/Deactivate: Build an interactive grid display for showing all fonts in the system, a button to activate/deactivate them, and allow the user to create 'collections' within the library (like playlists in a music player) 

  1. Scan for .otf/.ttf type font files in the filesystem and add them to the library

2. Import/Export: open .ufo.zip files using python and defcon and export/generate .otf and .ttf files with fontmake

3. Complete documentation and organising code if needed according to sugar labs Activity Teams mentioned specification 

Mock:

![Image of Complete Font display](https://raw.githubusercontent.com/sugarlabs/font-editor-activity/gh-pages/files/img/3.png)

#### Milestone 2: Glyph Editor Basic Version

1. Build the glyph picker class, to select which glyphs to edit

2. Build the glyph class and the methods required for manipulating it 

3. Implement PostScript bezier outline editing feature which will be similar to the Glyph editor currently found in [Trufont](https://github.com/trufont/trufont/releases/tag/0.2.0)

![Image of Glyph Editing Interface](https://raw.githubusercontent.com/sugarlabs/font-editor-activity/gh-pages/files/img/4.png)

#### Milestone 3: Metrics Integrated Glyph Editing View

1. A view as mentioned above which allow us to adjust spacing while in glyph edit mode 

2. Testing Stage/Paragraph View

  1. This module will only show a text box in which the written text is rendered in the font currently being edited/created

  2. There will not be any editing option in this module- this is just to get a visual feedback of the font in question

  3. This module will also contain predefined text templates eg. "the quick brown fox jumps over the lazy dog"  and a export image button to save a image of the rendered font  

#### Milestone 4: Glyph Editor with Added Functionality 1

Implement spiro spline curve fitting as can be done with inkscape

#### Milestone 5: Glyph Editor with Added Functionality 2

Implement curve offsetting that will be used in skeleton based glyph design 

#### Milestone 6: Packaging

Get the code integrated in the main sugar distribution