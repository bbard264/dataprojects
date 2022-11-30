# JoJoGAN: One Shot Face Stylization

This is the experiment of [JoJoGAN: One Shot Face Stylization](https://arxiv.org/abs/2112.11641).

>**Abstract:**<br>
While there have been recent advances in few-shot image stylization, these methods fail to capture stylistic details
that are obvious to humans. Details such as the shape of the eyes, the boldness of the lines, are especially difficult
for a model to learn, especially so under a limited data setting. In this work, we aim to perform one-shot image stylization that gets the details right. Given
a reference style image, we approximate paired real data using GAN inversion and finetune a pretrained StyleGAN using
that approximate paired data. We then encourage the StyleGAN to generalize so that the learned style can be applied
to all other images.

## Download Models
checkpoints:
- [stylegan2-ffhq-config-f.pt](https://drive.google.com/file/d/1Yr7KuD959btpmcKGAUsbAk5rPjX2MytK/)
- [e4e_ffhq_encode.pt](https://drive.google.com/file/d/1o6ijA3PkcewZvwJJ73dJ0fxhndn0nnh7/)
- [restyle_psp_ffhq_encode.pt](https://drive.google.com/file/d/1nbxCIVw9H3YnQsoIPykNEFwWJnHVHlVd/)
- [dlibshape_predictor_68_face_landmarks.dat](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)

pretrained style models (optional):
- [arcane_caitlyn.pt](https://drive.google.com/file/d/1gOsDTiTPcENiFOrhmkkxJcTURykW1dRc/)
- [arcane_caitlyn_preserve_color.pt](https://drive.google.com/file/d/1cUTyjU-q98P75a8THCaO545RTwpVV-aH/)
- [arcane_jinx_preserve_color.pt](https://drive.google.com/file/d/1jElwHxaYPod5Itdy18izJk49K1nl4ney/)
- [arcane_jinx.pt](https://drive.google.com/file/d/1quQ8vPjYpUiXM4k1_KIwP4EccOefPpG_/)
- [arcane_multi_preserve_color.pt](https://drive.google.com/file/d/1enJgrC08NpWpx2XGBmLt1laimjpGCyfl/)
- [arcane_multi.pt](https://drive.google.com/file/d/15V9s09sgaw-zhKp116VHigf5FowAy43f/)
- [sketch_multi.pt](https://drive.google.com/file/d/1GdaeHGBGjBAFsWipTL0y-ssUiAqk8AxD/)
- [disney.pt](https://drive.google.com/file/d/1zbE2upakFUAx8ximYnLofFwfT8MilqJA/)
- [disney_preserve_color.pt](https://drive.google.com/file/d/1Bnh02DjfvN_Wm8c4JdOiNV4q9J7Z_tsi/)
- [jojo.pt](https://drive.google.com/file/d/13cR2xjIBj8Ga5jMO7gtxzIJj2PDsBYK4/)
- [jojo_preserve_color.pt](https://drive.google.com/file/d/1ZRwYLRytCEKi__eT2Zxv1IlV6BGVQ_K2/)
- [jojo_yasuho.pt](https://drive.google.com/file/d/1grZT3Gz1DLzFoJchAmoj3LoM9ew9ROX_/)
- [jojo_yasuho_preserve_color.pt](https://drive.google.com/file/d/1SKBu1h0iRNyeKBnya_3BBmLr4pkPeg_L/)
- [art.pt](https://drive.google.com/file/d/1a0QDEHwXQ6hE_FcYEyNMuv5r5UnRQLKT/)

## Evaluate a Pretrained Style Model on Image
Download the pretrained style model and put it under the `models` folder like in the diagram shown above. Put the input image in the `test_input` folder, in the following `image_name`, you don't need to provide the file path, just the file name.

```sh
python evaluate.py --input <image_name> --model_name <model_name> --seed <random_seed> --device <cuda/cpu>
```
eg.
```
python evaluate.py --device cuda --input iu.jpeg --model_name jojo --seed 3000
```

## Train a Custom Model
Add images with the same style into the folder `style_images`. See inside the folder for example.

```sh
python train_mystyle.py --model_name <new_name> --alpha <alpha_value> --preserve_color <True/False> --num_iter <number_of_iterations> --device <cuda/cpu>
```
- `model_name`: give your new model a name, maybe based on the style images?
- `alpha`: the alpha value that'll determine the strength of the style. `0` = strongest, `1` = weakest. Float value between 0 and 1
- `preserve_color`: To whether preserve the color from the style images. This should be a boolean `True` or `False`
- `num_iter`: Number of iterations for the training. Usually `300` ~ `500` iter would be fine
- `device`: If you don't have NVIDIA GPU with CUDA, use `cpu`. Otherwise, `cuda` (basically the default and you don't need to declare)

eg.
```
python train_mystyle.py --model_name custom --alpha 0.0 --preserve_color False --num_iter 300 --device cuda
```
To evaluate the model, follow the previous step will do, just change the `model_name` to the one you just created. It'll just be like:
```
python evaluate.py --device cuda --input iu.jpeg --model_name custom --seed 3000
```

## How to use
Everything to get started is in the [colab notebook](https://colab.research.google.com/github/mchong6/JoJoGAN/blob/main/stylize.ipynb).

## Citation
If you use this code or ideas from our paper, please cite our paper:
```
@article{chong2021jojogan,
  title={JoJoGAN: One Shot Face Stylization},
  author={Chong, Min Jin and Forsyth, David},
  journal={arXiv preprint arXiv:2112.11641},
  year={2021}
}
```

## Acknowledgments
This code borrows from [StyleGAN2 by rosalinity](https://github.com/rosinality/stylegan2-pytorch), [e4e](https://github.com/omertov/encoder4editing). Some snippets of colab code from [StyleGAN-NADA](https://github.com/rinongal/StyleGAN-nada)
