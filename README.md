# Data augmentation for Automatic Speech Recognition or Speech Classification 

You can use this repository to generate syntactic data for ASR models training. 
 
## Noise Data Preprocessing 
- Collect background noise wav files `/background_noise/`. 
- It contains various sounds such as people talking, music, fan, playground, white noise, etc.
- Convert noise files to the same sample rate as your dataset.
- Create `/noise_files/noise_manifest.jsonl` to be used for data augmentation.
- run `create_noisy_files.ipynb`


##  Data Augmentation 
- Create `manifest_label1.jsonl` for key words.
- Apply **Speed Perturbation** to change the speed of the speech, but it does not preserve pitch of the sound. Try a few random augmentations to see how the pitch changes with change in duration of the audio file.
- Apply **Noise Perturbation** to add backgorund noise to original speech. It randomly chooses an audio clip from the set of noise audio samples available.
- Create `manifest_label1_aug_noise.jsonl` to be used for model training/fine tuning in speech classication.
- run `data_augmentation.ipynb`

Reference source code for [augmentation](https://colab.research.google.com/github/NVIDIA/NeMo/blob/v1.0.0b2/tutorials/asr/05_Online_Noise_Augmentation.ipynb#scrollTo=zV9ypBqz7V9a)
