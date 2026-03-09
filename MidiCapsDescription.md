---
license: cc-by-sa-4.0
size_categories:
- 100K<n<1M
midi-files: 168385
text-captions: 168385
music-features: 13
extended-music-features: 3
---
# MidiCaps Dataset

<!-- Provide a quick summary of the dataset. -->

The [MidiCaps dataset](https://arxiv.org/abs/2406.02255) [1] is a large-scale dataset of 168,385 midi music files with descriptive text captions, and a set of extracted musical features. 

The captions have been produced through a captioning pipeline incorporating MIR feature extraction and LLM Claude 3 to caption the data from extracted features with an in-context learning task. The framework used to extract the captions is available open source on [github](https://github.com/AMAAI-Lab/MidiCaps). 
The original MIDI files originate from the Lakh MIDI Dataset [2,3] and are creative commons licenced. 

Listen to a few example synthesized midi files with their captions [here](https://amaai-lab.github.io/MidiCaps/).

If you use this dataset, please cite [the paper](https://arxiv.org/abs/2406.02255) in which it is presented: 
_Jan Melechovsky, Abhinaba Roy, Dorien Herremans, 2024, MidiCaps: A large-scale MIDI dataset with text captions._


## Dataset Details

<!-- Provide a longer summary of what this dataset is. -->
We provide all the midi files in a .tar.gz form.
Captions are provided as .json files. The "short" version contains the midi file name and the associated caption.

The dataset file contains these main columns:
1. **location** (of the files afte decompressing the .tar.gz file)
2. **caption** - the text caption describing the music piece


Additionally, the file contains the following features that were used for captioning:

3. genre - top two detected genres
4. genre_prob - associated confidence scores for genres
5. mood - top five detected mood/theme tags 
6. mood_prob - associated confidence scores for mood
7. key - most dominant key of the track
8. time_signature - time signature of the track
9. tempo - tempo of the track in beat per minute (bpm)
10. tempo_word - tempo in either Classical Italian terms of Adagio, Largo, Presto, etc., or simplified terms of Slow, Fast, etc.
11. duration - duration of the track in seconds
12. duration_word - duration tag designating short/medium/long piece
13. chord_summary - the most frequent chord pattern in the track
14. chord_summary_occurence - the number of occurence of the most frequent chord pattern
15. instrument_summary - the top 5 instruments by play duration
Last, the file contains the following additional features:
16. instrument_numbers_sorted - instrument numbers (according to MIDI assignment) present in the track sorted by play duration (most played is first)
17. all_chords - this column contains all the chords detected in the track
18. all_chords_timestamps - respective timemarks for the chords from the previous column
19. test_set - we provide a 90/10 train/test split for optional use; this column states either True (is part of the test set) or False (belongs to train set)
## Citation
If you use this dataset, please cite [the paper](https://arxiv.org/abs/2406.02255) that presents it: 
**BibTeX:**
```
@article{Melechovsky2024,
  author    = {Jan Melechovsky and Abhinaba Roy and Dorien Herremans},
  title     = {MidiCaps: A Large-scale MIDI Dataset with Text Captions},
  year      = {2024},
  journal   = {arXiv:2406.02255}
}
```
**APA:**
Jan Melechovsky, Abhinaba Roy, Dorien Herremans, 2024, MidiCaps: A large-scale MIDI dataset with text captions. arXiv:2406.02255.
**GitHub:**
[https://github.com/AMAAI-Lab/MidiCaps](https://github.com/AMAAI-Lab/MidiCaps)
## References
[1] Jan Melechovsky, Abhinaba Roy, Dorien Herremans. 2024. MidiCaps: A large-scale MIDI dataset with text captions. arXiv:2406.02255.
[2] Raffel, Colin. Learning-based methods for comparing sequences, with applications to audio-to-midi alignment and matching. Columbia University, 2016.
[3] https://colinraffel.com/projects/lmd/