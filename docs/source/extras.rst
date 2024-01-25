#####################################
Bonus Features
#####################################

TrackerJack was designed to quickly import a 3D Camera Tracked Movie into Blender that could be scaled and aligned with ease. Allowing you to spend your time modeling and rendering. Since it's initial release more features have been added with the idea of saving time, and allowing you to quickly render quality scenes. 


Setup Compositor
_________________

Enabled by default in the Blender TrackerJack Import panel this creates a very simple Compositor setup so you're ready to render your created items with the background footage. Leaving this checkbox unchecked will skip this setup.

    .. image:: images/BPanelCompositor.png
        :alt: TrackerJack Import Compositior Setup
        



Eevee Shadow Catcher
_________________

    .. image:: images/Extra_ShadowCatcher.gif
        :alt: TrackerJack Import Eevee ShadowCatcher
        
This is a hidden feature. While shadow catchers are built into Cycles, Trackerjack can create a simple procedural shadowcatcher material for use with eevee.

#. Rename a tracked solid to "Shadow" in After Effects.
#. Export the JSON file with the TrackerJack After Effects Panel.
#. Import the JSON file with TrackerJack Import command.
#. The Shadow layer has been imported.
#. Model or extend the shadow plane as needed for your scene.
#. Go to the Shading Workspace and view the ShadowCatcher material.
#. Set the Viewport shading to Rendered.
#. Adjust the White slider in the Color Ramp node until you are satisfied with the result.


