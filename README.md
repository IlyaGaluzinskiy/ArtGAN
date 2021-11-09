## Art generator (GAN)

### Generative adversarial Network for new art generation, built using PyTorch
- Dataset - Kaggle dataset ["Best Artworks of All Time"](https://www.kaggle.com/ikarus777/best-artworks-of-all-time).
- GAN was trained on the Impressionism and Post-Impressionism artworks (2400+ images).
- Training was done using [Google Colab](https://colab.research.google.com/) (basic) and took approximately 3 hours.
- Super-resolution [ISR](https://github.com/idealo/image-super-resolution) was applied to chosen pictures (result of GAN work).

#### Descriminator: 2,765,568 parameters
Discriminator architecture:

Images with a shape [3, 64, 64] -> Conv2d -> LeakyReLU activation ->

-> 3 blocks of [Conv2d -> BatchNorm2d -> LeakyReLU activation] ->

-> Conv2d -> Sigmoid activation -> Classification (Real data or created by generator)

Loss function: Binary Cross Entropy

#### Generator: 3,576,704 parameters
Generator architecture:

Random input with a shape [100, 1, 1] ->

-> 4 blocks of [Conv2d -> BatchNorm2d -> LeakyReLU activation] ->

-> Conv2d -> Tanh activation -> Generated images with a shape [3, 64, 64]

Loss function: Binary Cross Entropy

### Examples of GAN art:

![x4](https://user-images.githubusercontent.com/74296883/138862894-58ebada9-aa3e-4750-970f-20e4864cb075.jpg)
![x4-2](https://user-images.githubusercontent.com/74296883/138862925-e56755c2-e3bb-4f7f-a17b-aeabb1e3ea06.jpg)

#### This project was completed by:
- https://github.com/IlyaGaluzinskiy
- https://github.com/plazinho
- https://github.com/aabdysheva
