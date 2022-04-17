# w2v2-vad
A wrapper for Audeering's wav2vector-based dimensional speech emotion recognition (valence, arousal, dominance).

## Input-output
input: any audio file readable by librosa at any sample rate (will be resampled to 16000 Hz on the fly)  
output:  score of valence, arousal, and dominance in a range [0, 1]  


## Installation
    pip3 install -r requirements.txt
    
## Usage
    python3 predict_vad_w2v2.py -input.wav

## Arguments
```
Positional: input file  at any sample rate
Optional:  
-s split: chunks or full  
-d duration in seconds (if split is chunks, must be specified)  
```

## Example

```
bagus@L140MU:w2v2-vad$ python3 predict_vad_w2v2.py bagus-test_16000.wav 
Valence, arousal, and dominance #0: [[0.32293236 0.41639617 0.5942142 ]]
bagus@L140MU:w2v2-vad$ python3 predict_vad_w2v2.py bagus-test_16000.wav -s chunks -d 2
Valence, arousal, and dominance #0: [[0.3404813  0.42247295 0.35256445]]
Valence, arousal, and dominance #1: [[0.22009875 0.322832   0.51018834]]
Valence, arousal, and dominance #2: [[0.3478799  0.4332775  0.45645887]]
Valence, arousal, and dominance #3: [[0.29967275 0.4038131  0.4949872 ]]
Valence, arousal, and dominance #4: [[0.24804251 0.33543587 0.50990975]]
Valence, arousal, and dominance #5: [[0.38564402 0.43214017 0.37035757]]
```

## Demo (v1.0)
[![asciicast](https://asciinema.org/a/1XhSclhNuVsfG6bBCPoQLwvN1.svg)](https://asciinema.org/a/1XhSclhNuVsfG6bBCPoQLwvN1)

## Original repo  
https://github.com/audeering/w2v2-how-to

All credit goes to Audeering.
