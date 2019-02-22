# Conv-KNRM

This is a implementation of the paper:
[Convolutional Neural Networks for So-Matching N-Grams in
Ad-hoc Search](http://www.cs.cmu.edu/~zhuyund/papers/WSDM_2018_Dai.pdf)

Inspired by project [K-NRM]([https://github.com/AdeDZY/K-NRM) by the author.


Features
- python3.6 compatible
- latest tensorflow features.
   - ok with tensorflow 1.10 or later
- a Conv-KNRM implementation


### Requirements
---
- Tensorflow
- Numpy
- traitlets

### Run

To run the Conv-KNRM model, just append an argument '--convolution true', for example:


**Training**
```shell
python ./knrm/model/model_knrm.py config-file\
    --train \
    --train_file: path to training data\
    --validation_file: path to validation data\
    --train_size: size of training data (number of training samples)\
    --checkpoint_dir: directory to store/load model checkpoints\
    --load_model: True or False. Start with a new model or continue training \
    --convolution true
```


**Testing**:
```shell
python ./knrm/model/model_knrm.py config-file\
    --test \
    --test_file: path to testing data\
    --test_size: size of testing data (number of testing samples)\
    --checkpoint_dir: directory to load trained model\
    --output_score_file: file to output documents score\
    --convolution true

```

For more details,see the original [README file](./README_KNRM.md).