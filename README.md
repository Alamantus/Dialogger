Dialogger
=========

[![Dialogger](http://i.imgur.com/KliEDM7.png)](http://i.imgur.com/KliEDM7.png)

Dialogger is a simple dialogue graph editor. It saves your dialogue graph in
two file formats:

- **.dl** - JSON file including all visual layout information
- **.json** - (when using "Export..." dialog) Optimized JSON, easier to parse in
    other systems.

It uses [Electron](http://electron.atom.io/) and [JointJS](http://www.jointjs.com/).

Read more about the rationale
[here](http://etodd.io/2014/05/16/the-poor-mans-dialogue-tree/).

Running
-------

Navigate to the project folder install the dependencies with NodeJS + NPM using:

```
npm install
```

After all the dependencies are installed (Electron is an included dependency),
just run it:

```
npm start
```

Usage
-----

Click and drag the grid to navigate around.

Right click on the grid to select the type of node to create:

- **Text** - Create a simple node for a string of text.
- **Choice** - Branch from a text node with multiple options.
- **Branch** - A switch/case list for previously set variables. Click the `+`
    to add more cases and the `-` to remove (from the bottom).
- **Set** - Name and set a variable.
- **Node** - Does nothing but behaves like Text. Best to just ignore it.

After creating a node, click and drag from the green semicircle of the node to
another node's red semicircle to connect them. You can change which node an
arrow is attached to by clicking and dragging the appropriate end of the
arrow.

Click the X anywhere you see it to delete the attached thing.

Building Releases
-----------------

You can build executable files for all major operating systems using:

```
npm run build
```

The files are output to `releases` when it's done.

You can also install to individual operating systems using the following:

```
npm run build-win
npm run build-lin
npm run build-mac
```

**NOTE:** This uses pretty old versions of everything, and for some reason `electron-packager@v7.4.0`
refuses to work with NodeJS versions in the double digits. Use a [Node Version Manager](https://npm.github.io/installation-setup-docs/installing/using-a-node-version-manager.html)
and use Node v8.x with this project.

**ALSO:**  If you're using MacOS to build Windows releases, reconsider. If you still
want to do it, you'll need to [install Wine](https://www.davidbaumgold.com/tutorials/wine-mac/)
and check out [this comment](https://github.com/electron/node-rcedit/issues/51#issuecomment-546234084)
for how to get the icon editor to work since MacOS Catalina and up don't have 32-bit capability.

### Why are the dependencies so out of date?

Because this project was originally just a fork of the original project to get it working
in Electron and nothing more. At this point, trying to update all the dependencies
and get everything working again with the new versions would simply not be worth the effort.

If you feel called to upgrade everything, feel free to fork and send a pull request my way.
I'll merge it as soon as I can if it works!

The MIT License
---------------

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
