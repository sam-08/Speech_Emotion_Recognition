The goal of this project is to build MLP, LSTM and CNN Model for speech emotion recognitionusing Ravdess Emotional Speech Audio dataset.

Using RAVDESS dataset which contains around 1440 audio file inputs from 24 different actors
(12 male and 12 female ),First, we analyzed our dataset by plotting the spectrogram and
waveforms of a sample audio file from the dataset. Then we extracted the features of the data
using Mel Frequency Cepstral Coefficents (MFCCs), chroma frequencies, MeI spectrogram and
Spectral centroid. Then we build a Multi-layer perceptron (MLP) model to predict the emotions
of the audio data as well as the gender of the speaker. We plan to improve upon our performance
by using LSTM model and CNN model, compare the performances of the three and establish
which model is the best for Speech Emotion Recognition (SER).

Feature extraction: is very effective in increasing the accuracy and efficiency of machine learning
algorithms in emotional speech recognition. The input audio file is reduced to a set of features
which represent or summarise the original input. The extracted features are then fed into the
neural network to identify the respective emotion. The features which have been used in the
project are discussed below.

Mel Spectrogram: An audio signal can be broken down into sine and cosine waves that form the original signal.
The frequencies and amplitudes of these representative waves can be used to convert the input
signal from the time to the frequency domain. The fast Fourier transform (FFT) is an algorithm
that can be used to perform this conversion. The FFT is however performed on a single time
window of the input signal. If the frequencies of the representative signals change over time
(non-periodic), the change cannot be captured through a single time window conversion. Using
the FFT over multiple overlapping windows can be used to construct a spectrogram representing
the amplitude of the representative frequencies as they change over time.

Mel-frequency cepstral coefficients (MFCCs): The Fourier spectrum is obtained by using the FFT on an audio signal. Taking the log of
the Fourier spectrum’s magnitude and then taking the spectrum of this log through a cosine
transformation allows us to calculate the cepstrum of the signal (ceps is the reverse of spec,
called so due to being a non-linear ‘spectrum of a spectrum’). The amplitudes of this resulting
cepstrum are the cepstral coefficients. Representing the frequencies in terms of the mel scale
(discussed above) instead of a linear scale converts the cepstrum to a mel-frequency cepstrum
and the cepstral coefficients to mel-frequency cepstral coefficients (MFCCs). The cepstrum
represents the rate of change in the different spectrum bands, and the coefficients are widely
used in machine learning algorithms for sound processing.

Chroma: An octave is a musical interval or the distance between one note and another, which is twice
its frequency: A3 (220 Hz) - A4 (440 Hz) – A5 (880 Hz). An octave is divided into 12 equal
intervals, and each interval is a different note. The intervals are called chromas or semitones
and are powerful representations of audio signals. The calculation of the chromagram is similar
to the spectrogram using short-time Fourier transforms, but semitones/pitch classes are used
instead of absolute frequencies to represent the signal. The unique representation can show
musical properties of the signal which is not picked up by the spectrogram.
