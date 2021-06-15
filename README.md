# Be Water - Camera As Presence Sensor
This is a patch made in MAX MSP 8, that engages the user in an interactive way. 
The WebCam is used as a sensor to detect motion/presence. If the user moves, then the sound of the ocean is triggered, else the sound of wind is heard. 
The sound is generated with a reson~ object using noise~. The parameters (gain, frequency and resonance) are changing values for both wind and ocean, depending on which one is triggered.
The patch uses Vizzie objects and MaxMsp objects.

## Installing
You need to have MAX MSP 8 installed on your computer. 
## Usage
1. Open the patch. 
2. Enter Lock Mode: CTRL + mouseClick
3. You will notice the patch is split in 2 parts. The one in the left side is dealing with grabbing the camera and analyzing the RGB average values of the video. The 2nd part of the screen deals with creating the sound with a reson~ object. You will interact with both sides.
4. Follow instructions in the comments to start the patch:
    1. GRABBR - select an input camera. If it's mirrored, set it right. 
    2. CROPPR - select a portion of your image, that you want to be analyzed for motion detection. 
    You could choose to trigger the sound with your eyes, mouth or your hands, or the whole video; whatever you want. 
    After you select the Crop in the first square, position the L and R edges of the cropped image in the second square, by pulling the sliders. 
    Enter Help Mode, for a better understanding of the object. (Unlock Mode, Right Click on the object -> Help OR Alt Click on the object)
    3. OPER8R - Set operation to - (MINUS)
    4. DELAYR - delay with 1 frame, to compare the current frame with the previous one to see if there is motion.
        set Delay -> 1, Feedback ~ 0.53, Crossfade -> 1. VIEWR object will show the motion.
    5. SPEAKER - set speaker on, and add a low gain value (reson~'s output). Be careful, the noise could be very powerful. Add a little gain to the reverb object as well. (cverb~'s output). 
 
## Links
this is a video that shows how to configure the objects in the patch related to camera and demonstrates how it works.
https://youtu.be/QHUuzLUZI1I
## License 
the image analyzer is inspired by the work of Morten Elkjær 'Max/MSP - Using video (webcam) to control audio and MIDI'
https://youtu.be/mmJ79sLDpE0 (accessed 14.06.2021)
