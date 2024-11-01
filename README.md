# DeepVLF
Variable-length feedback coding has the potential to significantly enhance communication reliability in finite block length scenarios by adapting coding strategies based on real-time receiver feedback. Designing such codes, however, is challenging. While deep learning (DL) has been employed to design sophisticated feedback codes, existing DL-aided feedback codes are predominantly fixed-length and suffer performance degradation in the high code rate regime, limiting their adaptability and efficiency. This paper introduces deep variable-length feedback (DeepVLF) code, a novel DL-aided variable-length feedback coding scheme. By segmenting messages into multiple bit groups and employing a threshold-based decoding mechanism for independent decoding of each bit group across successive communication rounds, DeepVLF outperforms existing DL-based feedback codes and establishes a new benchmark in feedback channel coding.
## Train 
We implement a 2-stage strategy during the training process. Following command can be an example to train and evaluate a model.
```python
python main.py --snr1 0 --snr2 100 --batchSize 8192 --totalbatch 40  --train 1 --core 1 --truncated 10 --restriction 'mid'
```

## Test 
Large batchsize could help improve the statistics accurancy in test stage. Following is an example to test our pretrained's performance.
```python
python main.py --snr1 0 --snr2 100 --batchSize 100000 --train 0 --truncated 10 --restriction 'mid' --test_model 'weights/weight_ff_1_fb_100_gamma_1-1e-5'
```
