  
==============================================================================
Code accompanying the paper ["Real-time Fault Localization in Power Grids With Convolutional Neural Networks"](https://arxiv.org/abs/1810.05247)

## Prerequisites
The proposed method is implemented through Jupyter Notebook. The required packages include:
- Jupyter Notebook
- Python 3
- Numpy
- Tensorflow 1.11

## Getting started
1) If you have Jupyter Notebook, you can directly run the codes of "ipynb" files;
2) If you only have python, you can run the "py" files in the command line, for example:
```bash
    python  Training_by_CNN_on_partial_data.py
```
 

## Visualization of the 4-layer CNN structure

<center><img src="img/CNN.png" /></center> 

## Simulation Platform

<center><img src="img/System.png" /></center>

## Performance comparison of different methods (Multiclass support vector machine (MSVM), Neural Network (NN), and CNN) when 100% observability 

<center><img src="img/Compare_full_data.png"/></center>

## Performance comparison of different methods when 15%~30% observability

<center><img src="img/Compare_partial_data.png"/></center>

## Neighborhood property when partial observability

<center><img src="img/neighbor.png"/></center>

## The proposed algorithm to select meausured buses

<center><img src="img/alg.png"/></center>

<center><img src="img/alg_cmp.png"/></center>

## Robustness to noise
<center><img src="img/noise.png" /></center>

## What we have achieved:
1, Define the feature vector based on the sparse fault current;

2, Build a CNN of 4 layers to locate the fault by classifying the faulted line;

3, The performance on four types of line faults with different fault impedances are tested;

4, When only partial buses are measured, the performances of CNN and other machine learning methods are compared,
 and CNN is superior than others;
 
5, An algorithm of selecting the measured buses is proposed and compared with other topology based method;

6, The location performance under noisy condition is also tested.

## Introduction of the files included:
1, 'Datasets': saves the training and testing datasets;

2, 'Codes': include the codes by python 3 implemented on Jupyter Notebook, and the details are summarized as follows:

	1, "Training_by_CNN_on_partial_data": is the training model with complete or partial measured buses together with the 
		topology of our 4-layer CNN visualized through tensorboard;
		
	2, "Testing_by_CNN_on_partial_data" : is the testing codes of the CNN with different measured bus. In the example, performance 
		with 12 buses measured is obtained,  but different performance with various measured buses could be tested by changing the name of folder names "best_model_#_bus";
		
	3, "Training_by_NN_on_partial_data" and "Testing_by_NN_on_partial_data" are the training and testing datasets through NN classifier;
	
	4, "Testing_by_Multi_SVM_on_partial_data" is the training and testing process using Multi-SVM;
	
	5, Compared with the performance using the Random or topology based algorithms (2-hop VC), the proposed method shows better 
		location accuracy rate, and the saved model and testing codes are in the folders of "best_model_proposed_12", 
		"best_model_random_12" and "best_model_topology12" respectively.
		
3, 'Figures_codes': Some performance comparison figures.


## Reference

Feel free to apply our methods, run the codes, and please cite our paper as follows:

Li, Wenting, Deepjyoti Deka, Michael Chertkov, Meng Wang. **"Real-time Faulted Line Localization and PMU Placement in Power Systems through Convolutional Neural Networks."** IEEE Transactions on Power Systems (2019). 
 
