# CG-method for TV-like regularization
We implement an algorithm, leveraging the [conjugate gradient(CG) method](https://en.wikipedia.org/wiki/Conjugate_gradient_method#The_resulting_algorithm) to solve the inverse problem
$$Ax\approx y^\delta$$
with a [total-variation-like regularization](https://en.wikipedia.org/wiki/Total_variation_denoising#2D_signal_images), specifically, we minimize
$$L:=\frac{1}{2}\|Ax-y^\delta\|_2^2 +  \frac{\lambda}{2} \|\nabla x\|_2^2,$$
where $\nabla x$ denotes the spatial derivative of $x$.

We assume $A\in\mathbb{R}^{m\times n^2}$ to be the forward operator and $x\in\mathbb{R}^{n^2}$ to be a vectorized $n\times n$ gray-scale image.