#####################################
Bonus Features
#####################################

Speed and Ease of use
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TrackerJack was designed to quickly import a 3D Camera Tracked Movie into Blender that could be scaled and aligned with ease. Allowing you to spend your time modeling and rendering. Since it's initial release more features have been added with the idea of saving time, and allowing you to quickly render quality scenes. 

Fexible workflow
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
One important feature that was part of TrackerJack's design from the start is the ability, to track and export from After Effects, import and work in Blender. Then if you decide that more tracker points or solids are needed to be able to go back to After Effects, create more layers and update the existing Blender scene without having to start over.

Animated Layers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Begining with TrackerJack 2.0 - animated nulls and solids are transferred with their position and orientation animation intact. You can motion track a object in your movie, attact the tracker to a null and have it brought into your 3D Blender scene and to replace with a 3D model.

.. tip::
        TrackerJack does not work with layer animation that is based on expressions, it must be keyframed. If you have a layer that uses expressions for position, orientation, or rotation make sure to select the layer then use the After Effects command *Animation > Keyframe Assitant > Convert Expression to Keyframes* to convert the layer before exporting with TrackerJack. 

            .. image:: images/AEExpressionAnimation.png
                :alt: Expression Animation
        
            .. image:: images/AEKeyframeAnimation.png
                :alt: Keyframe Animation

Setup Compositor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Enabled by default in the Blender TrackerJack Import panel this creates a very simple Compositor setup so you're ready to render your created items with the background footage. Leaving this checkbox unchecked will skip this setup.

    .. image:: images/BPanelCompositor.png
        :alt: TrackerJack Import Compositior Setup
        

Eevee Shadow Catcher
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The **Eevee Shadow Catcher** is a bonus feature. There are two ways to use it. 

• Any solid layer that you rename "Shadow" in After Effects before exporting, will automatically have the "ShadowCatcher" material appplied to the layer when it is imported into Blender.

• Select a mesh layer in your scene. In Object mode click the **Add Eevee Shadow Catcher** button. The "ShadowCatcher" material will be appplied.

The "ShadowCatcher" material may require adjusting the **Color Ramp** and **Subtract** nodes in the **Shader Editor** in order to match your scene. 

        .. image:: images/BlenderShadowCatcherAdjust.png
            :alt: ShadowCatcher Adjust

.. tip::
        See the Eevee Shadow Catcher chapter in the quick start video |here|.
    
        .. |here| raw:: html
        
           <a href="https://youtu.be/btiEqsJ1q_E&t=677" target="_blank">here</a>


Vertical Video Correction
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TrackerJack Supports the import and use of vertical or portrait orientation video. However some footage (primarily taken on smartphones) is recorded in horizontal orientation and encoded with a 90˚ rotation in the metadata. After Effects reads this and automatically interprets the footage as vertical, Blender does not. After you **Import Scene** with vertical video with this issue, when you Press '0' to switch to the Camera view, or go to View -> Cameras -> Active Camera and press spacebar to play the timeline and update the scene, you will notice a problem with the background video.

• Click the **Vertical Video Correction** button and the video will automatically be rotated to match your scene.

        .. image:: images/BlenderVerticalVideo.gif
            :alt: Vertical Video Button

Set KeyFrame Interpolation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you import After Effects layers that have postion and orientation key frame animation, TrackerJack automatically uses Linear interpolation for those key frames. 

• You can change this to any other interpolation that Blender supports by selecting the layer then clicking the **Set Keyframe Interpolation** button. 

        
        .. image:: images/BlenderKeyFrameInterpolation.png
            :alt: Interpolation 1


• A pop up menu will appear and you can apply the new interpolation mode.


        .. image:: images/BlenderKeyFrameInterpolation2.png
            :alt: Interpolation options


 .. tip::
        When using easing or any complex animation in After Effects, it's better to use the **Bake All Frames** option in the |After Effects TrackerJack Settings Panel| to create keys for every frame of animation. 

.. |After Effects TrackerJack Settings Panel| raw:: html

       <a href="https://trackerjack-tutorial.readthedocs.io/en/latest/panel_options.rst#frame-export-drop-down-choice">After Effects TrackerJack Settings Panel</a>

Reset Scene Button
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sometimes, you may import a scene, then decide to make changes such as **Adjust Start Frame** the **Reset Scene - Delete Everything** button is a quick way of deleting all items in the scene and any orphaned data.

        .. image:: images/BPanelResetScene.png
            :alt: Reset Scene Button


Start Frame Adjust
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

TrackerJack by default sets up the scene using the same start frame as your After Effects comp. However, depending on your source footage and workflow, the are times your After Effects comp might not start with frame 0. This results in your Blender scene being created later in your timeline. While you can change the start frame in the composition settings in After Effects before you export the JSON file with TrackerJack, you might find it easier to adjust where your footage begins in Blender by using this setting. 

**Enable** - If Checked start frame will be adjusted.
**Frame** - Enter the Frame Number in Blender where the scene should start.
**Movie Only** - Click Enable if you want to adjust the movie start independent of the tracked camera. (Uncommon for most uses)

        .. image:: images/BPanel_ImportOpts3.png
            :alt: Start Frame Adjust
        
 .. tip::
        After Effects compositions normally start at Frame 0, Blender timelines begin at Frame 1. TrackerJack adjusts all start frames from 0 to 1 automatically. However, if the After Effects composition begins after frame 1, TrackerJack makes no adjustment. (Unless you use the Frame Adjust option).

Alternate Import Workflow
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Although there are many more features when using the TrackerJack 'n' panel in the 3D View, the original method of import is maintained. 

• From the Blender Menu commands *File > Import > TrackerJack AE Tracking Data (.json)*

        .. image:: images/BImport1.png
            :alt: File Import

• Tap the n key to display the **Import Options**
• Choose the appropriate settings and click the **Import** button.

        .. image:: images/BImport2.png
            :alt: File Import Options

 .. tip::
        This method is only reccomended for users who have no issues with file paths (different Windows systems, network drives, or unsual naming conventions can make file path resolution inconsisitent).
        If you have errors using this, you should instead use the TrackerJack panel in order to verify filepaths and other error checks availble in the full user interface.
