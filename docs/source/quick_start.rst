#################
Quick Start
#################

|Video Link|

.. |Video Link| raw:: html

   <a href="https://youtu.be/btiEqsJ1q_E" target="_blank">Video Link</a>
   
After Effects
#################

#. Install After Effects Effects Panel

   \a)  |Install| TrackerJack_AE-2.00.jsxbin to your After Effects ScriptUI Panels folder and if you haven't already.  (After Effects > Scripts > ScriptUI Panels) 
   
   .. |Install| raw:: html

      <a href="https://trackerjack-tutorial.readthedocs.io/en/latest/installation.html#after-effects-panel-install">Install</a>
   


   \b)  Open After Effects, and launch the TrackerJack Panel via the Windows Menu (Windows > TrackerJack_AE-2.00.jsxbin)
   
   \c) Open After Effects Preferences and make sure that "Allow scripts to write files and access network" is enabled.

    .. image:: images/AE01-Install.gif
        :alt: Install AE Panel
        
#. Add footage and Track

   \a) Add footage and create a composition.
   
   \b) Use Effects > 3D Camera Tracker on the footage layer in your composition.

    .. image:: images/AE02-Import.gif
        :alt: Import and Track Footage
        
#. Select tracked points and create elements

   \a) Select points and right click to create Origin and Ground
   
   \b) Right click to create Solid and Camera.
   
   \c) Select additional points to create additional nulls and solids as desired.

    .. image:: images/AE03-AddItems.gif
        :alt: Add AE Items
        
#. Using the TrackerJack Panel

   \a) Enter the Camera information on the TrackerJack panel. Camera Settings units must be millimeters.
   
   \b) Save the After Effects file.
   
   \c) Click the Export JSON button on the TrackerJack Panel

    .. image:: images/AE04-Export.gif
        :alt: Export JSON

Troubleshooting

    .. image:: images/AE05-Troubleshooting.gif
        :alt: Export JSON
    .. tip::
        "Allow scripts to write files and access network" must be enabled in AE Preferences.
        
    TrackerJack requires that After Effects Application is in English Language. A universal language version of TrackerJack is being tested.

Blender
#################

#. |Install the Addon| if you haven't already

   .. |Install the Addon| raw:: html

      <a href="https://trackerjack-tutorial.readthedocs.io/en/latest/installation.html#after-effects-panel-install">Install the Addon</a>

   * Open Blender and |Install|.
   * Locate the TrackerJack zip file
   * Enable the check box to activate the add-on


   .. |Install| raw:: html

      <a href="https://trackerjack-tutorial.readthedocs.io/en/latest/installation.html#blender-panel-install">Install</a>

    .. image:: images/BL00-Install.gif
        :alt: Install Blender Add-on

#. Import the JSON data into Blender

   * Press 'a' to select all, then press 'x' and click the *Delete* button to clear the default elements.
   * Go to the File menu and select *TrackerJack AE Tracking Data (.json)* listed by selecting the import command.
   * Locate and select the JSON file exported from After Effects. (Adjust settings of panel or use default settings)

    .. image:: images/BL01-Import.gif
        :alt: Import JSON data
        
#. Scale and Rotate the World

   * Press '0' to switch to the Camera view, or go to *View* -> *Cameras* -> *Active Camera*.
   * Press Spacebar to play the timeline (Advancing frames)
     will update the scene if your pointclould doesn't seem to be aligned.
   * Select the "World" empty in the Scene Outiner
   * Press 's' and adjust the scale so the "Human Scale" mesh matches the scale for your scene.
   * Press 'r' then 'z' and adjust the z rotation so the grid matches your scene.

    .. image:: images/BL02-ScaleandRotate.gif
        :alt: Scale and Rotate the World


Adding Additional Items
#################

Once you begin modeling your scene in Blender, you may require addtional pointclouds or planes to build out your scene. It is easy to go back to After Effects and create additional layers, ammend the orginal JSON file, and import them into your Blender scene while maintaining the world scale and rotation you have already set.

#. Adding Additional Items - After Effects 

   * In After Effects you set the frame to the frame number in Blender to see the same footage
   * Select additional tracking points and create additional solids as desired.
   * Select the "Add" tab in the TrackerJack Panel
   * Create a name for the new pointcloud, and click *Export*
   
    .. image:: images/BL03-AdditionalItemsAE.gif
        :alt: Scale and Rotate the World

#. Adding Additional Items - Blender

   * Go to the File menu and select *TrackerJack AE Tracking Data (.json)* listed by selecting the import command.
   * In the options panel (press 'n' if necessary) select *Option 2 Add Additional Items*
   * Click the *Import* button
   
    .. image:: images/BL04-AdditionalItemsBlender.gif
        :alt: Scale and Rotate the World
