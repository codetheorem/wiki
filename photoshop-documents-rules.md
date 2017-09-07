When using Photoshop to create a document that will present the user interface of a given  product based on the UX/UI Guideline some rules must be respected in order to create documents consistent with each other and compatible with our workflow and tools. Here’s the list:

**1) Creating a new photoshop document**

When creating a new document Photoshop proposes to choose among different formats: 
the one to choose is “Web” because it has “Art boards”,  choose a width of 1366x768 pixels @72 ppi, RGB.
In case the height of the document is not enough for a certain project it’s possible to increase it, but only on a specific artboard and not across the whole document.

**2) Artboards**

Each page will be displayed on a different Artboard. 
Artboards must always have a name, the more specific, the better. InVision and other software generate screens from artboards use the names from Photoshop so be careful how you name your Artboards (MORE INFO NEEDED).

**3) Layers**

Layers should always be named with the name of the description and the kind of object;
for example the logo on the top of the header should be called "top-right-logo-icon". 
Layers named like "layer 32" or "logo" should not exists.

The layers structure should reflect the actually format of the application.
For example the folder "heather" should be on the top and the folder "footer"on the bottom.

Hidden layer should exists only when a part of a document needed to be hidden, if I layer has not function should be deleted.



**4) Folders**

- Folders have to be always named.
- Each layer must always be put inside a folder. The folder should group objects inside the same conceptual area. For example, the folder “header” will contain all layers that contain objects that are inside the header area. 
- Inside the header folder, there will be subfolders that will group layers that compose an object. For example, the username and the icon next to it will be grouped in the same subfolder.
- Folders structure should reflect the actual HTML structure in this order:
-- Header
-- Section
-- Navbar(s)
-- Footer
-- Background
inside each folder there will be subfolders for each element contained in that folder.
EXAMPLE:
in the Header folder there will be a subfolder called "user menu" where will be placed the icon for the user and the text layer of the username. If, like in our current version, the user menu area activates dropdown menu on click, than another folder with the drop down menu elements will have to be created.

The subfolder structure should be organized creating first the element on top and, in case there are elements that are on the same height, first the one on the left.
EXAMPLE:
Assuming that in the section folder there is a title and a table you will find first the title, than the subfolder with the table. In the subfolder of the table there will be other subfolder and the elements on the left should be placed first. 


**5) Smart objects**

Certain elements like Header or Footer will repeat on every artboard, to facilitate the process and to be able to apply changes at once across all artboards use a “Smart Object”.
Therefore common elements will be converted into “Smart Objects” and inserted into a specific library in order for them to be replicated in a fast way, without error, and by automatically propagating changes across all artboards which use the Smart Object.

*this also means to be very careful with existing smart objects since they may affect not only the document you’re working on, but also other file(s) from other team members.*

**6) Naming convention**



**7) Libraries**

All the common elements will be stored in our Adobe shared library for a faster and consistent design. 
The elements are:
- Colors
- Logos
- Character styles
- Smart Objects
- Graphic objects
- Icons
All the elements that are in the library should be discussed and approved from the team first.

**8) Layers modification**

- Never rasterize a layer.
- when changing the color of a shape don't use the layer effects panel but change the actual color from the top panel

**9) Location of the file**

All files need to be stored in the Adobe Creative Cloud drive.

**10) Guides**
- Use only essential guides.
- Guides should reflect the Margins among elements.

**11) Space for experiment**
Make a folder that sits at the bottom of your layers panel and name it “Unused” pile” and throw all of your experimental groups and layers in there. Collaborators will know to ignore the folder and you can go back to it at any time if you decide to change your mind about a design.

**12) Lock element**
Element that are already discussed, approved and in his final design version should be locked to avoid mistakes. There could be the case where someone need to unlock to experiment something, that's ok, but always remember to lock it again.