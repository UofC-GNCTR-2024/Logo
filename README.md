# GNCTR Logo
The GNCTR logo (in vector format)

## Files
For each design, there are a few different files:

- The `*_inkscape.svg` files are inkscape SVG files.  These are the ones that should be actively worked on (if using inkscape)
- The `*_optimized.svg` files are the ones that should be used for most purposes (web, printing, embroidery, etc.)
- The `*_plain.svg` files are perhaps useful for active development in other programs than inkscape.  Probably not useful for much of anything.
- The `*.png` files are PNG exports that are 96 DPI or 500x500px.  These can be used for whatever.

## Versioning
A commit with a tag (v1.0.0) means that this is a version ready for use, and all three files mentioned above match each other and correspond to the same design.
Do not tag a release unless your commit includes a PNG and a `plain` and `optimized` file that you JUST exported.

This repo uses semantic versioning.

In this case, the first number is the major revision number and indicates which design version this is a release for.
The second number indicates a minor revision of a particular design.  This should be incremented for small tweaks.
The third number is the bug fix number.  This should be changed if a previous release has a small problem that needs to be fixed in the design or file.
This is something that should have been in the previous release but wasn't by mistake.

Here is an example of a possible series of releases in chronological order:
- v1.10.0
- v1.10.1
- v2.0.0
- v1.11.0
- v2.1.0

## Releasing
When your design is finished and ready to use, please follow these steps:

1. `Save As` a copy of the inkscape file and make sure it is open (Don't commit this file)
2. Delete all unused layers in the file
3. Convert all text layers to a path by selecting the text object layer (make sure it is visible and unlocked) by clicking `Path` > `Object to Path` in the menu at the top
4. Ungroup all paths and layers
5. Combine paths that should be linked together using `Flatten`, `Combine`, `Differece`, and `Union` if you can
6. Click `File` > `Save a Copy`
7. Select `plain SVG`, and save it with the suffix `_plain.svg`
8. Repeat step 6, then select `Optimized SVG` and save it with the suffix `_optimized.svg`
9. Accept the default options
10. Go to `File` > `Export`
11. On the right pane, select `Page`
12. Enter `96` into the DPI field
13. Set the filename as the project name without a suffix and select PNG as the file type, and click `Export`
14. Add both those files and commit them along with your new inkscape SVG file.  (These can also be added in their own commit, provided they match the inkscape file)
15. Push the commit
16. In GitHub, go to `Releases` and add a new release with notes about what changed and credits for who changed it
17. Include the same plain SVG, optimized SVG, and PNG files generated in the above steps
18. Set `Previous tag` to the last release with this major version and uncheck `Set as the latest release`

