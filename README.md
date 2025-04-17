# HKUMX-Survival
## Preliminary (Multi-Instance Learning)

**Motivation**: Whole Slide Images are too large for end-to-end pathological tasks (e.g., classifcaiton, survival analysis,...).

**Solution**: To address this challenge, MIL methods first downsample patches into a feature space using pre-trained feature extractors, including traditional models (like ResNet pretrained on ImageNet) and foundation models (models trained on pathology images using pre-training techniques such as Masked Autoencoders (MAE) and Contrastive Language-Image Pretraining (CLIP)).

After extracting patch-level feature embeddings, these can be integrated into slide-level representations using MIL models. A straightforward approach is to compute the mean of the patch-level features to obtain the slide-level representation.

Optional Reading: https://github.com/peterlipan/Awesome-Multi-instance-Learning-for-Whole-Slide-Images



**GPU server:**

Remote Server (Host/IP/URL): research15.saas.hku.hk
Port: 22
Username: r15user15 
Password: Maximus+226 (case-sensitive)

Path to the slides: /home/medshare/WSI/SARC_sorted



## Data preprocessing

Following  the steps in CLAM (https://github.com/mahmoodlab/CLAM), create_patches_fp.py then extract_features_fp.py to transfer each .svs slide to .pt feature file.



## Model Training

https://github.com/peterlipan/qmh
