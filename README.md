Experiment1 (Val Loss: 0.8822, norm. scored wrt baseline: 0.9826):
- PCA with 10 components
- maks. 2M pixels in pca matrix
- efficientnet_b0, pretrained = False
- augmentations for training:
            v2.Resize((224, 224)),
            v2.RandomHorizontalFlip(p=0.5),
            v2.GaussianNoise(mean=0.0, sigma=0.03)
  
