# This is a guide to how we are designing and compiling the EOS-icons

### The repositories:

We use 2 different repositories when creating new icons:

1. The EOS-backup repo: it holds the original designs in .ai (illustrator extension). The folder where icons in .ai are being saved is: `design-system/EOS-Icons/`. The repository's URL is https://github.com/SUSE/eos-backup

2. The EOS-icons repo: it holds the final .svg icons as well as the compiled version of the icon font (with a nice demo page `dist/index.html`). Repo URL: https://gitlab.com/SUSE-UIUX/eos-icons

### Naming conventions for icons files:

The library used to compile the icon font requires some strict naming conventions:

- No `eos` prefix in the file name. The library will add a `.eos-icons` class for the usage of the icon in html. This class may be overridden by the developers using our iconic font, but this way it is compliant to Material Design Icons.

- No ` ` (spaces) or `-` (minus) to separate a more_than_one_word icon name. Use `_` (underscore) to separete them.

- No UPPERCASE_NAME.svg or Capitals_Either.svg. Use only lowercase_icon_names.svg

- Keep the file name as simple as possible, and as descriptive as possible. If the icon is a cloud, then call it cloud.svg

- When choosing a file name for the icon, always check that this icon name doesnt exist already in Material Icons: https://material.io/icons/. If it does, then it can be confusing when using EOS-icons together to Material Icons.

### Exporting SVG from Adobe Illustrator

- Use illustrator "Save as" or "Save as copy". Do not use "Export as" or "Export for screens"

- Select CSS Properties: "Style Attributes (Entity References)"

- Set the "Decimal Places" to 5

- Check the "Responsive" checkbox.

### Compiling the icon font:

All you have to do is:

1. Be at the project directory in your terminal `EOS-icons`
2. Run `grunt` to compile the fonts (follow the instructions in the readme.md file if this is the first time you run the compiler: https://gitlab.com/SUSE-UIUX/eos-icons/blob/version.1.0.0.WIP/README.md)
3. Check the dist/index.html to see the demo page `open dist/index.html`

### Creating a PR:

1. When creating a PR for the new icon designed, remember to always:
  - Be in **version.1.0.0.WIP** and Pull for the latest changes
  - Create a new branch from **version.1.0.0.WIP**
  - Add the new .svg icon into the `svg/` folder
  - Compile the icon font by running in the command line `grunt` (remember, you need to be inside the project directory for this to work)
  - Test that `dist/index.html` works well and you can see your icon there.
  - Create the commit by adding all the changes in `dist/` and your new icon in `svg/`
  - Push the changes and go to gitlab.com to create the Merge Request, which you will need to change the destination from **master** to **version.1.0.0.WIP**
  - Tell someone in the EOS Rocket Chat group to review your PR.

### Reviewing an icon PR:

First off, make sure that all the above has been followed. Secondarily:

1. Check that the SVG icon added to the `svg/` directory follows the guidelines present in: https://gitlab.com/SUSE-UIUX/eos/wikis/Icon-Review-Checklist
2. Check that the icon font compiled correctly by simply checking the `dist/index.html` file and that the new icon appears in there correctly. If it doesnt, it is most likely an issue with the file name or the SVG file itself.
3. Check that the new icon looks good in all the different sizes the `dist/index.html` demo page allows you to test. Other sizes are not required to be tested since those are the recommended sizes.