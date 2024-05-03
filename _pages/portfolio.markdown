---
title: Portfolio
permalink: /portfolio/
classes: wide
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


# Dual-Sequence Net

**Summary**:
Human thinking process is inherently dual in nature: Like while we are chopping an onion (local/actual actions), we might "mind-wander" and think what if we wathced TV instead? (remote/virtual plan). To model such a process, we simulated a biological neural network to test our theory. We showed that sequential firing of neurons can support such dual coding, and published our results in *eLife*.

**Methods**:
Theoretical Modelling with Differential Equations, Numerical Simulation, Non-linear Classifiers, Synaptic Learning Rules, Time-series Analysis.

**Implementations**: 
Python (NumPy, PyTorch, Pandas, SciPy, Matplotlib), SQL

**Collaborators**: 
[Prof. Christian Leibold](https://www.bio.uni-freiburg.de/groups/leibold-en)

**Publication**: 
[*eLife*, 2023](https://elifesciences.org/articles/86837)




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


# Brain Data Science

**Summary**:
We proposed [a network model of dual processes](#dual-sequence-net), but is it actually how our brain works? By analyzing the brain data of rodents recorded by microelectrodes, we were able to prove that such dual coding exists, and published our results in *The Journal of Neurosciences*.

**Methods**: 
Circular Statistics, Regression Analysis, Hypothesis Testing, Linear classifiers, Time-series Analysis, Bayesian Parameter Estimation.

**Implementations**: 
Python (NumPy, Pandas, SciPy, Matplotlib), MATLAB, SQL

**Collaborators**: 
[Prof. Christian Leibold](https://www.bio.uni-freiburg.de/groups/leibold-en), [Prof. Jill Leutgeb](https://biology.ucsd.edu/research/faculty/jleutgeb)

**Publication**: 
[*The Journal of Neurosciences*, 2022](https://www.jneurosci.org/content/42/11/2282)


<figure style="width: 600px; margin: 10px;">
    <img src="/assets/images/exp_raw_data_base.png" alt='image 1' />
    <figcaption>Data set: Raw EEG time-series data (Left) and extracted spike events (Right). </figcaption>
</figure>

<figure style="width: 600px; margin: 5px;">
    <img src="/assets/images/exp_results.png" alt='image 1' />
    <figcaption>Methods: Data processing and visualization, time-series analysis, regression and hypothesis testing. See our <a href="https://www.jneurosci.org/content/42/11/2282">paper</a> for more details.</figcaption>
</figure>






