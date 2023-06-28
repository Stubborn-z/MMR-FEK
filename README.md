#  Improving Medical Entity Disambiguation withMedical Mention Relation Information and Entity Fine-grained Information

Code for the  paper "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension"

## Environment
- black=21.5b2
- nlp=0.4.0
- nltk=3.4.5
- numpy=1.21.2
- pandas=1.3.5
- python=3.7.12
- pytorch=1.8.0
- pytorch-lightning=0.9.0
- tqdm=4.64.0
- transformers=3.2.0
- wandb=0.12.12


## Data Preparation
We conduct experiments on two real-world public biomedical datasets for MED, which are MedMentions and BC5CDR. You can download the dataset [[here](https://github.com/chanzuckerberg/MedMentions)]and unpack it in the data folder.
## Train the WSD Model on the Dataset
If you want to train your own model you just have to run the following command in the KELESC folder:
```shell
python model/train.py
```
## Evaluation
If you want to evaluate the model on a dataset, just run the following command in the KELESC folder:
```shell
python model/predict.py --ckpt <kelesc_checkpoint.ckpt> --dataset-paths data/WSD_Evaluation_Framework/Evaluation_Datasets/semeval2007/semeval2007.data.xml 
```
The ```--dataset-paths``` can be modified. For example, change  ```/semeval2007/semeval2007.data.xml``` to ```/semeval2013/semeval2013.data.xml```. The predictions will be saved in the folder ```predictions``` with the name ```<dataset_name>_predictions.txt```.
## Citation
Please cite our paper if you find it helpful.
```
@inproceedings{,
    title = "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension",
    author = "Guobiao Zhang and 
      Wenpeng Lu and
      Xueping Peng and
      Shoujin Wang and
      Baoshuo Kan and
      Rui Yu",
    booktitle = "Proceedings of the 29th International Conference on Computational Linguistics",
    year = "2022",
}
```
## Acknowledgement
Parts of the code are modified from [ESC](https://github.com/SapienzaNLP/esc). We appreciate the authors for making ESC open-sourced.


