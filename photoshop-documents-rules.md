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

- Folders have to be always named.
- Each layer must always be put inside a folder. The folder should group objects inside the same conceptual area. For example, the folder “header” will contain all layers that contain objects that are inside the header area.
- Inside the header folder, there will be subfolders that will group layers that compose an object. For example, the username and the icon next to it will be grouped in the same subfolder.


[I THINK WE NEED TO DESCRIBE THE HTML5 STRUCTURE FOR FOLDER BETTER. MAKE SURE EVERYONE UNDERSTAND THE BASIC HTML5 STRUCTURE WE NEED TO FOLLOW: HEADER, SECTION, NAV, AND FOOTER. INSIDE OF THOSE, WE NEED TO GROUP THE COMPONENTS IN FOLDERS AS WELL, USING THE EXAMPLE YOU GAVE OF THE USERNAME INSIDE THE HEADER. -- CYNTHIA]

**5) Smart objects**

Certain elements like Header or Footer will repeat on every artboard, to facilitate the process and to be able to apply changes at once across all artboards use a “Smart Object”.
Therefore common elements will be converted into “Smart Objects” and inserted into a specific library in order for them to be replicated in a fast way, without error, and by automatically propagating changes across all artboards which use the Smart Object.

*this also means to be very careful with existing smart objects since they may affect not only the document you’re working on, but also other file(s) from other team members.*

**6) Colors**

We will use colored labels on folders and layers to communicate a state of an element (folder or layer) using the following scheme:
RED = the element is already defined don’t change it.
GRAY = an experiment, just a test
GREEN = work in progress
YELLOW = ready for review
BLUE = just a place holder
VIOLET = need to be changed

[I DONT LIKE IT SO MUCH... RED IS DANGER, I THINK IT SHOULD BE GREEN THE DONE, AND RED THE WORK IN PROGRESS -- CYNTHIA]
[IN THE OTHER HAND, I DONT THINK WE NEED SOMETHING LIKE THIS, BECAUSE IN THE END WHEN WE FINISH A PSD FILE, EVERYTHING SHOULD BE DONE, AND THEN WE WOULD SEE THE PSD FILE FROM INSIDE, MEANING, HAVING THE STATE OF THE WORK IN PROGRESS INSIDE THE FILE WOULD MAKE IT COMPLICATED. THAT SHOULD BE TRACKED IN TRELLO IF SOMETHING IS NOT YET FINISHED. WHAT I WOULD RECOMMEND IS USING THIS GUIDE FOR COLORS: https://www.dtelepathy.com/blog/design/25-best-practices-collaborative-work-photoshop]

**7) Libraries**

All the common elements will be stored in our Adobe shared library for a faster and consistent design.
The elements are:
- Colors
- Logos
- Character styles
- Smart Objects
- Graphic objects
- Icons

[I LIKE THE PLAN, BUT WE NEED TO HAVE AN STRATEGY FOR THIS FIRST, WHICH IM MISSING HERE. FOR EXAMPLE, IF I MAKE SOMETHING, WOULD THAT MEAN I CAN JUST UPLOAD IT TO THE LIBRARY? NO!! WE CAN ONLY UPLOAD ITEMS TO THE LIBRARY WHEN THEY ARE DONE AND APPROVED. I WOULD REMOVE THIS RULE NOW BECAUSE IT WOULD ONLY ADD UNCERTAINTY. I WOULD SUGGEST THAT THE LIBRARY IS TAKEN CARE OF WHEN, AND UPDATED, ONCE WE MOVE CARDS TO DONE AND WE KNOW FOR SURE THAT THIS IS THE FINAL DESIGN AND THERE WILL BE NO RE-DESIGN OF THE PIECE -- CYNTHIA]

**8) Layers modification**

Never rasterize a layer and always chose effect in line with the possibilities the media, be it html5/css3 or static images.

[I HONESTLY DONT UNDERSTAND THIS RULE; I GET THAT WE DONT WANT TO RASTERIZE LAYERS, 100% AGREE WITH THAT ONE. BUT THE MENTION OF HTML5 AND MEDIA IS UNCLEAR TO ME -- CYNTHIA]

**9) Location of the file**

All files need to be stored in a location where all the team have easy access to. Invision allows you to upload the assets of a prototype.




[All in all, i think it is a good start, but we have to set more rigid rules. I would suggest following the guide I posted: https://www.dtelepathy.com/blog/design/25-best-practices-collaborative-work-photoshop, and check the screenshots (maybe just using those could be good). They have very easy to understand rules for collaboration and many rules that we can apply here as well.


Check in rule number 16 of the document I sent you, that rule is really important. Adding a layer style of type "color overlay" should be the lassst option always!, always replace the color of the vector layer -- cynthia]
