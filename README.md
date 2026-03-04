# MILESTONE3 - Jan-2026-DLGenAI-Project---Messy-Mashup

Overview
Competition Overview: Messy Mashup
The Messy Mashup competition focuses on robust music genre classification under realistic and noisy mixing conditions. Participants are provided with a curated training dataset consisting of songs from 10 distinct music genres, where each song is instrument-separated into four stems: drums.wav, vocals.wav, bass.wav, and others.wav. In addition, a separate dataset containing random noise sounds is supplied.

The core challenge lies in generalization. Instead of clean, original tracks, the test data is composed of mashups created by mixing instrument stems from different songs belonging to the same genre. To ensure musical coherence during mixing, some instrument tracks may undergo tempo adjustments so that all stems are rhythmically synchronized before being combined. To further increase complexity and simulate real-world audio conditions, random noise samples are added to these mashups at varying intensities and positions.

Description
Participants must design models capable of learning genre-specific musical characteristics that remain invariant to:

Cross-song stem recombination,
Tempo variations introduced during synchronization,
Instrument balance changes,
Additive environmental and synthetic noise. The goal is to predict the correct genre label for each noisy mashup. Success in this task requires effective audio representation learning, noise robustness, and the ability to capture high-level musical structure beyond individual instrument timbres. This competition emphasizes practical audio understanding and mirrors challenges encountered in real-world music information retrieval systems, such as remix analysis, noisy audio classification, and content-based music recommendation. The main challenge here is that the training dataset provided and the testing dataset follow different distributions and the participants must explore multiple data augmentation techniques and audio processing libraries such as librosa to get samples that match the test distribution.
Evaluation
Evaluation Metric
Submissions are evaluated using the Macro F1 Score across the 10 genre classes:

Macro F1 computes the F1 score independently for each genre and then averages them.
This metric treats all genres equally, making it well-suited for evaluating performance under potential class imbalance.
Higher macro F1 scores indicate better overall genre classification performance across all classes.

Submission Format
Participants must submit a CSV file with the following columns:

id: Unique identifier for each test mashup
genre: Predicted genre label
The genre column must contain one of the following values:

["blues", "classical", "country", "disco", "hiphop",
 "jazz", "metal", "pop", "reggae", "rock"]
The file should contain a header and have the following format:

id,genre
0001,blues
0002,classical
0003,country
etc.
Competition Host
Livin Nector

