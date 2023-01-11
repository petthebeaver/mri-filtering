# mri-filtering
# sr-tomography
implementation of an algorithm for removing noise in tomography images taken as part of a linear algebra course at AI Masters


## Постановка задачи
Магнитно-резонансная томография (МРТ) - это метод получения 3D снимков внутренних органов за счет картирования времени спиновых релаксаций с присутствием шумовых компонент с распределением Райса (Rice distribution).
<p align="center">
  <img src="https://github.com/Alexkkir/sr-tomography/blob/main/images/overview.png](https://github.com/petthebeaver/MRI-NLSD-denoising/blob/8db6b011043c0c6785576eb65549e728857cea73/images/overview.png" />
</p>
  
In this repository I implement the algorithm proposed in [Non-Local SVD Denoising of MRI Based on Sparse Representations
](https://www.mdpi.com/1424-8220/20/5/1536/htm)

## Main methods
The algorithm consists mainly of three parts

1. Variance-Stabilization Transformation

<p align="center">
  <img src="[https://github.com/pettheberaver/mri-filtering/blob/main/images/vst.png](https://github.com/petthebeaver/MRI-NLSD-denoising/blob/8db6b011043c0c6785576eb65549e728857cea73/images/vst.png)" />
</p>
   
2. KSVD matrix decomposition

<p align="center">
  <img src="https://github.com/pettheberaver/mri-filtering/blob/main/images/ksvd.png" />
</p>
  
3. None-local filtering

<p align="center">
  <img src="https://github.com/pettheberaver/mri-filtering/blob/main/images/nonlocal.png" />
</p>
  
## Pipeline
This figure briefly describes main steps of the algorithm
![pipeline](images/pipeline.png)

## Results at every step of the algorithm
Incremental reduction of noise at every step of the algorithm is shown below
![tmp](images/tmp.jpg)

## Comparison with other methods
In the figure below proposed algorithm is compared to other methods of MRI denoising [Super-Resolution on IXI
](https://paperswithcode.com/sota/super-resolution-on-ixi)

![methods](images/methods.jpg)
