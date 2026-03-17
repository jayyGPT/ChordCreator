# ChordCreator
My personal project in consideration to the great problem of finding good chords, ykiyk


## Plan of Action:

### 1. Type of Chords
- We have two types of chords 
    1. Bass-Like - Includes instruments like Bass Guitar, Trumphet, BassLine Synths
    2. Melodic - Here we have the mids and highs like Piano,Guitar,Arp, High Synths

    For now we will focus on the melodic part atleast for the Phase of Development

### 2. Instrument Selection
- We will therefore filter out only the chords(midi) for the required melodic parts 
- We can proceed in the following ways
    1. INSTRUMENT_SUMMARY - Either filter on the basis of the names of instruments in the "instrument_summary" column. 
    
        We would need the total unique instruments and their names then select the required instruments. Next we would need the specific channel the instrument is located in then extract the midi for the specific channel.

    2. Single instrument - OR we could just search for datasets with just the piano, in case we have enough datapoints we can train the model on those datapoints to get a basic working prototype


### 3. Learnings
- We would require the model to learn:
    1. The Keys (muscially the "scale")
    2. The Timings (musically the "rythm")

### 4. Tune Model
- Need to add few customizations to the trasnformer to effectively grasp rythm and chords