---
{"dg-publish":true,"permalink":"/atlas/vae/","noteIcon":"","updated":"2024-10-29T17:52:46.132-07:00"}
---


## Variational Autoencoder

A [Variational Autoencoder](https://en.wikipedia.org/wiki/Variational_autoencoder) is a type of neural network that is generative network that maps points in the input domain to points in the [latent space]() of the network, and then maps the latent space back to a point in the output domain.

Yeah, okay, so let's talk a bit more in English. It's comprised of two parts, the encoder and the decoder. I like to think of this as if it's a file format.

Let's pretend that we are talking about a JPG. The input domain for a JPG is the pixel data. it's a 2D matrix of color for each pixel in the image. The latent space (roughly) is the JPG file format that uses formulas to reduce the size of the JPG. So the encoder takes the pixel data, and turns it into the JPG format.

The decoder reads the JPG format and then turns it back into the pixel data, but it's not the exact same pixel data because we lose some data in the encoding, but it's close enough for humans so see little difference.

That's basically what an VAE does, except that you have to train it on the image data that you care about so we create a very optimized encoding method for our specific type of data.

## Why VAE?

Why are we covering such an old technique of machine learning?

I want to cover VAEs because I think they give you a very nice conceptual basis for neural networks and how they all work.

They are simple enough to understand the concepts and the architecture of the network without getting too deep in the weeds, and then you see how magical things feel.

