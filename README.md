# Text-Classification-on-IMDB  

## 1. Guidance  
* PyTorch Text Classification Benchmarks on IMDB Datasets 🔥  
### Dependencies  
* pandas   
* numpy  
* matplotlib  
* [PyTorch](https://pytorch.org/)  
* torchkeras  

## 2. Have Done  
### Dataset  
* IMDB  

### Methods  
* CNN  ( orginal from this repository: [《20天吃掉那只PyTorch》](https://github.com/lyhue1991/eat_pytorch_in_20_days)[ --《1-3 文本数据建模流程》](https://github.com/AnthonyK97/PyTorch-Tutorials-for-NLP/blob/main/1-3%20%E6%96%87%E6%9C%AC%E6%95%B0%E6%8D%AE%E5%BB%BA%E6%A8%A1IMDB(CNN).ipynb) )  
* CNN + Glove vec  
* BiLSTM  
* BiLSTM + Glove vec 
* BiLSTM + SelfAttention  


| Methods | accuracy | valid accuracy |   
| :------------ |:---------------:|  
| CNN | 0.935 | 0.808 |  
| CNN + Glove | 0.999 | 0.88 | 
| BiLSTM | | |  
| BiLSTM + Glove | | |  

| Methods | accuracy  | valid accuracy |
| :------------ |:---------------:| :-----:|
| CNN | 0.935 | 0.808 |  
| CNN + Glove | 0.999 | 0.88 | 
| BiLSTM | | |  
| BiLSTM + Glove | | |  
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |


### 改进
* A new Dataloader:  
  * 原Dataloader将每一个样本都切分成一个txt文件存放样本特征，造成了大规模的文件I/O操作，大大增加了时间开销（尤其是在GPU上进行训练时）
  * 重写的Dataloader只需要load数据预处理时已经处理好的text token tsv，不需要对train_samles和test_samples下的文件进行I/O操作。

## 3. Others 
* glove 词向量：
  * Download: http://nlp.stanford.edu/data/glove.6B.zip 
  * 解压至glove.6B folder (主要使用glove.6B.100d.txt)
