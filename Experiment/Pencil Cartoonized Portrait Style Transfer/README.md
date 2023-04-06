# Pencil Cartoonized Portrait Style Transfer <br/>
I am using PyTorch to explore the workings of Generative Adversarial Networks (GANs) and experimenting with fine-tuning StyleGANs for style transfer. Specifically, I am interested in using StyleGANs to transfer the style of a portrait photo to a pencil cartoon portrait.

StyleGANs are a type of GAN that are known for their ability to generate highly realistic images. They work by training a generator and a discriminator network in an adversarial manner, where the generator tries to generate images that fool the discriminator into thinking they are real, while the discriminator tries to distinguish between real and fake images.

Fine-tuning a pre-trained StyleGAN allows us to adjust the network to generate images that conform to a specific style or artistic preference. In my case, I am using a pre-trained StyleGAN to transfer the style of a portrait photo to a pencil cartoonized portrait.

The process of style transfer involves finding a way to combine the content of one image (the portrait photo) with the style of another image (the pencil cartoon) to create a new image that reflects both. One way to achieve this is to use a pre-trained convolutional neural network (CNN) to extract features from both the content and style images. These features are then used to define a loss function that guides the optimization process to create a new image that minimizes this loss.

To transfer the style of a pencil cartoon to a portrait photo, I would first feed both images into the pre-trained CNN to extract their features. Next, I would calculate the mean and covariance of the feature representations of the style image and use this information to compute a style loss. This style loss is then combined with a content loss that measures the difference between the feature representations of the portrait photo and the generated image. The final loss is a weighted combination of the content and style losses, which is used to update the generator network until the generated image has converged to an optimal solution.

The result of this process is a new image that reflects the content of the portrait photo with the style of a pencil cartoon, resulting in a striking, visually compelling image. By leveraging the power of StyleGANs and PyTorch, we can create highly realistic, stylized images that blur the line between reality and artistic expression.


check out the slide [Pencil Cartoonized Portrait Style Transfer with JoJoGAN](https://github.com/ppoompich/myprojects/blob/main/JoJoGAN%20experiment/Pencil%20Cartoonized%20Portrait%20Style%20Transfer%20with%20JoJoGAN.pdf)<br/>

this projects base on JoJoGANs
JoJoGANs are a type of Generative Adversarial Networks (GANs) that have the ability to add and style a photo using a single reference image. They require less time to train compared to other GANs. I have been experimenting with JoJoGANs to study the field of Convolutional Image in Deep Learning. For more details, please refer to the slide that I have uploaded.<br/>
Original JoJoGAN paper ->> [JoJoGAN: One Shot Face Stylization](https://arxiv.org/abs/2112.11641).<br/>
