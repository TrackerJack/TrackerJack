#################
After Effects Panel Options
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

2. Create new nulls and or solids in your composition.
    .. image:: images/SelectItems.gif
        :alt: Add Pointcloud Name

3. Enter a name for the new point cloud (new null layers)
 
    .. image:: images/AEPanelAdd2.png
        :alt: Add Pointcloud Name

4. Choose which layers to export

   * Auto - will export any new layers since the last export
   
   * Selected - will export the layers manually selected in the timeline
    
    .. image:: images/AEPanelAdd3.png
        :alt: Add Pointcloud Name

5. Click the Export Additional button

    .. image:: images/AEPanelAdd4.png
        :alt: Export Additional Button
.. tip::
        You can continue to create additional null layers, name them, and then click Export Additional repeatedly if you want to create more named pointcloud layers before returning to Blender.

Info Tab
_________________

    .. image:: images/AEPanelInfo.png
        :alt: Info Tab

After exporting the JSON file the Info tab displays detailed information about your comp and project, which can be useful for troubleshooting any issues.


JSON Tab
_________________

    .. image:: images/AEPanelJSON.png
        :alt: JSON Tab

After exporting the JSON file the JSON tab displays the generated JSON data. You can copy and paste into a text editor or use the 'Save JSON File' button if the export didn't complete writing to a file. You can also edit the data in this box before saving.

Settings Tab
_________________

    .. image:: images/AEPanelSettings.png
        :alt: Info Tab

There are a few options to change the method of operation for TrackerJack in the Settings Panel.

1. JSON Save Location 
    .. image:: images/AESettingsSave.png
        :alt: Info Tab
You can change where the TrackerJack JSON file is saved. If you're on a team and need to save the JSON file locally this can be useful.

   * Default - will export to the same folder where your After Effects project is saved.
   
   * User Selection - After you click export you can choose where to save the JSON file.



