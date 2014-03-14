ckk_patches
===========

This is collection of patches required by our Community Knowledge Keeper project at Affinity Bridge. These patch files are pretty specific this one project, however you might find something for your project too.


async-zoomtolayer_7.x-2.0-beta1.patch
-------------------------------------
The zoom to layer feature in OpenLayers would only work with the KML layer type. This patch makes it work with any layer type with a URL property. The only asynchronous OpenLayers type provided is KML. We provided our own GeoJSON layer type so we needed to make these changes to work.


remove_pf_key.patch
------------------

CIS Species Migrate imports files from a source server. These files are private files at the source. Feeds does not have an authentication mechanism. So on the destination server, we use a feeds hook to add a key to the private file URI, and on the source server we check for that key in the file access hook, and pass it through if the key is good. This work but also creates a file on the destinatino server with the private file key in the filename. This patch removes that key before the file is saved, but after the file has been downloaded (ie. key no longer needed or wanted in the URI). Note this method will come in handy for any external accessing of private files, including FNFN species sync.


leaflet_051_fullscreen_fix.patch
--------------------------------

Fixes an issue described https://github.com/Leaflet/Leaflet/issues/1980. This fix is in Leaflet 0.7.
