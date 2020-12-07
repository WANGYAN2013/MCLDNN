# A Spatiotemporal Multi-Channel Learning Framework for Automatic Modulation Recognition
by Jialang Xu, Chunbo Luo, Gerard Parr, Yang Luo.

Official implement of the paper, '[A Spatiotemporal Multi-Channel Learning Framework for Automatic Modulation Recognition](https://ieeexplore.ieee.org/document/9106397)'.

This repository contains MCLDNN implementation and datasets in the paper.

## Introduction
Automatic modulation recognition (AMR) plays a vital role in modern communication systems. We proposes a novel three-stream deep learning framework to extract the features from individual and combined in-phase/quadrature (I/Q) symbols of the modulated data. The proposed framework integrates one-dimensional (1D) convolutional, two-dimensional (2D) convolutional and long short-term memory (LSTM) layers to extract features more effectively from a time and space perspective. Experiments on the benchmark dataset show the proposed framework has efficient convergence speed and achieves improved recognition accuracy, especially for the signals modulated by higher dimensional schemes such as 16 quadrature amplitude modulation (16-QAM) and 64-QAM.

## Citation
If this work is useful for your research, please consider citing:
```
@ARTICLE{9106397,
	author={J. {Xu} and C. {Luo} and G. {Parr} and Y. {Luo}},
	journal={IEEE Wireless Communications Letters}, 
	title={A Spatiotemporal Multi-Channel Learning Framework for Automatic Modulation Recognition}, 
	year={2020},
	volume={9},
	number={10},
	pages={1629-1632},
	doi={10.1109/LWC.2020.2999453}
	}
```

## Disclarm
- Note that our code is partly based on [radioml](https://github.com/leena201818/radioml). Thanks [leena201818](https://github.com/leena201818) for his great work!

## Requirements
- Python 3.6.10
- TensorFlow-gpu 1.14.0
- Keras-gpu 2.2.4

## Content
### Model Performance
The recognition accuracy of the MCLDNN is shown in Fig.1. 

<img src="https://github.com/wzjialang/MCLDNN/blob/master/figure/Acc.png" height="300"/>

Fig.1 Recognition accuracy comparison on the RadioML2016.10a dataset.
### Datasets
The available datasets can be downloaded from the table below:
<table>
	<tr>
	    <th>Datasets</th>
	    <th>Download</th>
	</tr>
    <tr>
	    <td>RadioML2016.10a</td>
        <td>[<a href="https://pan.baidu.com/s/1VE2w7of0FW__EgMm3RreoA" target="_blank">drive password:1234</a>] [<a href="https://www.deepsig.ai/datasets" target="_blank">official</a>] </td>
	</tr>
	    <td>RadioML2016.10b</td>
        <td>[<a href="https://pan.baidu.com/s/1VE2w7of0FW__EgMm3RreoA" target="_blank">drive password:1234</a>] [<a href="https://www.deepsig.ai/datasets" target="_blank">official</a>]</td>
    </tr>
</table> 


### Training
For the RadioML2016.10a dataset:
```
python train.py --datasetpath /path/to/RML2016.10a_dict.pkl --data 0
```

For the RadioML2016.10b dataset:
```
python train.py --datasetpath /path/to/RML2016.10b.dat --data 1
```

### Testing
For the RadioML2016.10a dataset:
```
python test.py --datasetpath /path/to/RML2016.10a_dict.pkl --data 0
```

For the RadioML2016.10b dataset:
```
python test.py --datasetpath /path/to/RML2016.10b.dat --data 1
```


## License
Code is released under the GPLv3 license for non-commercial and research purposes only. For commercial purposes, please contact the authors.


## Q & A
For any queries, please contact '504006937@qq.com'.
