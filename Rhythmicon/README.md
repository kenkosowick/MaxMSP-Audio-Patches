# Rhythmicon

A digital version of Leon Theremin's Rhythmicon; an electro-mechanical instrument that plays pitches from the harmonic series
along with their equivalent rhythmic values. 

### Initial Approach 
For the Rhythmicon my initial approach was to use the poly~ object and have 16-voice polyphony, where all the voice subpatchers are identical. 
I originally mapped the midi notes to the harmonics using the “sel” object that sends the harmonic to the respective voice. 
Each voice had its own metronome and would take the harmonic message to determine the pitch and rhythm from it. 
This was a very challenging approach that led to many problems with routing and synchronization. Also, this method made it extra challenging to incorporate the 1/2 harmonic. 
The main downfall of this approach was that it required perfect rhythmic accuracy when performing or else the rhythms would be slightly off.

### Final Design
In the new design, polyphony is created using the “sel” object connected to 16 different voices. 
There is a unique voice for each of the 16 harmonics which are all synced up to a global metronome. 
This was a successful design and worked perfectly when performing the piece.
