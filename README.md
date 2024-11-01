# DeepVLF

#Train
We implement a 2-stage strategy during the training process. Following command can be an example to train and evaluate a model.
```python
python main.py --snr1 0 --snr2 100 --batchSize 8192 --totalbatch 40  --train 1 --core 1 --truncated 10 --restriction 'mid'
```

#Test
Large batchsize could help improve the statistics accurancy in test stage.
```python
python main.py --snr1 0 --snr2 100 --batchSize 100000 --train 0 --truncated 10 --restriction 'mid' --test_model 'weights/weight_ff_1_fb_100_gamma_1-1e-5'
```
