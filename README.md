# Oedipus Captcha Solver

Solves captcha generated by the [Sphinx Captcha Generator](https://github.com/DavidPierre21/sphinx-captcha)

### Example of captcha:

![1](https://github.com/davidpierre21/oedipus/raw/master/samples/ABPK_48a4.jpg)
![2](https://github.com/davidpierre21/oedipus/raw/master/samples/MPCY_ee70.jpg)
![3](https://github.com/davidpierre21/oedipus/raw/master/samples/RYUM_a4d6.jpg)

## How to use:
Install the requirements using:
```
pip install -r requirements.txt
```
### Executing:
To train the neural network, run:
```
python train.py
```

some few arguments are:
```
usage: train.py [-h] [--epochs EPOCHS] [--verbose VERBOSE] [--gpu]
                [--gpu-false]

Neural Network to break captchas

optional arguments:
  -h, --help         show this help message and exit
  --epochs EPOCHS    Number of epochs to be executed
  --verbose VERBOSE  Show data at each N value
  --gpu-false        forces model to run on CPU
```

---

After the neural network is trained you can predict images by executing:
```
python predict.py --path path/to/image
```
Some other few arguments are:
```
usage: predict.py [-h] --path PATH [--debug]

Predict captchas using CNN

optional arguments:
  -h, --help            show this help message and exit
  --path PATH, -p PATH  Path to the captcha image
  --debug               Run in debug mode

```

### Based on [Skyduy](https://github.com/skyduy/CNN_keras)'s model