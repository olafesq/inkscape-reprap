RepRap G-Code Output Plugin for Inkscape
===========================================

This is an Inkscape extension that allows you to save your Inkscape drawings as
G-Code files suitable for plotting with any RepRap printer. 

Modified by Olafesq. Added Bezier curve smoothness parameter.


Based on Unicorn plug-in from:

Author: [Marty McGuire](http://github.com/martymcguire)

Website: [http://github.com/martymcguire/inkscape-unicorn](http://github.com/martymcguire/inkscape-unicorn)

Credits
=======

* Marty McGuire pulled this all together into an Inkscape extension.
* [Inkscape](http://www.inkscape.org/) is an awesome open source vector graphics app.
* [Scribbles](https://github.com/makerbot/Makerbot/tree/master/Unicorn/Scribbles%20Scripts) is the original DXF-to-Unicorn Python script.
* [The Egg-Bot Driver for Inkscape](http://code.google.com/p/eggbotcode/) provided inspiration and good examples for working with Inkscape's extensions API.

Install
=======

Copy the contents of `src/` to your Inkscape `extensions/` folder.

Typical locations include:

* OS X - `/Applications/Inkscape.app/Contents/Resources/extensions`
* Linux - `/usr/share/inkscape/extensions`
* Windows - `C:\Program Files\Inkscape\share\extensions`

Usage
=====

* Size and locate your image appropriately:
	* Setting units to **mm** in Inkscape makes it easy to size your drawing.
	* The extension will automatically attempt to center everything.
* Convert all text to paths:
	* Select all text objects.
	* Choose **Path | Object to Path**.
* Save as G-Code:
	* **File | Save a Copy**.
	* Select **RepRap Plotter G-Code (\*.gcode)**.
	* Save your file.
* Preview
	* For OS X, [Pleasant3D](http://www.pleasantsoftware.com/developer/pleasant3d/index.shtml) is great for this.
	* For other [Repertier] (http://www.repetier.com/) is great.
* Print!
	* Open your `.gcode` file in your preferred printer management software.
	* Set up your printer and pen.
	* Center your build platform.
	* Start!

TODOs
=====

* Rename `*PolyLine` stuff to `*Path` to be less misleading.
* Formalize "home" to be a reasonable place to change pages/pens.
* Use native curve G-Codes instead of converting to paths?

