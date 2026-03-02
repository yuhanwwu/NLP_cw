## BestModel
HateBERT fine tuned for PCL binary classification, with weighted loss, keyword augmentation, and increased dropout.

## Results
| Model | Dev F1 on PCL |
|---|---|
| RoBERTa-base baseline | 0.48 |
| HateBERT alone | 0.5381 |
| HateBERT + weighted loss | 0.5506 |
| HateBERT + weighted loss + dropout | 0.5658 |
| HateBERT + weighted loss + dropout + keyword (BestModel) | 0.5714 |

All experimental runs including ablations (e.g. HateBERT without weighted loss, without keyword augmentation, without dropout) can be found in `hatebert_pcl.ipynb` in the root of the repository.

## Load pretrained model 
`best_model.pt` is included in this repo vio Git LFS. Set `LOAD_MODEL = True` in the config cell (default), and run all cells.

## Train from scratch
Set `LOAD_MODEL = False` in the config cell and run all cells. Training takes approximately 45 minutes on a GPU. 

## Pretrained Model
HateBERT: Caselli et al. (2021) - https://huggingface.co/GroNLP/hateBERT
