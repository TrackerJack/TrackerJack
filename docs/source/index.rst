===================================
TrackerJack
===================================
Curent version - 2.0.0

What is TrackerJack?
---------------------------------
.. Insert animated gif here

Do you need to match move your footage for use in a 3D environent?

This is the fast and easy way to export |After Effects| 3d Camera tracked footage including cameras, nulls, and solids into |Blender| as tracked cameras with background footage, vector pointclouds, and planes. Including nulls and solids that have been animated in After Effects.

.. |After Effects| raw:: html

   <a href="https://www.adobe.com/products/aftereffects.html", target="_blank">After Effects</a>

.. |Blender| raw:: html

   <a href="https://www.blender.org", target="_blank">Blender</a>
---------------------------------
Why?
---------------------------------
Blender is a fantastic tool with many powerful features for 3D. While it contains a versatile 3d Tracker, it can be very cumbersome and time consuming while Adobe After Effects has a very fast and easy to use 3d Camera Tracker. TrackerJack leverages the power and speed of After Effects, so you can spend most of your time in Blender with modeling, animating, and rendering. 

---------------------------------
How?
---------------------------------
TrackerJack has 2 components - 
   * Adobe After Effects Panel to export the tracked data 
   * Blender Add-on to import the data into your Blender file. 
   
   #. Track your footage in After Effects. 
   #. Create nulls and solids as you desire to add details to your scene. 
   #. Add the Camera information to the TrackerJack Panel and export a JSON file with all of your tracked data.
   #. Use the TrackerJack Import in Blender to automatically create a matched scene with: 
   
      * All 3d camera details, animation, and background footage attached
      
      * Scene duration, Frame Rate, Color Settings
      
      * Tracked points imported as point clouds with editable vertices
      
      * Solids imported as Mesh Planes

      * Supports import of After Effects animated solids and nulls, importing either key frames or data for every frame (for matching complicated AE animations)
      
      * All imported items parented to a Empty named "World" for easy scaling and grid alignment.
      
      * Human Scale mesh created for use in scaling the scene.
      
      * Simple Compositor setup by default
      
      * Any Solid in your After Effects Timeline named "Shadow" will have a simple Eevee shadowcatcher shader node setup.

---------------------------------
Features
---------------------------------

* Uses After Effects Automated 3d Camera Tracking.
* One button Auto Export from After Effects.
* Faster results - spend more time modeling and animating instead of tracking.
* Longer and more complicated tracks.
* Easy to us scene alignment and real world scaling.
* Supports import of animated nulls and solids.
* One button correction of smartphone vertical footage.
* Speed shortcuts like background footage and composition node setup.
* Add additional pointclouds and layers after intital import.
* Easily adjust Keyframe interpolation
* Includes these bonus effects 
   * Eevee shadow catcher
   * Fake HDRI



---------------------------------
How to Purchase
---------------------------------
TrackerJack is exculsively available at |BlenderMarket.com|

Support creators by purchasing software directly.
Software piracy destroys the incentive necessary for a thriving community of innovation and creativity. 
Every purchase is a show of appreciation for the hard work and dedication necessary to develop even more amazing and useful tools for everyone.

.. |BlenderMarket.com| raw:: html

   <a href="https://blendermarket.com/products/trackerjack", target="_blank">BlenderMarket.com</a>


Technical Support
---------------------------------
If you have any issues please reach out for assistance at use the "Contact Creator" button at |Blender Market Contact Page|

Verified purchases thru Blender Market have access to customer support and free upgrades.

.. |Blender Market Contact Page| raw:: html

   <a href="https://blendermarket.com/creators/jim-elder", target="_blank">Blender Market Contact Page</a>

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   index
   installation
   quick_start
   panel_options
   Blender_panel_options
   extras
   
.. note::
   This project is under active development.
   

