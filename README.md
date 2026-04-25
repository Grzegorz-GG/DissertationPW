<h3>Experiment1 (Val Loss: 0.8822, norm. score wrt baseline: 0.9826):</h3>
<p>
P: Model MSE = 659.6602, Baseline MSE = 650.8644, Normalized = 1.0135 <br>
K: Model MSE = 3364.4214, Baseline MSE = 3366.1325, Normalized = 0.9995 <br>
Mg: Model MSE = 1624.4281, Baseline MSE = 1640.6900, Normalized = 0.9901 <br>
pH: Model MSE = 0.0627, Baseline MSE = 0.0676, Normalized = 0.9273 <br>
</p>
<ul>
    <li>PCA with 10 components</li>
    <li>maks. 2M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment2 (Val Loss: 0.8794, norm. score wrt baseline: 0.9770):</h3>
<p> Notes: Slightly better overall performance wrt baseline</p>
<p>
P: Model MSE = 648.0110, Baseline MSE = 650.8644, Normalized = 0.9956<br>
K: Model MSE = 3333.3560, Baseline MSE = 3366.1325, Normalized = 0.9903<br>
Mg: Model MSE = 1678.2568, Baseline MSE = 1640.6900, Normalized = 1.0229<br>
pH: Model MSE = 0.0608, Baseline MSE = 0.0676, Normalized = 0.8994<br>
</p>
<ul>
    <li>PCA with 10 components</li>
    <li>Incremental PCA applied in batches (all pixels used)</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment3 (Val Loss: 0.8605, norm. score wrt baseline: 0.9705):</h3>
<p> Notes: Slightly better overall performance wrt baseline, but in general worse for P and Mg</p>
<p>
P: Model MSE = 656.0670, Baseline MSE = 650.8644, Normalized = 1.0080<br>
K: Model MSE = 3285.4338, Baseline MSE = 3366.1325, Normalized = 0.9760<br>
Mg: Model MSE = 1648.3019, Baseline MSE = 1640.6900, Normalized = 1.0046<br>
pH: Model MSE = 0.0604, Baseline MSE = 0.0676, Normalized = 0.8935<br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 2M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment4 (Val Loss: 0.8914, norm. score wrt baseline: 1.0017):</h3>
<p> Notes: Very weak performance with pretrained encoder</p>
<p>
P: Model MSE = 652.3175, Baseline MSE = 650.8644, Normalized = 1.0022 <br>
K: Model MSE = 3420.5713, Baseline MSE = 3366.1325, Normalized = 1.0162 <br>
Mg: Model MSE = 1752.4696, Baseline MSE = 1640.6900, Normalized = 1.0681 <br>
pH: Model MSE = 0.0622, Baseline MSE = 0.0676, Normalized = 0.9201 <br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 2M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>


<h3>Experiment5 (not saved):</h3>
<p> Notes: Warm-up phase added</p>
<p>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 2M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 6(norm. score wrt baseline: 0.9902):</h3>
<p> Notes: 4M pixels with rand pca (better GPU used) + warm-up phase. Performance did not improve.</p>
<p>
P: Model MSE = 658.4203, Baseline MSE = 650.8644, Normalized = 1.0116 <br>
K: Model MSE = 3388.1912, Baseline MSE = 3366.1325, Normalized = 1.0066 <br>
Mg: Model MSE = 1674.3439, Baseline MSE = 1640.6900, Normalized = 1.0205 <br>
pH: Model MSE = 0.0623, Baseline MSE = 0.0676, Normalized = 0.9221 <br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 4M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>


