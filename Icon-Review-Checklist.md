◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#designing-the-eos-project)


It is important that each icon pull-request is reviewed properly before merging. The checklist below can help you ensure that a given pull-request is ready to be merged.

Some icons might exhibit differences in line-thickness and padding(?). Every such case should be discussed with the submitter to determine whether an exception to the rule is warranted (#15). Exceptions are allowed but should stay in the minority or they are no longer exceptions but rather should become the rule.

1. Clone or download the pull-request branch in order to view the file locally. Do not view the icon in the browser!

1. Check that the name of the icon follows the [icon naming rules](https://gitlab.com/SUSE-UIUX/eos/wikis/Designing-and-compiling-svg-icons#naming-conventions-for-icons-files).

1. Check that the .ai source file is properly saved in the [correct repository] (https://gitlab.com/SUSE-UIUX/eos-backup). Open the .ai file to ensure that it is identical to the SVG file from the pull-request, except the ai. file has the grid in it.

1. Check if the icon fits the description of its purpose in the associated Trello card.

1. Check whether there are any existing material or Eos icons which use a similar visual metaphor.

1. Check that the icon is front-facing and fits with the other material and Eos icons.

1. Check whether icon forms and lines can be simplified. Ensure that negative space is optimally used.

1. Check that the canvas is 24p high and 24px wide and that there are 2 empty pixels on all sides of the icon.

1. Check that lines and shapes are aligned to the grid and, where applicable, the keyline shapes (the squares, rectangles, and circle visible in the grid).

1. Check that all or most-all lines are 2px in thickness. If any line is less than 2px thick it should only use geometric forms which other icons are based upon.

1. Check that all outer corners have a 2px radius. 

1. Check that line-ends are not rounded.

1. Check that none of the interior corners are rounded.

1. Check that the grid is not visible.

1. Discuss any exceptions to the rules above with the submitter in the pull-request itself.

1. Open index.html in the /dist folder to ensure that the font has been compiled correctly and that all icons are shown.