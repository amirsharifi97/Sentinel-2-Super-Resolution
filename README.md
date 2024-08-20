# Sentinel-2 SuperResolution
Super-Resolution of Sentinel-2 RGB Images with VENµS Reference Images

https://doi.org/10.3390/ECRS2023-16863

In this we tried to enhance spatial resolution of sentinel-2 images in visible bands using real ground-truth data VENµS images.

we used SEN2VENµS paired tensors to do this research.
## 1 Installation
First of all, You need install packages. run below code:
```
!pip install -r requirements.txt
```

## 2 Load Data
You have to load your data in tensor form (as we used VENµS images). Geolocation is not necessary.

## 3 Training
In this part you can modify hyper parameters based on your resource. here we used learning rate decay to improve training and learning process. in each epoch if validation loss is better than the previous epoch, the model state will be saved.

## 4 Test
In this part we load our Test image in tensor form and also load the best state model. here you can compare input data, ground-truth and output.
## 4 Calculate Metrics
here we calculate PSNR and SSIM for each training, validation and test process.








