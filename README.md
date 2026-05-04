# bergen_test
Final Project Code for Intro to LLMs

#*SETUP:*

Download BERGEN (can be found at `github.com/naver/bergen`).

Replace `bergen/modules/retrieve.py` with the `retrieve.py` file from this repo. This is necessary because older versions of PyTorch used to be able to handle 0-D tensors, and the versions available now aren't able to. There is a small modification in the new file that fixes this.

*Special config files* (in the `generator`, `dataset` and `prompt` folders):

Add `gemma-3-1b.yaml` from the repo to the folder `bergen/config/generators`.

Add `asqa_Karpukhin.yaml` to bergen/config/dataset. All experiments on the ASQA dataset run with this config file.

Add `asqa.yaml` and `nq.yaml` to the folder `bergen/config/prompt` (replace the current `nq.yaml` file). These contain updated prompts for the experiments that we used.

Add `requirements_josiah.txt` to the folder `bergen/`. This file accounts for package discrepancies of installed python packages.

Upload BERGEN to Google Drive inside the `Colab Notebooks` folder

Upload the two notebooks to Google Colab. To reproduce our environment, use Google Colab Pro with a A100 GPU on High-RAM mode. Make sure to give the notebooks access to your `HF_TOKEN` HuggingFace authentication token in your Secrets.


#*RUNNING THE EXPERIMENTS:*

Run the two notebooks in Google Colab to reproduce the experiments.

Note: You can adjust the configuration variables at the top of a notebook to run different checks and experiments.