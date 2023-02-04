# Generative-adversarial-network
The objective of my personal project is to create person face not existing in this world.Fake perfect faces,technically perfect sharp faces were the point behind it.It was preexisting idea but it came to me after i studied convolution neural network.I studied of Deconvolution and how it can be used to verify neural network related output.For eg Facial verification code is done CNN use use weightsnot directly to create reference image to verify it, image can be seen through deconvolution.

I used idea about using deconvolution network as generator and using basic verifying network for checking if image is real or not as discriminator.By combining this two GAN network is formed.The GAN network improves over time it starts creating from noise to perfect face after using GAN network.As generator and discriminator both train simultaenously one at a each time to perfact faces from noise.

The joined DCGAN is built by adding the discriminator on the top of the generator.
Before compiling the full setup, we have to set the discriminator model not to be trainable. This will freeze its weights and tell that the only part of the full network that needs to be trained, is the generator.
Although we compile the discriminator we don’t need to compile the generator model because we do not use the generator on its own.
This order ensures that the discriminator is updated at the right time and frozen when it has to be. Therefore if we train the whole model, it will just update the generator, and when we train the discriminator, it will only update the discriminator.

Botyh train on label 0 AND 1 for fake faces and real faces
