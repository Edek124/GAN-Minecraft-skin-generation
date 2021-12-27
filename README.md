This repository contains Python scripts that make use of PyTorch library to train a [generative adversarial network](https://en.wikipedia.org/wiki/Generative_adversarial_network)
model that can be used for generating Minecraft skins and
Python scripts that make use of Kivy to create an GUI app that allows for easy use of trained model to generate skins.

## Downloading and setting up Skin Generator

If you want to use the Skin Generator you should download this [zip file](https://drive.google.com/file/d/16OfjeeTLCeMnOgVtRjZAVkWzSHl3KNmn/view?usp=sharing).
After unzipping you can run SkinGenerator.py in order to launch the application. Keep in mind that in order to work SkinGenerator.py script needs to be in the same
directory as gen_model.dat (file containing weights and biases for network), UI_elements directory (contains pngs with ui elements) and temp_files directory
(deleting generated_skin.png from this directory will result in crash on launch, if deleted by mistake can be replaced with any 64x64 pixel png with name generated_skin.png)

In order to run the script you will need Python 3.7 and following packages installed:

[PyTorch](https://pytorch.org)

[Kivy](https://kivy.org/doc/stable/gettingstarted/installation.html)

[Pillow](https://pillow.readthedocs.io/en/stable/installation.html)

Unforunately going through dependency hell and making this into an exe file is too much for me, but please let me now if you somehow achive this.

## Using Skin Generator

Skin Generator is an window appliction. On the right is skin preview which shows how current skin looks like. Use arrows to turn the skin around.
Use random button to fill input vector to network with random numbers between -1 and 1 and generate random skin. Save button saves skin as png
in the same directory as SkinGenerator.py. Exit button exits the application. Input vector consists of 128 numbers. Each of 16 main sliders can be used to
set the same number to each of 8 neighbouring numbers in vector. Button under a slider gives you access to 8 more secondary sliders so you can change each
number form 8 element set independently.