<h3>Experiment 7(val loss:0.8706 ,norm. score wrt baseline: 0.9803):</h3>
<p> Notes: 8M pixels with rand pca (better GPU used) + warm-up phase.</p>
<p>
P: Model MSE = 825.3816, Baseline MSE = 833.2123, Normalized = 0.9906 <br>
K: Model MSE = 4115.5469, Baseline MSE = 4031.7278, Normalized = 1.0208 <br>
Mg: Model MSE = 1468.3999, Baseline MSE = 1499.2853, Normalized = 0.9794 <br>
pH: Model MSE = 0.0674, Baseline MSE = 0.0724, Normalized = 0.9303 <br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 8M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 8(Val Loss: 0.9092,norm. score wrt baseline: 0.9828):</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase.</p>
<p>
P: Model MSE = 835.7007, Baseline MSE = 833.2123, Normalized = 1.0030 <br>
K: Model MSE = 4030.0684, Baseline MSE = 4031.7278, Normalized = 0.9996 <br>
Mg: Model MSE = 1492.8458, Baseline MSE = 1499.2853, Normalized = 0.9957 <br>
pH: Model MSE = 0.0675, Baseline MSE = 0.0724, Normalized = 0.9328 <br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 9(Val Loss: 0.9092,norm. score wrt baseline: 0.9953):</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase.</p>
<p>
P: Model MSE = 838.8846, Baseline MSE = 833.2123, Normalized = 1.0068 <br>
K: Model MSE = 4089.4575, Baseline MSE = 4031.7278, Normalized = 1.0143 <br>
Mg: Model MSE = 1539.5592, Baseline MSE = 1499.2853, Normalized = 1.0269 <br>
pH: Model MSE = 0.0676, Baseline MSE = 0.0724, Normalized = 0.9333 <br>
</p>
<ul>
    <li>PCA with 10 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 10(norm. score wrt baseline: 1.0406:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase.</p>
<p>
P: Model MSE = 869.2822, Baseline MSE = 833.2123, Normalized = 1.0433 <br>
K: Model MSE = 4125.5552, Baseline MSE = 4031.7278, Normalized = 1.0233 <br>
Mg: Model MSE = 1589.5768, Baseline MSE = 1499.2853, Normalized = 1.0602 <br>
pH: Model MSE = 0.0750, Baseline MSE = 0.0724, Normalized = 1.0358 <br>
</p>
<ul>
    <li>PCA with 15 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>


<h3>Experiment 11(norm. score wrt baseline: 1.0495:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase.</p>
<p>
P: Model MSE = 895.3030, Baseline MSE = 833.2123, Normalized = 1.0745 <br>
K: Model MSE = 4197.0293, Baseline MSE = 4031.7278, Normalized = 1.0410 <br>
Mg: Model MSE = 1579.4727, Baseline MSE = 1499.2853, Normalized = 1.0535 <br>
pH: Model MSE = 0.0745, Baseline MSE = 0.0724, Normalized = 1.0292 <br>
</p>
<ul>
    <li>PCA with 25 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 12(norm. score wrt baseline: 4.5783:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 2428.2415, Baseline MSE = 833.2123, Normalized = 2.9143 <br>
K: Model MSE = 4279.1182, Baseline MSE = 4031.7278, Normalized = 1.0614 <br>
Mg: Model MSE = 14982.9570, Baseline MSE = 1499.2853, Normalized = 9.9934 <br>
pH: Model MSE = 0.3146, Baseline MSE = 0.0724, Normalized = 4.3442 <br>
</p>
<ul>
    <li>PCA with 25 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 13(norm. score wrt baseline: 0.9793:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 829.2197, Baseline MSE = 833.2123, Normalized = 0.9952 <br>
K: Model MSE = 3996.0264, Baseline MSE = 4031.7278, Normalized = 0.9911 <br>
Mg: Model MSE = 1504.6293, Baseline MSE = 1499.2853, Normalized = 1.0036 <br>
pH: Model MSE = 0.0671, Baseline MSE = 0.0724, Normalized = 0.9272 <br>
</p>
<ul>
    <li>PCA with 10 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 14(norm. score wrt baseline: 0.9877:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 841.9759, Baseline MSE = 833.2123, Normalized = 1.0105 <br>
K: Model MSE = 4078.8909, Baseline MSE = 4031.7278, Normalized = 1.0117 <br>
Mg: Model MSE = 1510.8041, Baseline MSE = 1499.2853, Normalized = 1.0077 <br>
pH: Model MSE = 0.0667, Baseline MSE = 0.0724, Normalized = 0.9209 <br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 15(val loss: 4.3667, norm. score wrt baseline: 15.1081:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 28493.1465, Baseline MSE = 833.2123, Normalized = 34.1967<br>
K: Model MSE = 14363.2334, Baseline MSE = 4031.7278, Normalized = 3.5626<br>
Mg: Model MSE = 14529.8545, Baseline MSE = 1499.2853, Normalized = 9.6912<br>
pH: Model MSE = 0.9400, Baseline MSE = 0.0724, Normalized = 12.9821<br>
</p>
<ul>
    <li>PCA with 15 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 16(Val Loss: 0.9003 , norm. score wrt baseline: 0.9744:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 844.2909, Baseline MSE = 833.2123, Normalized = 1.0133<br>
K: Model MSE = 3987.7471, Baseline MSE = 4031.7278, Normalized = 0.9891<br>
Mg: Model MSE = 1444.8723, Baseline MSE = 1499.2853, Normalized = 0.9637<br>
pH: Model MSE = 0.0674, Baseline MSE = 0.0724, Normalized = 0.9315<br>
</p>
<ul>
    <li>PCA with 3 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 17 (norm. score wrt baseline: 1.0033:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 839.4621, Baseline MSE = 833.2123, Normalized = 1.0075<br>
K: Model MSE = 4050.3098, Baseline MSE = 4031.7278, Normalized = 1.0046<br>
Mg: Model MSE = 1533.1549, Baseline MSE = 1499.2853, Normalized = 1.0226<br>
pH: Model MSE = 0.0709, Baseline MSE = 0.0724, Normalized = 0.9785<br>
</p>
<ul>
    <li>PCA with 10 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 18 (norm. score wrt baseline: 1.0495:</h3>
<p> Notes: 10M pixels with rand pca (better GPU used) + warm-up phase + gradient clipping.</p>
<p>
P: Model MSE = 895.3030, Baseline MSE = 833.2123, Normalized = 1.0745 <br>
K: Model MSE = 4197.0293, Baseline MSE = 4031.7278, Normalized = 1.0410 <br>
Mg: Model MSE = 1579.4727, Baseline MSE = 1499.2853, Normalized = 1.0535 <br>
pH: Model MSE = 0.0745, Baseline MSE = 0.0724, Normalized = 1.0292 <br>
</p>
<ul>
    <li>PCA with 5 components</li>
    <li>maks. 10M pixels in pca matrix</li>
    <li>efficientnet_b2, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.Resize((224, 224)),</li>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 19 (gradient exploded -> nan):</h3>
<p> Notes: 1x1 conv with 10 filters, adding padding instead of resize</p>
<p>
Completely wrong predicted values (even < 0)
</p>
<ul>
    <li>1x1 conv with 10 filters</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 20(very high gradient values):</h3>
<p> Notes: 1x1 conv with 10 filters, adding padding instead of resize, different norm method taking into account mask</p>
<p>
Completely wrong predicted values.
</p>
<ul>
    <li>1x1 conv with 10 filters</li>
    <li>different hyperparameters (smaller lr)</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 21(very high gradient values):</h3>
<p> Notes: 1x1 conv with 3 filters, adding padding instead of resize, different norm method taking into account mask</p>
<p>
Completely wrong predicted values.
</p>
<ul>
    <li>1x1 conv with 3 filters</li>
    <li>different hyperparameters (smaller lr)</li>
    <li>efficientnet_b0, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 22(very high gradient values):</h3>
<p> Notes: 1x1 conv with 3 filters, adding padding instead of resize, global normalization (!), training interrupted prematurely</p>
<p>
P: Model MSE = 969.3774, Baseline MSE = 956.1005, Normalized = 1.0139<br>
K: Model MSE = 3404.8650, Baseline MSE = 3448.3214, Normalized = 0.9874 <br>
Mg: Model MSE = 1470.4374, Baseline MSE = 1448.3911, Normalized = 1.0152<br>
pH: Model MSE = 0.0661, Baseline MSE = 0.0677, Normalized = 0.9765<br>
</p>
<ul>
    <li>1x1 conv with 3 filters</li>
    <li>different hyperparameters (smaller lr)</li>
    <li>efficientnet_b0, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>


<h3>Experiment 23:</h3>
<p> Notes: 1x1 conv with 10 filters, adding padding instead of resize, global normalization (!), changed hyperparameters,reasonable values of val loss and training loss</p>
<p>
P: Model MSE = 962.8198, Baseline MSE = 956.1005, Normalized = 1.0070<br>
K: Model MSE = 3423.0977, Baseline MSE = 3448.3214, Normalized = 0.9927<br>
Mg: Model MSE = 1480.3582, Baseline MSE = 1448.3911, Normalized = 1.0221<br>
pH: Model MSE = 0.0671, Baseline MSE = 0.0677, Normalized = 0.9917<br>
</p>
<ul>
    <li>1x1 conv with 10 filters</li>
    <li>different hyperparameters (smaller lr)</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 24:</h3>
<p> Notes: 1x1 conv with 10 filters, adding padding instead of resize, global normalization (!), changed hyperparameters,reasonable values of val loss and training loss</p>
<p>
P: Model MSE = 990.8983, Baseline MSE = 956.1005, Normalized = 1.0364<br>
K: Model MSE = 5301.6675, Baseline MSE = 3448.3214, Normalized = 1.5375<br>
Mg: Model MSE = 1577.3319, Baseline MSE = 1448.3911, Normalized = 1.0890<br>
pH: Model MSE = 0.0746, Baseline MSE = 0.0677, Normalized = 1.1031<br>
</p>
<ul>
    <li>1x1 conv with 15 filters</li>
    <li>different hyperparameters (smaller lr)</li>
    <li>efficientnet_b0, pretrained = False</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 25:</h3>
<p> Notes: Best val loss and training loss learning curves so far (decreasing), 1x1 conv with 3 filters, adding padding instead of resize, global normalization (!), changed hyperparameters,reasonable values of val loss and training loss</p>
<p>
P: Model MSE = 965.4764, Baseline MSE = 956.1005, Normalized = 1.0098<br>
K: Model MSE = 3227.5916, Baseline MSE = 3448.3214, Normalized = 0.9360<br>
Mg: Model MSE = 1480.8820, Baseline MSE = 1448.3911, Normalized = 1.0224<br>
pH: Model MSE = 0.0630, Baseline MSE = 0.0677, Normalized = 0.9312<br>
</p>
<ul>
    <li>1x1 conv with 3 filters</li>
    <li>different hyperparameters (smaller lr)</li>
    <li>convnext_base_in22k, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 26:</h3>
<p> Notes: Best val loss and training loss learning curves so far (decreasing), 1x1 conv with 3 filters, adding padding instead of resize, global normalization (!), changed hyperparameters,reasonable values of val loss and training loss</p>
<p>
P: Model MSE = 961.5493, Baseline MSE = 956.1005, Normalized = 1.0057 <br>
K: Model MSE = 3242.3088, Baseline MSE = 3448.3214, Normalized = 0.9403 <br>
Mg: Model MSE = 1424.8456, Baseline MSE = 1448.3911, Normalized = 0.9837 <br>
pH: Model MSE = 0.0608, Baseline MSE = 0.0677, Normalized = 0.8980 <br>
</p>
<ul>
    <li>1x1 conv with 3 filters</li>
    <li>different hyperparameters (higher lr, batch 32 -> 64)</li>
    <li>convnext_base_in22k, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>v2.RandomHorizontalFlip(p=0.5),</li>
            <li>v2.GaussianNoise(mean=0.0, sigma=0.03)</li>
        </ul>
    </li>
</ul>

<h3>Experiment 27:</h3>
<p> Notes: Best val loss and training loss learning curves so far (decreasing), 1x1 conv with 3 filters, adding padding instead of resize, global normalization (!), changed hyperparameters,reasonable values of val loss and training loss</p>
<p>
P: Model MSE = 987.0714, Baseline MSE = 956.1005, Normalized = 1.0324 <br>
K: Model MSE = 2672.7766, Baseline MSE = 3448.3214, Normalized = 0.7751 <br>
Mg: Model MSE = 1264.7209, Baseline MSE = 1448.3911, Normalized = 0.8732 <br>
pH: Model MSE = 0.0639, Baseline MSE = 0.0677, Normalized = 0.9440 <br>
Overall: 0.9 <br>
</p>
<ul>
    <li>1x1 conv with 3 filters</li>
    <li>different hyperparameters (changed lr for head -> ~10^-3, backbone ~10^-4, reducer ~10^-3, batch 64)</li>
    <li>convnext_tiny_in22k, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>no augmentation </li>
        </ul>
    </li>
</ul>

<h3>Experiment 28:</h3>
<p> Notes: Best val loss and training loss learning curves so far (decreasing), 1x1 conv with 3 filters, adding padding instead of resize, global normalization (!), changed hyperparameters,reasonable values of val loss and training loss</p>
<p>
P: Model MSE = 910.9445, Baseline MSE = 956.1005, Normalized = 0.9528 <br>
K: Model MSE = 2665.4558, Baseline MSE = 3448.3214, Normalized = 0.7730 <br>
Mg: Model MSE = 1275.5963, Baseline MSE = 1448.3911, Normalized = 0.8807 <br>
pH: Model MSE = 0.0590, Baseline MSE = 0.0677, Normalized = 0.8718 <br>
Overall: 0.87 <br>
</p>
<ul>
    <li>1x1 conv with 3 filters</li>
    <li>different hyperparameters (changed lr for head -> ~10^-4, backbone ~10^-5, reducer ~10^-4, weight decay ~10^-3, batch 64)</li>
    <li>convnext_tiny_in22k, pretrained = True</li>
    <li>augmentations for training:
        <ul>
            <li>no augmentation </li>
        </ul>
    </li>
</ul>

  
  
  
  
  
