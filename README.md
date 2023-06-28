#  Improving Medical Entity Disambiguation withMedical Mention Relation Information and Entity Fine-grained Information

Code for the  paper "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension"

## Environment
- numpy=1.23.5
- pandas=2.0.2
- python=3.8
- pytorch=1.9.0
- scikit-learn=1.2.2
- scipy=1.10.1
- tqdm=4.65.0
- transformers=4.2.0


## Data Preparation
We conduct experiments on two real-world public biomedical datasets for MED, which are MedMentions and BC5CDR. You can download the MedMentions dataset [[here](https://github.com/chanzuckerberg/MedMentions)]and BC5CDR dataset [[here](http://www.biocreative.org/tasks/biocreative-v/track-3-cdr/)], then unpack it in the data folder.
## Download BioBERT model
Download the BioBERT v1.1 model and place is under the root directory /biobert.
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


