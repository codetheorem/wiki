When using Photoshop to create a document that will present the user interface of a given  product based on the UX/UI Guideline some rules must be respected in order to create documents consistent with each other and compatible with our workflow and tools. Here’s the list:

**1) Creating a new photoshop document**

When creating a new document Photoshop proposes to choose among different formats: 
the one to choose is “Web” because it has “Art boards”,  choose a width of 1366x768 pixels @72 ppi, RGB.
In case the height of the document is not enough for a certain project it’s possible to increase it, but only on a specific artboard and not across the whole document.

**2) Artboards**

Each page will be displayed on a different Artboard. 
Artboards must always have a name, the more specific, the better. InVision and other software generate screens from artboards use the names from Photoshop so be careful how you name your Artboards (MORE INFO NEEDED).

[CAN YOU GIVE AN EXAMPLE OF GOOD NAMING, AND ONE OF BAD NAMING? -- cynthia]

**3) Layers**

Layers should always be named with the name of the description and the kind of object;
for example “home Icon”

**4) Folders**

- Each layers must always be put inside a folder. The folder should group objects inside the same conceptual area. For example the folder “header” will contain all layers that contain objects that are inside the header area. 
- Inside the header folder there will be subfolders that will group layers that compose an  object. For example the username and the icon next to it will be grouped in the same subfolder.
- Folders have to be always named.

**5) Smart objects**

Certain elements like Header or Footer will repeat on every artboard, to facilitate the process and to be able to apply changes at once across all artboards use a “Smart Object”.
Therefore common elements will be converted in “Smart Object” and inserted into a specific library  in order for them to be replicated in a fast way, without error, and by automatically propagating changes across all artboards which use the Smart Object.

*this also means to be very careful with existing smart objects since they may affect not only the document you’re working on, but also other file(s) from other team members.*

**6) Colors**

We will use color labels on folders and layers to communicate a state of an element ( folder or layer )using the following scheme:
RED = the element is already defined don’t change it.
GRAY = an experiment, just a test
GREEN = work in progress
YELLOW = ready for review
BLUE = just a place holder
VIOLET = need to be changed

**7) Libraries**

All the common elements will be stored in our Adobe shared library for a faster and consistant design. 
The elements are:
- Colors
- Logos
- Character styles
- Smart Objects
- Graphic objects
- Icons

**8) Layers modification**

Never rasterize a layer and always chose effect in line with the possibilities the media, be it html5/css3 or static images. 

**9) Location of the file**

All files need to be stored in a location where all the team have easy access to. Invision allows you to upload the assets of a prototype.




