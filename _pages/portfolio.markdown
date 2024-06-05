---
title: Portfolio
permalink: /portfolio/
classes: wide
toc: true
---

<style>
p {
    font-size: 12px;
}
.container {
    display: flex;
    justify-content: space-around;
    align-items: flex-start; /* Ensures alignment at the top even if one is taller */
}

img {
    width: 100%;
    height: auto; /* Maintains aspect ratio */
}

figcaption {
    text-align: left; /* Aligns caption text to the left */
}
</style>

<br>
<br>

# Imitative Navigator
2023-24
<div class="container">
    <figure style="width: 350px; margin: 10px;">
        <img src="/assets/images/iminav/breakroom.png" alt='image 1' />
        <figcaption>The environment of the robotic simulation. The robot (top right) needs to navigate to the bottom left corner.</figcaption>
    </figure>
    <figure style="width: 450px; margin: 10px;">
        <img src="/assets/images/iminav/iminav.gif" alt='image 2' />
        <figcaption> (Top left) In robotics, a simple room is already too complex for a random policy to reach the goal. After showing the demo to the RL agent (top right), the agent learned the demo policy (bottom left), which was later fine-tuned to be optimal (bottom right). </figcaption>
    </figure>
</div>

**Summary**:
When applying reinforcement learning (RL) to robotic problems, it is often time-intensive to train a policy from scratch, since the sparse reward signal cannot be sampled efficiently. One solution is to "jump-start" the training by showing the agent how the task is "roughly" done, albeit in a suboptimal way. Given some prior knowledge, the agent can quickly sample the reward, and further fine-tune the policy. 

For that I implemented an Imitation Learning algorithm, called AWAC (Advantage Weighted Actor Critic), to solve the problem in the context of spatial navigation. It significantly reduced the training time by demonstrations of an easy-to-implement policy (object-avoidance). It was the first instance that imitation leraning was applied to a spatial navigation problem. The algorithm can  be applied to a wide range of RL problems.

**Methods**:
Deep Reinforcement Learning (PyTorch), Numerical Simulation (NumPy), Robotic Simulator (Webots, Python), Computer Vision (OpenCV & pretrained CNNs), Classical Machine Learning.

**GitHub repo**: <https://github.com/yyhhoi/ImiNav>

<br>
<br>


# Dual-Sequence Net
2021-2023
<div class="container">
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/dirnet_animation_base.gif" alt='image 1' />
        <figcaption>The agent thinks of the immediate action plan (local & actual movement) and althernative choices (remote & virtual pathways) during spatial navigation. Colored dots are neural activities. </figcaption>
    </figure>
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/dirnet_model.png" alt='image 2' />
        <figcaption>The neural network model. Two layers of place cells producing local and remote sequences. </figcaption>
    </figure>
</div>

**Summary**:
Human thinking process is inherently dual in nature: While we were chopping an onion (local/actual actions), we might "mind-wander" and think what if we wathced TV instead? (remote/virtual plans). To model such a process, we simulated a biological neural network to test our theory. We showed that sequential firing of neurons can support such dual coding, and published our results in *eLife*.

**Methods**:
Mathematical Modelling of Complex Systems, Numerical Simulation (Python, C++), Classical Machine Learning, Synaptic Learning Rules, Time-series Analysis.


**Publication**: Yiu, Y.-H., & Leibold, C. (2023). A theory of hippocampal theta correlations accounting for extrinsic and intrinsic sequences. eLife, 12, RP86837. <https://doi.org/10.7554/eLife.86837.4>


<br>
<br>


# Brain Data Science
2019-22
<figure style="width: 600px; margin: 10px;">
    <img src="/assets/images/exp_raw_data_base.png" alt='image 1' />
    <figcaption>Data set: Raw EEG time-series data (Left) and extracted spike events (Right). </figcaption>
</figure>

<figure style="width: 600px; margin: 5px;">
    <img src="/assets/images/exp_results.png" alt='image 1' />
    <figcaption>Cross-correlation of spike trains demonstrates the existence of both local (A-B) and non-local (C) spike sequences as the heterogeneous components of neural representation (D). See our <a href="https://www.jneurosci.org/content/42/11/2282">paper</a> for more details.</figcaption>
</figure>

