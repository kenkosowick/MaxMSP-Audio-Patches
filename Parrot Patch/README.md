# Parrot Patch

For the Parrot Patch, I started by building upon the level detection patch shared with the class. 
I used an if statement to toggle recording while using the clocker object to set a timer for 4000 ms. 
The timer was used to automatically toggle recording and play from the buffer. 
I used the groove object to play the samples stored in the buffer at 1.3 speed to mimic the sound and pitch of a parrot. 
Using an additional clocker object, the samples stored in the buffer are triggered to play again after 2000 ms. 
After it finishes, level detection is enabled once again to allow for another recording. 

Additionally, I added keyboard sampling capabilities by playing back the sound at different speeds depending on what note is pressed on the keyboard.
