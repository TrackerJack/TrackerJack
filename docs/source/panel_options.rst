#################
Panel Options
#################


After Effects Panel
#################

Create Tab
_________________

|InstallAEPanel| the UI Panel and open After Effects if you haven't already.

Under the Create tab you have two options - Auto Export and Manual Export. 
 Auto Export is the default and easiest way to export your project data from After Effects to a JSON file that the Blender TrackerJack add-on will import. 
 Manual Export exists as a backup in case of the unlikely instance where Auto Export fails.

 .. image:: images/AEPanelCreate.png
      :alt: After Effects TrackerJack Panel
 
 .. |InstallAEPanel| raw:: html

      <a href="https://trackerjack-tutorial.readthedocs.io/en/latest/installation.html#after-effects-panel-install">Install</a>
      



Auto Export
_________________
1. Save your AE project file to a folder. This is the location where your JSON file will be saved. 
   You can also save to a custom file location (Settings > JSON Save Location > User Selection) 
2. Click the Auto Export Button.

     .. image:: images/AEAutoBut.png
        :alt: Auto Export Button


Manual Export
_________________
There are only two entries to make in order create the initial export of your tracked composition. The values for Focal Length and Angle of View boxes which can be copied from the Camera Settings panel.

1. Double click on the 3D Tracker Camera layer in the comp timeline.
2. Copy the Focal Length value.

     .. image:: images/AEManCam1.png
        :alt: Camera Settings Focal Length
        
3. Click Cancel to close the panel
4. Paste the value into the TrackerJack Focal Length box.

    .. image:: images/AEManPan1.png
        :alt: TrackerJack Focal Length


5. Double click on the 3D Tracker Camera layer in the comp timeline.
6. Copy the Angle of View value.


    .. image:: images/AEManCam2.png
        :alt: Camera Setting Angle of View

7. Click Cancel to close the panel
8. Paste the value into the TrackerJack Angle of View box.

    .. image:: images/AEManPan2.png
        :alt: TrackerJack Angle of View
        
9. Make sure that you have saved your After Effects file.
10. Click the Export button to create the JSON file. A dialog box with the JSON file location will confirm success.

    .. image:: images/AEManBut.png
        :alt: Manual Export Button

   The JSON file is named {Your Project File Name}_{The Comp Name}_TrackerJack.json. You can track one camera for each composition in your Project file.

.. tip::
        TrackerJack will export the JSON file for Blender to the same location where you've saved the After Effects Project File. When TrackerJack imports your footage into Blender, it first looks for the movie file wherever it was orginally located when imported into After Effects. If the file has moved, it will then look for it in the same folder as the JSON file. The simplist method to avoid issues is to keep your footage file, AE project file, and JSON file in the same folder.



Add Tab
_________________

    .. image:: images/AEPanelAdd.png
        :alt: TrackerJack Add Tab

Once you've created your scene in Blender and begun modeling, you may decide to return to After Effects to create additional nulls and solids in order to add detail in areas not previously added. The Add tab allows you to update the existing JSON file with new items added to your timeline after the inital export. Each time you click Export Additional the file is updated. 

1. Click the 'Select 3D Tracker Layer Button'. This is the shortcut to selecting the movie layer and the 3D Tracker Effect, which activates the track points for selection.


    .. image:: images/AEPanelAdd1.png
        :alt: Select Trackers button

2. Create new nulls and/or solids in your composition.
3. Enter a name for the new point cloud (new null layers)
 
    .. image:: images/AEPanelAdd2.png
        :alt: Add Pointcloud Name

#. Choose which layers to export

   * Auto - will export any new layers since the last export
   
   * Selected - will export the layers manually selected in the timeline

       .. image:: images/AE_8_tjpanel_add_options.png
        :alt: TrackerJack Add Tab Options

#. Click the Export Additional button

.. tip::
        You can continue to create additional null layers, name them, and then click Export Additional repeatedly if you want to create more named pointcloud layers before returning to Blender.
        
        
Blender Import Options Panel
#################

|InstallBIPanel| the Blender Add-on and open Blender if you haven't already.

 .. image:: images/BP_1_full_panel.png
    :alt: TrackerJack Blender Import Options
      
 .. |InstallBIPanel| raw:: html

       <a href="https://trackerjack-tutorial.readthedocs.io/en/latest/installation.html#blender-add-on-install">Install</a>


        
Import Settings
_________________

    .. image:: images/BP_2_import_settings.png
        :alt: TrackerJack Import Settings
 
 * 1. Import AE Scene - This is the default setting, to be used for the first import of a JSON file to set up your scene.
   
 * 2. Add Additional Tracked Items - Use this setting to update your scene with any with additional items you create in After Effects.
 
Point Cloud
_________________

    .. image:: images/BP_3_point_cloud.png
        :alt: TrackerJack Import Pointcloud
        
 The null layers in your After Effects file can be imported into Blender as vertices in a point cloud mesh, or as individual empty layers.
 
 * 1. Vertex - This is the default setting, it is the fastest to import, and ready for modeling.
   
 * 2. Empty - You may import each null as a Blender Empty, but it is considerably slower. May take several minutes.
 
Setup Compositor
_________________

    .. image:: images/BP_4_compositor_setup.png
        :alt: TrackerJack Import Compositior Setup
        
This setting is enabled by defaut. TrackerJack creates a very simple Compositor setup so you're ready to render your created items with the background footage. Leaving this checkbox unchecked will skip this setup.

Start Frame Adjust
_________________

    .. image:: images/BP_5_start_frame_adjust.png
        :alt: TrackerJack Import Frame Start
        
TrackerJack, by default, sets up the scene using the same start frame as your After Effects comp. However, depending on your source footage and workflow, the are times your After Effects comp might not start with frame 0. This results in your Blender scene being created later in your timeline. While you can change the start frame in the composition settings in After Effects before you export the JSON file with TrackerJack, you might find it easier to adjust where your footage begins in Blender by using this setting. 

* Enable - Click Enable to adjust the start frame
* Frame - Enter the Frame Number in Blender where the scene should start.
* Movie Only - Click Enable if you want to adjust the movie start independent of the tracked camera. (Uncommon for most uses)

 .. tip::
        After Effects compositions normally start at Frame 0, Blender timelines begin at Frame 1. TrackerJack adjusts all start frames from 0 to 1 automatically. However, if the After Effects composition begins after frame 1, TrackerJack makes no adjustment. (Unless you use the Frame Adjust option).
