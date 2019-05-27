### USGS Contour Maps Download and Modification Notes
 
-------------

To get maps, go to

https://viewer.nationalmap.gov/basic/?basemap=b1&category=ustopo&title=US%20Topo%20Download


Check the Map Indices box and select 7.5 minute.  Zoom in to the quadrangle you want.  Select the Draw Point tool (teardrop icon).  Click on the map you want.  In the left panel, click on Find Products.  Click “Download”.

These are large files (28 MB) in full (scalable vector) PDF format.  They take a long time to download, but be patient, and let Firefox and OSX do what then need to unpack the files.  When they are done, there will be a single PDF in Downloads which you keep, and other zip files you can trash.  the main reasons these files are so large is that they contain a layer holding a satellite bitmap picture exactly underlying the map drawings.

-----

Maps without an extensive gravel layer open directly and quickly (a few seconds) in AI, which strips out the raster images.  This is fine if you don’t need to edit the rivers or gravel.  If you do (for example, gravel as drawn frequently doesn’t match the satellite image), or if the gravel precludes opening in AI (there is no actual mis-coding, but the gravel coding is so inefficient that AI takes many minutes to open, and then takes impossibly long to do anything), you need to open the maps in Inkscape.  The Inkscape import dialog (which takes half a minute to appear) shows a thumbnail.  Leave Poppler unchecked, and the resolution set to the coarse default.  Press OK.  Wait a minute or two.

Once the drawing shows, add a layer above the current one.  Use the magnifier to zoom in to the extent that you can clearly distinguish raster images from any of the vector graphics.  Click the selector tool on pure raster where there you expect green forested image to be. A group of 2 objects should be selected.  Click delete.  The green overlay should disappear, and the remaining image look darker.  Again click on raster, and again delete to delete the shading layer.  (If you misdelete yourself, cmd-z restores.)  Now you should see pure image.  Click again, but this time choose Layers menu > Move selection to layer above.  The original layer will now contain just vector graphics.  Contrive to save the two layers as separate .pdf files.

Opening in AI and “saving as” strips out the underlying pic, and reduces the files from 28 to 5 MB.

Note that both AI and Inkscape convert layers in the original PDF to groups, all of which are loaded into a single layer.  If you have a disabling gravel layer, separate it out too in Inkscape.

Work with the (remaining) vector graphics .pdf in AI.

Note, if you are going to have to edit the rivers, and perhaps draw the gravel by hand, it helps a great deal to have the underlying satellite raster in place under the vector stuff so that you can trace over it.  This turns out to be easy in AI — use File menu > Place.  Do all your editing on the stripped version of the original quadrangle.  This obviates fiddling with alignments all the time.

Open the layers pane, and open up the top levels of the group hierarchy.  You can then Cmd-Click on individual features of the working map to select them without selecting the whole containing group (eg the main river itself), and the selected object will show a small rectangular mark on the right side of the pane.  If you click (Cmd-Click?) on that small mark, it will get bigger and all the stuff in its group will be selected.  You can check your work unchecking the visibility icon on the line.  Double click the object name to get an editing box, where you can change the name (say to "Rivers").

In this way, locate and rename all of the following:  Rivers, River names, Creeks, Creek Names, Highways and Small Roads and their names an numbers.  Also find and name the contours themselves and their numerical values, but make these invisible so that the map display is cleaner.  Actually, it is better to do this before the other steps in this paragraph.  Save As frequently.

You can adjust groupings (when allowed) by dragging and dropping in the pane.  Similarly, you can create new layers with the icon at the pane bottom, and distribute the named groups among the (new) layers.  Move the keeper groups in  keeper level(s?), and trash everything else.  Save.  Then Save As again, but this time selecting SVG as the output file type (non-compressed, use SVG fonts).

NOTE:  Because Inkscape does not have an equivalent object manager, manipulating the groups is much easier to do in AI.

After making a joint, stripped map, set the artboard to 11x17, lay out the appropriate number of individual map rectangles.  Then, one at a time, move the whole joint map so that a rectangle exactly overlies the art board.  Make a separate file copy for each.  Then, enlarging the eraser tool (double click on it), erase outside the artboard.  This will remove all line objects outside, leaving the text objects.  Then, using the white pointer tool, elastic box the text items and delete.  This process actually cuts the items at the artboard and throws away all outside drawing information, making the file much smaller.

