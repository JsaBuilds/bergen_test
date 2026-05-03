# bergen_test
Final Project Code for Intro to LLMs

To run:
Upload BERGEN to Google Drive (can be found at `github.com/naver/bergen`) to the `Colab Notebooks` file
Run the two notebooks in Google Colab to reproduce the experiments.

##Note:
Replace `bergen/modules/retrieve.py` with the `retrieve.py` file. This is necessary because older versions of TorchVision used to be able to handle 0-D tensors, and the versions available now aren't able to. There is a small modification that fixes that in this file.

Add `gemma-3-1b.yaml` to `bergen/config/datasets`, because it is not a model in BERGEN's standard support.