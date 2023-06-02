# wav2vec2-xls-r-elderly-cv-13-frisian-augmented
This is my demonstration which was made for my MSc Voice Technology thesis at Rijksuniversiteit Groningen/Campus Fryslân. The title of the thesis is **Evaluation of wav2vec 2.0 Speech Recognition for the Elderly Frisian Population**.
## Requirements
The experiments were conducted on an Nvidia Tesla A100 Tensor Core GPU with 40GB of VRAM and 512GB of memory from the Habrok high-performance computing cluster of Rijksuniversiteit Groningen. In this setup, the jobs must be running for at least 2 hours in order to execute one of the fine-tuning experiments. All the pip installs you need to do to run the code can be found and executed in the jupyter notebooks (and I recommend using a virtual environment to install them), but here is a list of them:
```
!pip install audiomentations
!pip install numpy
!pip install soundfile
!pip install pydub
!pip install audio2numpy
!pip install datasets
!pip install transformers
!pip install torch
!pip install pandas
!pip install IPython
!pip install unidecode
!pip install transformers
!pip install torchaudio
!pip install jiwer
!pip install soundfile
!pip install librosa
!pip install evaluate
```


## How to run the code?
Make sure you have Python 3.9.6 installed. 
Download version 13.0 of the Frisian subset from the [Common Voice website](https://commonvoice.mozilla.org/en/datasets).
Next, clone the repository to your local machine:
```
git clone https://github.com/Golesheed/wav2vec2-xls-r-elderly-cv-13-frisian-augmented
``` 
Then, make a virtual enviroment:
```
python3 -m venv name_of_the_venv
```
And activate it:
```
source name_of_the_venv/bin/activate
```
Lastly, install Jupyter Notebook:
```
pip install jupyter
```
Make sure you change the path in all of the .csv files. If you do not want to do the augmentations yourself you can unzip the .zip files in [aug_audio](https://github.com/Golesheed/wav2vec2-xls-r-elderly-cv-13-frisian-augmented/tree/main/aug_audio).

Here is a list of the models I made in hugging face for the purpose of this project, the models are not the best results but they are the results to the last experiment in hand:
- golesheed/wav2vec2-large-xls-r-1b-frisian-cv-13-elderly on greenw0lf/wav2vec2-large-xls-r-1b-frisian
- golesheed/wav2vec2-large-xls-r-1b-cv-13-elderly-frisian on facebook/wav2vec2-xls-r-1b
- golesheed/wav2vec2-large-xls-r-1b-frisian-cv-13-elderly-augmented on greenw0lf/wav2vec2-large-xls-r-1b-frisian 
