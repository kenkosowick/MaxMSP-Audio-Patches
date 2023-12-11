# Harmonic Generator

A patch that generates pitches found in the harmonic series from equal tempered midi notes with the use of xbendout. 

For the Harmonic Generator, my approach was to start by finding the closest midi value to the generated harmonic using “ftom” then converting it back to frequency using “mtof”. 
I then divided that value by the frequency of the harmonic then using the formula “1200 * log(x)/log(2)” to calculate the difference between these frequencies in cents. 
That number was divided by 100 to find it as a ratio of a semitone. After this I had to multiply by -1 to ensure the pitch bends in the correct direction. 
Finally, the number was multiplied by 4096 and added to 8192 to obtain the correct xbendout value to bend the midi pitch to match the pitch of the harmonic. 

The biggest challenge for this project was to figure out a robust way of testing each harmonic. 
A helpful method demonstrated in classes was to use a button to trigger the next harmonic where the midi pitch and cycle are held until triggered again. 
This allowed for enough time to thouroughly cheack each pitch. 
