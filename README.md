# GNCTR Logo
The GNCTR logo (in vector format)

## Files
For each design, there are a few different files:

- The `*_inkscape.svg` files are inkscape SVG files.  These are the ones that should be actively worked on (if using inkscape)
- The `*_optimized.svg` files are the ones that should be used for most purposes (web, printing, embroidery, etc.)
- The `*_plain.svg` files are perhaps useful for active development in other programs than inkscape.  Probably not useful for much of anything.

## Versioning
This repo uses semantic versioning.
A commit with a tag (1.0.0) means that this is a version ready for use, and all three files mentioned above match each other and correspond to the same design.
Do not push a tagged release unless your commit includes a `plain` and `optimized` file that you JUST exported.

## Releasing
When you are ready to tag a release and export the `plain` and `simplified` files, please follow these steps:

1. `Save As` a copy of the inkscape file and make sure it is open (Don't commit this file)
2. Delete all unused layers in the file
3. Convert all text layers to a path by selecting the text object layer (make sure it is visible and unlocked) by clicking `Path` > `Object to Path` in the menu at the top
4. Ungroup all paths and layers
5. Combine paths that should be linked together using `Flatten`, `Combine`, `Differece`, and `Union` if you can
6. Click `File` > `Save a Copy`
7. Select `plain SVG`, and save it with the suffix `_plain.svg`
8. Repeat step 6, then select `Optimized SVG` and save it with the suffix `_optimized.svg`
9. Accept the default options
10. Add both those files and commit them along with your new inkscape SVG file.  (These can also be added in their own commit, provided they match the inkscape file)
11. Tag this release by running `git tag <release name>`
12. Push the commit!

