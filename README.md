# Super-Resolution of Sentinel-2 RGB Images with VENµS Reference Images Using SRResNet CNNs
Super-Rsolution (SR) is a well-established technique used to enhance the resolution of low-resolution images. In this paper, we introduce a novel approach for the super-resolution of Sentinel-2 10 m RGB images using higher-resolution Venus 5 m RGB images. The proposed method takes advantage of a modified SRResNet network, integrates perceptual loss based on the VGG network, and incorporates a learning rate decay strategy for improved performance. By leveraging higher-resolution VENµS 5 m RGB images as reference images, this approach aims to generate high-quality super-resolved images of Sentinel-2 10 m RGB images. The modified SRResNet network was designed to capture and learn underlying patterns and details present in Venus images, enabling it to effectively enhance the resolution of Sentinel-2 images. In addition, the inclusion of perceptual loss based on the VGG network helps preserve important visual features and maintain the overall image quality.
```
https://doi.org/10.3390/ECRS2023-16863
```

We used SEN2VENµS paired tensors to do this research.

## 1 Installation
First of all, You need install packages. run below code:
```
!pip install -r requirements.txt
```

## 2 Load Data
You have to load your data in tensor form (as we used VENµS images). Geolocation is not necessary.

## 3 Training
In this part you can modify hyper parameters based on your resource. here we used learning rate decay to improve training and learning process. in each epoch if validation loss is better than the previous epoch, the model state will be saved.
![environsciproc-29-00080-g001](https://github.com/user-attachments/assets/83a2efd5-1096-4e28-be7f-174d24107cea)
![output](https://github.com/user-attachments/assets/494abe17-ba55-435c-bf1c-22342031cd98)
![output2](https://github.com/user-attachments/assets/458c6d78-4c86-47a9-a521-1a4571bf89c0)


## 4 Test
In this part we load our Test image in tensor form and also load the best state model. here you can compare input data, ground-truth and output.
## 4 Calculate Metrics and Evaluation
here we calculate PSNR and SSIM for each training, validation and test process.

## 🖊️ 5 Citation
If you use this work in any way, please mention this citation:
```

@Article{ECRS2023-16863,
AUTHOR = {Sharifi, Amir and Shah-Hosseini, Reza},
TITLE = {Super-Resolution of Sentinel-2 RGB Images with VENµS Reference Images Using SRResNet CNNs},
JOURNAL = {Environmental Sciences Proceedings},
VOLUME = {29},
YEAR = {2024},
NUMBER = {1},
ARTICLE-NUMBER = {80},
URL = {https://www.mdpi.com/2673-4931/29/1/80},
ISSN = {2673-4931},
DOI = {10.3390/ECRS2023-16863}
}
```





