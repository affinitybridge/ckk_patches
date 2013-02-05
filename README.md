ckk_patches
===========

This is collection of patches required by our Community Knowledge Keeper project at Affinity Bridge. These patch files are pretty specific this one project, however you might find something for your project too. 


async-zoomtolayer_7.x-2.0-beta1.patch
-------------------------------------
The zoom to layer feature in OpenLayers would only work with the KML layer type. This patch makes it work with any layer type with a URL property. The only asynchronous OpenLayers type provided is KML. We provided our own GeoJSON layer type so we needed to make these changes to work. 