# TeamsAudio
Useful scripts to work with audio data in teams research

## Extract Voiced Audio
Based on python interface to the WebRTC Voice Activity Detector (VAD).

```
python2 newAudio.py <aggressiveness> <inFile.wav> <outFile.csv>
```

This will process the audio and detect voiced speech. <aggressiveness> are values 1, 2, 3 with 3 being most aggressive (a good default). 
  Output is csv that has one row for every "frame" -- same sample rate as the input audio.
  "Voiced speech" are then those frames that have IsSpeech==1 and Chunk != NA.

This is based on the `example.py` script https://github.com/wiseman/py-webrtcvad
