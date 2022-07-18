## Data augmentation for Automatic Speech Recognition or Speech Classification 

You can use this repository to generate syntactic data for ASR models training. 
 
# Noise Datasets Preprocessing 
- Collect background noise wav files (`/background_noise/`). 
- It contains various sounds such as people talking, music, fan, playground, white noise, etc.
- Convert noise files to the same sample rate as your dataset.
- Create (`/noise_files/noise_manifest.jsonl`) to be used for data augmentation.
- run `create_noisy_files.ipynb`
