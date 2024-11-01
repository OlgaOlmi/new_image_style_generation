# New image style generation based on pseudo-random variation of the reduced VQGAN latent space for a specific image

This notebook demonstrates the use of VQGAN with my LatentAutoEncoder to generate image latent spaces 
produced by VQGAN and reduced by the LatentAutoEncoder, 
along with a variation algorithm for the reduced latent space to create new image appearances.

The LatentAutoEncoder is a reduced autoencoder for the VQGAN latent space. It compresses the VQGAN representation from 256 
numbers per image patch to 4 numbers per patch while reconstructing the original VQGAN latent space with high quality.
The concept behind new image style generation is as follows: if we can reconstruct the full VQGAN latent space from a 
significantly reduced latent space with fewer parameters per patch, we can explicitly vary this smaller set of parameters, 
which will, in turn, implicitly vary the full latent space. This allows us to change the image’s appearance while 
maintaining an accurate representation of objects. For details, see the article on https://medium.com/@olga.mindlina/new-image-style-generation-using-autoencoders-practical-experiments-with-vqgan-latent-space-9337cfffcf98

To try it out, download the pre-trained model of the LatentAutoEncoder "model_aenc_vqgan_4out_6st.cnn" 
from https://drive.google.com/drive/folders/1t64Hgy_FUbZlrM7nksyTklrVmxOVCB-I?usp=sharing and move it to the '/data' folder.

The model was trained on a GPU.
