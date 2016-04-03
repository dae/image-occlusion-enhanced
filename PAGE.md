*Image Occlusion 2.0 Enhanced* is an updated version of the [Image Occlusion 2.0](https://github.com/tmbb/image-occlusion-2) add-on for Anki with a number of improvements and new features.

## Table of Contents

<!-- MarkdownTOC -->

- [Screenshots](#screenshots)
- [Installation](#installation)
- [Customization](#customization)
    - [DOs and DO NOTs](#dos-and-do-nots)
- [Usage and Tips](#usage-and-tips)
    - [Making full use of SVG-Edit](#making-full-use-of-svg-edit)
    - [Using all available fields to their full extent](#using-all-available-fields-to-their-full-extent)
    - [Consistency across different note types](#consistency-across-different-note-types)
- [Changes](#changes)
- [Credits](#credits)
- [License and Warranty](#license-and-warranty)

<!-- /MarkdownTOC -->

**Overview of the Changes**

- new tabbed interface
- multi-line entry fields
- new buttons for adding notes
- advanced keyboard controls
- new "labels" layer for occluding custom labels
- new note type with more fields
- ability to customize field names
- ability to reuse existing i/o notes
- synchronization between image occlusion editor window and Anki's editor
- remember last used directory

...and many many other bug fixes and improvements. 

As you can probably tell, there have been some significant changes to how Image Occlusion behaves. With that in mind, I'd advise you give the [README on my GitHub repository](https://github.com/Glutanimate/image-occlusion-2-enhanced) a full read, as it elaborates on each of these changes and how they will affect your workflow.

## Screenshots

![Screenshot of the Masks Editor](https://github.com/Glutanimate/image-occlusion-2-enhanced/blob/master/screenshots/screenshot-io-editor-1.png?raw=true)

![Screenshot of the field entry tab](https://github.com/Glutanimate/image-occlusion-2-enhanced/blob/master/screenshots/screenshot-io-editor-2.png?raw=true)

![Screenshot of the reviewer](https://github.com/Glutanimate/image-occlusion-2-enhanced/blob/master/screenshots/screenshot-io-reviewer.png?raw=true)

**Development status**

While this add-on has gone through some testing on Linux and Windows by now, it's still in its early stages. If you use this add-on do not be surprised if you run into bugs, weird behaviour or other issues - especially if you're on OS X.

As always: Use this add-on at your own risk.

Bug reports and suggestions are always welcome, but it might take me a while to get to them. Please don't post them here, as I won't be able to help you or reply to them. Instead, either use the [Issues page](https://github.com/Glutanimate/image-occlusion-2-enhanced/issues) on GitHub or [this discussion](https://anki.tenderapp.com/discussions/add-ons/7049-revamped-version-of-image-occlusion-2-for-anki-beta-testers-wanted) on the Anki forums.

If you know how to code please feel free to improve this project, file pull requests, etc. The code could definitely benefit from some refactoring as I am not very adept in Python.

See [here](https://github.com/Glutanimate/image-occlusion-2-enhanced#known-issues-and-limitations) for a list of known issues.

## Installation

Simply go to []() and install *Image Occlusion 2.0 Enhanced* like you would with any other add-on. It doesn't matter if Image Occlusion 2.0 has been installed previously, as the installation will automatically overwrite any existing files.

## Customization

*Image Occlusion 2.0 Enhanced* can be customized, but only to a certain degree

### DOs and DO NOTs

**What you really should not do**:

- delete or rename the `Image Q/A - 2.0 Enhanced` note type
    + deleting the note type should restore it to default next time I/O is launched, but doing so will remove all notes associated with it
- re-order the fields of the note-type
- add new fields or remove existing ones
- rename the following fields: *Question*, *Answer*, *SVG*, *Original Image*

**What you can do**:

- rename the following fields: *Header*, *Footer*, *Remarks*, *Sources*, *TempField3*, *TempField4*, *TempField5*
- modify the card template and CSS
    + be careful, though: the right styling and layout is essential for layering the original image and SVG mask over each other

## Usage and Tips

Please check out tmbb's [comprehensive manual](http://tmbb.bitbucket.org/image-occlusion-2/) for a full tutorial on using image occlusion. Most of the instructions there still apply to this modified version of I/O.

What follows are a few additional tips to help you get the most out of *Image Occlusion 2.0 Enhanced*.

### Making full use of SVG-Edit

SVG-Edit ships with a lot of very useful **hotkeys**. Make sure to use them! E.g.:

- hold down <kbd>Shift</kbd> while clicking to select multiple shapes
- <kbd>G</kbd> to group items and mark them as one single mask
- <kbd>A</kbd> to select all items in the current layer
- <kbd>V</kbd> for the selection tool
- <kbd>R</kbd> for the rectangle tool
- <kbd>E</kbd> for the ellipse tool
- <kbd>T</kbd> for the text tool
- <kbd>C</kbd> to fit the image to the canvas
- <kbd>CTRL+Z/Y</kbd> to undo/redo
- <kbd>X</kbd> to show the layers side panel

Use the **layers dialog** to add labels to your images before occluding them. Here's how:

- click on the right-sided labels side pane in SVG-Edit; a panel with all active layers will appear
- select the *Labels* layer by left-clicking on it in the labels list
- anything you draw while this layer is active will appear above your picture, but below the occluding shapes
- when you want to draw the occlusion masks again, simply re-select the *Shapes* layer

**Other tricks**:

- add arrow heads to your lines: Draw a line using the line tool and select it. A drop-down box labeled "arrows" should appear in the top bar. Choose the arrow head you want or use the "markers" tool beside it for a larger variety of markers 

### Using all available fields to their full extent

This version of image occlusion comes with two new fields, *Remarks* and *Sources*. In total, you now have four different fields to choose from when adding additional information to your I/O notes (plus 3 more that are somewhat hidden, see above).

So what should you use these fields for? Well, you can customize and rename them however you please, but here are some suggestions:

- *Header* field: appears both on the front and back of your cards. I would use this for short titles that put your image in the right context. Notes in the browser can be sorted by this field, so make sure to choose a descriptive title.
- *Footer*: appears both on the front and back of your cards. You could use this for hints, mnemonics, recall prompts, etc.
- *Remarks* fields: Only appears on the back. Best suited for additional information, trivia, etc. Use this to nourish a big-picture understanding of the subject.
- *Sources*: Only appears on the back. Self-explanatory name. The best place to put references, links to your sources, lecturers etc. Very important if you ever want to go back and read up on the topic at hand.

### Consistency across different note types

Consider supplementing your other note types with a *Remarks* and a *Sources* field. Not only does it make for a more consistent experience, it also enables *Image Occlusion 2.0 Enhanced* to sync your sources between the I/O Editor and Anki's note editor. See [Enhancements to the core functionality of the add-on](#enhancements-to-the-core-functionality-of-the-add-on) for more information.

## Changes

New versions and changelogs will be posted on the [Releases page](https://github.com/Glutanimate/image-occlusion-2-enhanced/releases).

## Credits

- [tmbb](https://github.com/tmbb) for creating Image Occlusion
- [Abdolmadi Saravi, MD](https://bitbucket.org/amsaravi/) for patching Image Occlusion to reuse existing images in the media collection and on notes
- [Ank_U](https://bitbucket.org/Ank_U/) for patching Image Occlusion to support more fields

## License and Warranty

*Copyright © 2012-2015 tmbb*

*Copyright © 2016 Glutanimate*

*Image Occlusion 2.0 Enhanced* is licensed under the simplified BSD license.

Third-party open-source software shipped with *Image Occlusion 2.0 Enhanced*:

- [Python Imaging Library](http://www.pythonware.com/products/pil/) (PIL) 1.1.7. Copyright (c) 1997-2011 by Secret Labs AB, Copyright (c) 1995-2011 by Fredrik Lundh. Licensed under the [PIL license](http://www.pythonware.com/products/pil/license.htm)
 
- [SVG Edit](https://github.com/SVG-Edit/svgedit) 2.6. Copyright (c) 2009-2012 by SVG-edit authors. Licensed under the [MIT license](https://github.com/SVG-Edit/svgedit/blob/master/LICENSE)

- Python [ElementTree toolkit](http://effbot.org/zone/element-index.htm). Copyright (c) 1999-2008 by Fredrik Lundh. See header in `ElementTree.py` for licensing information.

All software in this repository is provided  "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. 