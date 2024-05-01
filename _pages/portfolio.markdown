---
title: Portfolio
permalink: /portfolio/
classes: wide
---


## Directional Net (2023)
<!--
#TODO: Reduce the Gif's caption length by indicating the "Online"/"Remote" directly in the animation.
#TODO: Remove "Nth theta cycle".
-->

<style>
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

<div class="container">
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/dirnet_animation_base.gif" alt='image 1' />
        <figcaption>Neural activity sequences representing the immediate action plan (local movement, arrow), and the remote alternative pathways (virtual plans), in spatial navigation. </figcaption>
    </figure>
    <figure style="width: 400px; margin: 10px;">
        <img src="/assets/images/dirnet_model.png" alt='image 2' />
        <figcaption>The neural network model. Local sequence is produced by local recurrence between neurons (place cells). Remote sequence is played out by remote projections, learnt from past experiences via learning rules. </figcaption>
    </figure>
</div>


Human thinking process is inherently dual in nature: One is "local/actual", and the another is "remote/virtual". Like while we are chopping an onion, we also "mind-wander" about what if we make a soup today instead? Or buying a house in the future?

To model such a memory function, we **developed a mathematical framework** and **simulated the dynamics of a biological neural network** (see figures). We applied methods such as **predictive classifiers**, **time-series analysis** and **bayesian parameter estimation** on the simulated neural data to prove our hypothesis. We demonstrated that sequential firing of neurons can support such dual coding, and published our results in a highly-recognized scientific journal [*eLife*](https://elifesciences.org/articles/86837).





