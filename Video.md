Video Tips
======
  
Software for Editing Video
------
  
## Linux  
  
### Lightworks  
  
**Useful Tips To Remember**  
1. Make sure that you isolate the component that you are wanting to cut (switch off the unwanted channels - `FX, V1, A1-A2, A3-A4`) unless you are wanting to cut and move a completed film segment.  
2. To make a frame freeze 
  * Ensure to isolate your video from other components especially the `A1-A2 and A3-A4` channels  
  * Find the frame and zoom right in `CTRL + MouseScroll` press `C` to make a cut in the video then press the `Right Keyboard Arrow` to move one frame to the right then press `C` to make another cut to isolate the single frame.  
  * Right click on the frame and select `Speed` which will bring up a dialog box.  
  * Change the speed to 0% and click `Do it`.  
  * If you would like to extend the duration of the frozen frame click on the right hand join but ensure only the frozen frame's side of the join is highlighted yellow to prevent overwriting the next frame. We want to push the next frame along a little bit.  
  * Use the `Right Keyboard Arrow` to extend the frame by as many frames as you would like it to.  
  * Deselect the frozen frame by clicking the end of the frame within the yellow highlighted area.  
  * Rewind and replay the new frame to ensure that it has worked correctly.  
  * Turn the sound and VFX channels back on as required.  
3. Add audio last if it isn't attached to your video already. If it is attached take care when cutting and removing sections of your video that you cut the audio track as well to maintain sync between the video and audio. You don't want your sound playing out of sync with your video.  
4. Lightworks prefers `.wav` files to use as audio files over `mp3` or other formats. I've had bugs when using other formats. There is an Audio section in this Cookbook that deals with Audio Conversion if required.  
5. Add your audio files after you have finished editing your video for best results.  
6. Use keyframes to add animations to text headings. Go to the VFX you've added and find the **Stopwatch** symbol and click it to highlight it. Now whatever settings that the VFX has is what it will have at the time corresponding with the keyframe time bar you will know that it is correlating due to the small diamond that will appear on the Keyframe progress bar in the bottom left corner of the screen. So for example if you have set the text size to something big and then after clicking the Stopwatch you change the size to 0 then when played the text will grow over time from 0 to large.  
7.  To create a zoom in animation create an **In** and an **Out** and the place a **2d DVE** inside your selection. On the **2d DVE** options panel you can zoom in using *Master* and then pan around using **X** and **Y** to find the desired location.
  * This however creates a choppy effect so we can make it smooth by counting in say 15 or so frames from the beginning of the clip and then clicking on the + button to the left of the keyframes bar to create another **diamond** marker. Go back to the beginning of the clip and reset the positioning before zooming and then once played back the zoom will move straight to the correct position nice and smoothly and finish up at the second **diamond** marker.  This is the key to smooth zoom animations.
  * Do the reverse to zoom back out smoothly.  
8. To add a **Dissolve** transition at the beginning of a film Zoom in enough to see what you are doing.
  * Switch off all channels except the **Video** channel.
  * Move your mouse pointer near the join of the first clip where it starts and it will eventually turn into a **H** on it's side. Right click and make sure that the **Position > From Here** option is selected. Change the **Speed** to whatever suits *72 frames is approximately 3 seconds*. Then click **Add > Dissolve**.
  * If you are unhappy with the result **Ctrl + Z** will undo it and you can repeat the process.
  * To place a **Dissolve** at the end for a **Fadeout** effect make sure **Position > To Here** is selected.  
9. Using the `Text VFX` you can make some of your own effects such as flashing text signs by creating an effect then cutting after about 10 frames followed by 10 frames of no effect then start the effect again for another 10 frames. Continue this for as long as desired. This also works if you would like a text banner that transforms between bigger and smaller just run one banner at a smaller font then change to a larger font then back to smaller etc. I have produced some good effects playing around with editing in different ways.  
  
