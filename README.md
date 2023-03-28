# Cross-Enhancement Transformer for Action Segmentation
This repo provides training &amp; inference code for paper: [Cross-Enhancement Transformer for Action Segmentation](https://arxiv.org/abs/2205.09445.pdf) 

## Enviroment
Pytorch == 1.5.0, torchvision == 0.6.0, python == 3.7.3, CUDA=10.1

## Reproduce our results
```
1. Download the dataset data.zip at (https://mega.nz/#!O6wXlSTS!wcEoDT4Ctq5HRq_hV-aWeVF1_JB3cacQBQqOLjCIbc8) or (https://zenodo.org/record/3625992#.Xiv9jGhKhPY). 
2. Unzip the data.zip file to the current folder. There are three datasets in the ./data folder, i.e. ./data/breakfast, ./data/50salads, ./data/gtea
3. Download the pre-trained models at (https://pan.baidu.com/s/1q8u3c3e0PTi6WXaqVW1S0w?pwd=js9v). There are pretrained models for three datasets, i.e. ./models/50salads, ./models/breakfast, ./models/gtea
4. Run python main.py --action=predict --dataset=50salads/gtea/breakfast --split=1/2/3/4/5 to generate predicted results for each split.
5. Run python eval.py --dataset=50salads/gtea/breakfast --split=0/1/2/3/4/5 to evaluate the performance. **NOTE**: split=0 will evaulate the average results for all splits, It needs to be done after you complete all split predictions.
```

## Train your own model
Also, you can retrain the model by yourself with following command.
```
python main.py --action=train --dataset=50salads/gtea/breakfast --split=1/2/3/4/5
```


## Our code is based on ASFormer 
In our paper, We have improved the decoder and loss function of ASFormer.  [Code is Here](https://github.com/ChinaYi/ASFormer).


------
If you find our repo useful, please give us a star and cite
```
@inproceedings{chinayi_ASformer,  
	author={Wang, Jiahui and Wang, Zhenyou and Zhuang, Shanna and Wang, Hui}, 
	journal={arXiv preprint arXiv:2205.09445},   
	title={Cross-enhancement transformer for action segmentation},
	year={2022},  
}
```
Feel free to raise a issue if you got trouble with our code.
