◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#designing-the-eos-project)


When using Photoshop to create a document that will present the user interface of a given product based on the UX/UI Guideline some rules must be respected in order to create documents consistent with each other and compatible with our workflow and tools. Here’s the list:

## Creating a new photoshop document

![1](/uploads/9f541badea61da5914fc09391a9f710a/1.png)
When creating a new document Photoshop proposes to choose among different formats: 
the one to choose is “Web” because it has “Artboards”,  choose a width of 1366x768 pixels @72 ppi, RGB.
In case the height of the document is not enough for a certain project it’s possible to increase it, but only on a specific artboard and not across the whole document.

## Artboards
![Screen_Shot_2017-09-25_at_17.01.42](/uploads/dbe15db7623929b8f2ad0d4a4f0d5195/Screen_Shot_2017-09-25_at_17.01.42.png)
Elements of the user interface that occupy most of the frames will be displayed in artboards, that includes navbars, modals, header etc...
Each element's status will be displayed on a different Artboard and artboards will be named with the name of the element and his status

## Layers






![Screen_Shot_2017-09-25_at_17.28.02](/uploads/40a0bba659321449f7872449b9ea1f5f/Screen_Shot_2017-09-25_at_17.28.02.png)





We will follow the rules describer in this webpage: http://photoshopetiquette.com/layers/
plus:
Layers should always be named with the name of the description and the kind of object;

The layers structure should reflect the actual format of the application.
The layers on top and those on the left should be first.

The hidden layer should exist only when a part of a document needed to be hidden. If a layer doesn't have a function should be deleted.



## Folders




![Screen_Shot_2017-09-29_at_11.42.22](/uploads/28e159a70bb827b9e1a7315594ec66d0/Screen_Shot_2017-09-29_at_11.42.22.png)







- Folders have to be always named.
- The folder should group objects inside the same conceptual area. For example, the folder “header” will contain all layers that contain objects that are inside the header area. 
- Inside the header folder, there will be subfolders that will group layers that compose an object. For example, the username and the icon next to it will be grouped in the same subfolder.
inside each folder, there will be subfolders for each element contained in that folder.

EXAMPLE:
In the Header folder there will be a subfolder called "user menu" where will be placed the icon for the user and the text layer of the username. If, like in our current version, the user menu area activates dropdown menu on click, then another folder with the drop-down menu elements will have to be created.

The subfolder structure should be organized creating first the element on top and, in case there are elements that are on the same height, first the one on the left.
EXAMPLE:
Assuming that in the section folder there is a title and a table you will find first the title, then the subfolder with the table. In the subfolder of the table, there will be other subfolder and the elements on the left should be placed first. 


## Smart objects





![5](/uploads/0665d33acb1be19aa029dcfc15e9eba2/5.png)





Certain elements like Header or call-to-action button will repeat on every document, to facilitate the process and to be able to apply changes at once across all artboards use a “Smart Object”.
Therefore common elements will be converted into “Smart Objects” and inserted into a specific library in order for them to be replicated in a fast way, without error, and by automatically propagating changes across all artboards which use the Smart Object.

*This also means to be very careful with existing smart objects since they may affect not only the document you’re working on but also other file(s) from other team members.*



## Libraries





![Screen_Shot_2017-09-21_at_09.35.04](/uploads/df272820971acbe1eb4334436fc03c5c/Screen_Shot_2017-09-21_at_09.35.04.png)





All the common elements will be stored in our Adobe shared library for faster and consistent design. 
The elements are:
- Colors
- Logos
- Character styles
- Smart Objects
- Graphic objects
- Icons

All the elements that are in the library should be discussed and approved from the team first.

## Layers modification

- Never rasterize a layer.
- when changing the color of a shape don't use the layer effects panel but change the actual color from the top panel



## Guides




![Screen_Shot_2017-09-21_at_09.47.20](/uploads/8e9a53cd1f37371f3e0c31c7ed05558f/Screen_Shot_2017-09-21_at_09.47.20.png)






- Use only essential guides.
- Guides should reflect the Margins among elements.

## Space for experimenting





![Screen_Shot_2017-09-21_at_09.40.30](/uploads/b25f01508eec57ba74e0798a5f4946bd/Screen_Shot_2017-09-21_at_09.40.30.png)





Make a folder that sits at the bottom of your layers panel and name it “Unused” pile” and throw all of your experimental groups and layers in there. Collaborators will know to ignore the folder and you can go back to it at any time if you decide to change your mind about the design.

## Lock element





![Screen_Shot_2017-09-21_at_09.41.23](/uploads/a12083d01838ef0164b6d16ea3b53bf9/Screen_Shot_2017-09-21_at_09.41.23.png)





Elements that have already been discussed, approved and in his final design version should be locked to avoid mistakes. There could be the case where someone need to unlock to experiment something, that's ok, but always remember to lock it again.