
```console
nvidia-docker run -it -v "$HOME/Downloads":/workspace/cyclegan/datasets/datasets -v "$HOME/Desktop/checkpoints":/workspace/cyclegan/checkpoints tiao/cyclegan-pytorch
```

```console
$ python train.py --dataroot ./datasets/datasets/horse2zebra --name horse2zebra_cyclegan --model cycle_gan --gpu_id 0 --display_id -1
```