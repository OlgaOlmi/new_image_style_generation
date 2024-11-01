# New image style generation based on pseudo-random variation of the reduced VQGAN latent space for a specific image

This notebook demonstrates the use of VQGAN with my LatentAutoEncoder to generate image latent spaces 
produced by VQGAN and reduced by the LatentAutoEncoder, 
along with a variation algorithm for the reduced latent space to create new image appearances.

To try it out, download the pre-trained model of the LatentAutoEncoder "model_aenc_vqgan_4out_6st.cnn" 
from https://drive.google.com/drive/folders/1t64Hgy_FUbZlrM7nksyTklrVmxOVCB-I?usp=sharing and move it to the '/data' folder.

The model was trained on a GPU.