**Summary**:
We proposed [a network model of dual processes](#dual-sequence-net), but is it actually how our brain works? By analyzing the brain data of rodents recorded by microelectrodes, we were able to prove that such dual coding exists, and published our results in *The Journal of Neurosciences*.

**Methods**: 
Circular Statistics, Regression Analysis, Hypothesis Testing, Linear and Non-Linear Classifiers, Time-series Analysis, Bayesian Parameter Estimation.

**Publication**: 
Yiu, Y.-H., Leutgeb, J. K., & Leibold, C. (2022). Directional Tuning of Phase Precession Properties in the Hippocampus. The Journal of Neuroscience, 42(11), 2282–2297. <https://doi.org/10.1523/JNEUROSCI.1569-21.2021>

<br>
<br>


# Latent Gait Patterns
2019
<div class="container">
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/gait/Network.png" alt='image 1' />
        <figcaption>Network architecture. Pose sequences (inferred from walking videos) were compressed into low-dimensional latent space using VAEs, with auxiliary classification tasks to improve the embedding quality. </figcaption>
    </figure>
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/gait/Latents.png" alt='image 2' />
        <figcaption>Walking sequences (left) can be generated by sampling from the trained latent space (right). Some clusters demonstrate pathological walking patterns. Diagnosis could be made by evaluating the distance of a walking video to the pathological clusters (such as through a KNN classifier) in the latent space.</figcaption>
    </figure>
</div>

**Summary**: People with vertigo and balance disorders often exhibit abnormal gait patterns while walking, such as staggering or overly rigid motion. Here, we employed generative models such as Variational Autoencoders (VAEs) to extract the latent variables underlying these pathological walking patterns.

In cooperation with LMU clinics, we gained access to thousands of walking videos of patients. After training the VAEs on these videos, we found that pathological walking patterns were clearly clustered in the latent space. Such a representation can aid in video-based diagnosis without relying on clinical assessment.

**Methods**: Deep Learning (PyTorch), Computer Vision (OpenCV), Data Processing, Data Augmentation

**Article**:
[MSc Thesis link](https://www.researchgate.net/publication/381114885_Deep_Spatio-Temporal_Representation_Learning_of_Gait_Signals_in_Patients_with_Vertigo_and_Balance_Disorders)

**GitHub repo**: <https://github.com/yyhhoi/gait>

<br>
<br>



# DeepVOG
2018-19
<figure style="width: 500px; margin: 10px; text-align: center;">
    <img src="/assets/images/deepvog/deepvog.gif" alt='image 1' />
    <figcaption>Video-based Gaze estimation (Left) via semantic segmentation (Right, pixel-wise classification of the pupil area).</figcaption>
</figure>

<div class="container">
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/deepvog/Network.png" alt='image 1' />
        <figcaption>Netowrk architecture. A U-net schema with CNNs for semantic segmentation of eye pupil from images. </figcaption>
    </figure>
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/deepvog/3Dmodel.png" alt='image 2' />
        <figcaption>Using computational geometry to fit a 3D eye-ball model from a series of segmented 2D ellipses, enabling gaze direction estimation. </figcaption>
    </figure>
</div>


**Summary**: Conventional eye-tracking algorithms failed to detect eye movements in dark and noisy camera videos, such as when recorded inside an MRI machine. To solve the problem, we developed a deep-learning based eye tracking model for noisy camera feeds. 

The network was trained on clinical eyetracking images provided by LMU clinics. It performs semantic segmentation on eye pupil area and fit a 3D eye-ball model to estimate the gaze. The network generalizes well to other data sets. A Docker image is available for easy deployment of the model.

**Methods**: Deep Learning (TensorFlow, Keras), Computer Vision (OpenCV), Data Augmentation (Keras), Synthetic Data Generation (Blender), Data Processing.

**Publication**: 
Yiu, Y.-H., Aboulatta, M., Raiser, T., Ophey, L., Flanagin, V. L., zu Eulenburg, P., & Ahmadi, S.-A. (2019). DeepVOG: Open-source pupil segmentation and gaze estimation in neuroscience using deep learning. *Journal of Neuroscience Methods*, 324, 108307. <https://doi.org/10.1016/j.jneumeth.2019.05.016>

**GitHub repo**: <https://github.com/pydsgz/DeepVOG>