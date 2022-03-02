# Video Frame Interpolation Transformer

This repo is the official implementation of 'Video Frame Interpolation Transformer', CVPR 2022 [Paper](https://arxiv.org/pdf/2111.13817.pdf).

## Packages
The following pakages are required to run the code:
* python==3.7.6
* pytorch==1.5.1
* cudatoolkit==10.1
* torchvision==0.6.1
* cupy==7.5.0
* pillow==8.2.0
* einops==0.3.0

## Video
To be upload.


## Train
* Download the [Vimeo-90K septuplets](http://toflow.csail.mit.edu/) dataset. 
* Then train VFIT-B using default training configurations:

```
python main.py --model VFIT_B --dataset vimeo90K_septuplet --data_root <dataset_path>
```
Training VFIT-S is similiar to above, just change ```model``` to VFIT_S.

## Test
After training, you can evaluate the model with following command:
```
python test.py --model VFIT_B --dataset vimeo90K_septuplet --data_root <dataset_path> --load_from checkpoints/model_best.pth
```
We also provide our model weight here [weight](https://drive.google.com/drive/folders/1FMQv9VuoexlinzjZ4vuGEZAZDgywzH9T?usp=sharing).

More datasets for evaluation:
* [UCF](https://www.google.com/url?q=https%3A%2F%2Fwww.dropbox.com%2Fs%2Fdbihqk5deobn0f7%2Fucf101_extracted.zip%3Fdl%3D0&sa=D&sntz=1&usg=AFQjCNE8CyLdENKhJf2eyFUWu6G2D1iJUQ)
* [Davis](https://www.google.com/url?q=https%3A%2F%2Fwww.dropbox.com%2Fs%2F9t6x7fi9ui0x6bt%2Fdavis-90.zip%3Fdl%3D0&sa=D&sntz=1&usg=AFQjCNG7jT-Up65GD33d1tUftjPYNdQxkg)


Please consider citing this paper if you find the code and data useful in your research:
```
@article{shi2021video,
  title={Video Frame Interpolation Transformer},
  author={Shi, Zhihao and Xu, Xiangyu and Liu, Xiaohong and Chen, Jun and Yang, Ming-Hsuan},
  journal={arXiv preprint arXiv:2111.13817},
  year={2021}
}
```