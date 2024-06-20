# Computational-Creativity-Assessment
An emotion-based midi creation project.
The artefacts that the generative AI system produces are audio files. The user can choose what emotion they would like to hear, it downloads the dataset. The midi files are put through tempo adjustment, and an L System based on the emotion chosen. The L System adjusts the midi files using pretty midi, events such as pitch, start of note, end of note, duration and velocity. Key factors of the L-System are customisable such as extending the duration of notes, customising pitch, customising rhythmic patterns. After the changes are applied to the dataset of midi files, the processed files are put through the training class that then trains a LSTM architecture that consists of 6 LSTM Layers and 2 dropout layers separating the LSTM Layers. The LSTM Layers then proceed to four dense layers for pitch, velocity, step and duration, Sparse Categorical Cross Entropy is used for pitch and velocity, whilst Huber loss is used for duration and step loss.

After the midi files have been put through the neural network, it then uses pretty midi to generate audio from the notes generated to listen to the result of the whole process.

The concept of creativity with ai is explored with use of Chat GPT prompts, influencing sections of the project.

Prompt “I want to test your ability to be creative, I am going to give you underlying concepts of what I want you to achieve and step by
step I want you to generate creative code. How can you be creative with pre-processing creative concepts, non-conformity, originality“

I took heavy inspiration from the tensor flow tutorial on midi generation ([https://www.tensorflow.org/tutorials/audio/music_generation](https://www.tensorflow.org/tutorials/audio/music_generation))
