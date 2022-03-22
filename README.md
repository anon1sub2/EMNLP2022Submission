# Code for the ACL Rolling Review submission (March 2022) - 'FPDM: A Fast Pre-training Technique using Document-Level Metadata for Reliable Customer Support Question Answering'

## Required dependencies

Please run `pip install -r requirements.txt` (`python3` required). For fine-tuning on the TechQA Dataset, use [this](https://github.com/anon1sub2/ARRSubmission/blob/main/TechQA_code/requirements.txt).

## Links to models pre-trained on the EManuals Corpus

- Our proposed RoBERTa-based variants

1. [<em>FPDM<sub>RoBERTa</sub> (hier.)</em>](https://huggingface.co/AnonymousSub/rule_based_roberta_only_classfn_epochs_1_shard_1)
2. [<em>FPDM<sub>RoBERTa</sub> (triplet)</em>](https://huggingface.co/AnonymousSub/rule_based_roberta_bert_triplet_epochs_1_shard_1)
3. [<em>FPDM<sub>RoBERTa</sub></em>](https://huggingface.co/AnonymousSub/rule_based_roberta_hier_triplet_epochs_1_shard_1)

- Ablation studies - changing the document encoder of RoBERTa-based variants to 'Paragraph Encoder + 2-layer transformer' 

1. [PARA ENC. + 2L <em>(hier.)</em>](https://huggingface.co/AnonymousSub/rule_based_roberta_only_classfn_twostage_epochs_1_shard_1)
2. [PARA ENC. + 2L <em>(triplet)</em>](https://huggingface.co/AnonymousSub/rule_based_roberta_twostagetriplet_epochs_1_shard_1)
3. [PARA ENC. + 2L](https://huggingface.co/AnonymousSub/rule_based_roberta_twostagetriplet_hier_epochs_1_shard_1)

- Our proposed BERT-based variants

1. [<em>FPDM<sub>BERT</sub> (hier.)</em>](https://huggingface.co/AnonymousSub/rule_based_only_classfn_epochs_1_shard_1)
2. [<em>FPDM<sub>BERT</sub> (triplet)</em>](https://huggingface.co/AnonymousSub/rule_based_bert_triplet_epochs_1_shard_1)
3. [<em>FPDM<sub>BERT</sub></em>](https://huggingface.co/AnonymousSub/rule_based_hier_triplet_epochs_1_shard_1)

- Baselines

1. [BERT<sub>BASE</sub>](https://huggingface.co/bert-base-uncased)
2. [RoBERTa<sub>BASE</sub>](https://huggingface.co/roberta-base)
3. [EManuals<sub>BERT</sub>](https://huggingface.co/abhi1nandy2/EManuals_BERT)
4. [EManuals<sub>RoBERTa</sub>](https://huggingface.co/abhi1nandy2/EManuals_RoBERTa)
5. [DeCLUTR](https://huggingface.co/AnonymousSub/declutr-model)
6. [CLINE](https://huggingface.co/AnonymousSub/cline)
7. [ConSERT](https://huggingface.co/AnonymousSub/unsup-consert-base)
8. [SPECTER](https://huggingface.co/AnonymousSub/specter-bert-model)

## Fine-tuning on SQuAD 2.0

- To download the training set, run `wget https://rajpurkar.github.io/SQuAD-explorer/dataset/train-v2.0.json`.

- Run `python3 finetune_squad.py <MODEL_TYPE> <MODEL_PATH>`
	- `<MODEL_TYPE>` can be `bert` or `roberta`
	- `<MODEL_PATH>` is the model path/HuggingFace model name.

> To get the models fine-tuned on the SQuAD 2.0 models, just add `_squad2.0` at the end of a pre-trained model's link (For example, the link to the 'triplet + hier.' RoBERTa-based model obtained after pre-training and fine-tuned on SQuAD 2.0 is https://huggingface.co/AnonymousSub/rule_based_roberta_hier_triplet_epochs_1_shard_1_squad2.0)

## Fine-tuning on TechQA Dataset

- Go to https://github.com/anon1sub2/ARRSubmission/tree/main/TechQA_code

## Fine-tuning on S10 QA Dataset

- Go to https://github.com/anon1sub2/ARRSubmission/tree/main/S10_Code