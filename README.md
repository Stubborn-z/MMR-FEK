#  Medical Entity Disambiguation with Medical Mention Relation and Fine-grained Entity Knowledge

This repository contains the source code and available two datasets for the paper "Medical Entity Disambiguation with Medical Mention Relation and Fine-grained Entity Knowledge".

## Environment Requirements
- numpy=1.23.5
- pandas=2.0.2
- python=3.8
- pytorch=1.9.0
- scikit-learn=1.2.2
- scipy=1.10.1
- tqdm=4.65.0
- transformers=4.2.0


## Data Preparation
- We conduct experiments on two real-world public biomedical datasets for MED, which are MedMentions and BC5CDR. You can download the original MedMentions dataset https://github.com/chanzuckerberg/MedMentions and BC5CDR dataset http://www.biocreative.org/tasks/biocreative-v/track-3-cdr/, then unpack it in the data folder.
- We offer preprocessing code to ensure uniform formatting. You can execute these codes to process all datasets consistently. The corresponding codes can be found in the "data_preprocess" directory.
## Download BioBERT model
Download the BioBERT v1.1 model https://huggingface.co/dmis-lab/biobert-v1.1 and place is under the root directory ./biobert.
## Train the MED Model on the Dataset
If you want to train our model you just have to run the following command in the model folder:
```shell
python model/model.py --data_dir data/BC5CDR/processed_data/ --model_type bert --model_name_or_path biobert --output_dir output --overwrite_output_dir --overwrite_cache --use_hard_and_random_negative --do_train
```
## Evaluation
If you want to evaluate the model on a dataset, just run the following command in the model folder:
```shell
python evaluation/evaluate.py
```
## Acknowledgement
If this work is useful in your research, please cite our paper.
```shell
@inproceedings{zhang2022word,
  title={Medical Entity Disambiguation with Medical Mention Relation and Fine-grained Entity Knowledge},
  author={Lu, Wenpeng and Zhang, Guobiao and Guan, Hongjiao and Peng, Xueping and Wang, Shoujin},
  booktitle={},
  pages={},
  year={2024}
}
```



