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
  
