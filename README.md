## DL_LCSP

Our work focused on the low capacity status prediction (LCSP) problem to improve availability of cloud service with a classification model. We have proposed an effective approach to predict the low capacity status in the cloud, and the details are presented in the following paper. By exploiting the dependencies of time series, the LSTM-based model outperforms the classical approaches. Moreover, the attention and embedding mechanisms are effective to improve performance by concentrating on the significant part of time series and local behavior. 

"Effective low capacity status prediction for cloud systems". 

## Get Started
The model is implemented in pytorch.   
#inputs:  
data_x: time-series features with the shape of (d_f, d_t), where d_f denotes the dimension of time-series features, d_t denotes the time-step for LSTM network.  
key_inds: index of region VM-family key  
#label:   
low capacity status (0 or 1) in next 7 days.


### Files
config.py    : configurations for hyper-parameters and data root path  
models.py    : formulate models including base LSTM, LSMT+Attention, LSTM+key Embedding, and proposed model  
train.py     : train LCSP net (model checkpoints, loss records, and evaluation metrics are saved)  
visualize.py : visualize attention weight (heat map) and key-vector (t-SNE) results  

