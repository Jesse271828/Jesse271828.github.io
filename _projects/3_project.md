---
layout: page
title: Q-ary Sparse Fourier Transforms
description: May 2023 - May 2024
img: assets/img/cover_image_3.png
importance: 1
category: machine learning
giscus_comments: false
---

<hr style="border: 1px solid black; width: 100%;">

This project was my first project at BLISS, where I was guided by **<a href='https://erginbas.github.io/'> Efe</a>** and worked on the algorithm they had just published called q-SFT. I understood the algorithm to its mathematical details and worked with the code base to study the problem of **parameter selection** both theoretically and empirically. **I then developed a noise estimator algorithm that is now part of q-SFT**, authomating the selection of peeling noise. **The project is still ongoing in the sense that there are still several statistical questions in alasing, noise estimation, and sensing that I wish to spend more time on. The vision interpretability project is in some sense an applied continuation of this project. All results are included in the report below.** 

<hr style="border: 1px solid black; width: 100%;">

Q-SFT recovers the Fourier basis of a pseudo-boolean set function under sparsity assumptions. A psedo-boolean set function is one such that the input spans all strings of length n over an alphabet of size q, and the output belongs to the reals. For instance, if you have a set of features, then the function that maps weather you enable each feature or not to the joint impact of this combination would be a pseudo-boolean set function. When n becomes significantly large, using FFT to find the Fourier coefficients of this function becomes impossible. However, in the special case when the majority of the Fourier coefficients are zeros (the sparsity property), q-SFT allows fast recovery even for large ns.

On a high level, q-SFT first compresses the input space onto bins of a much lower dimension, then it performs sampling there. If sampling is done correctly, most bins would contain either one or no samples, enabling us to peel off or recover the Fourier coefficients in these bins. By repeating this process many times, the entirety of the Fourier basis can be recovered. 

The noise selection algorithm uses the fact that q-SFT fails different when different, incorrect noises are used for peeling. Peeling noise sets a threshold, and this threshold determines weather a bin is incorrectly detected as one that contains multiple samples or zero sample. By observing the detections and performing a golden search, one can find the optimal threshold for peeling. 

There are still many questions to be answered in q-SFT. For instance, what is the optimal way of compressing the input space into bins, or how good the noise estimator perfroms asympototically. Some of these questions are important while others are not. Maybe I will never get to answer most of them, but I'm continuously working toward them. 

<html>

<head>
    <title>PDF in HTML</title>
</head>
<style>
    .pdf {
        width: 100%;
        aspect-ratio: 4 / 3;
    }
    .pdf,
    html,
    body {
        height: 100%;
        margin: 0;
        padding: 0;
    }
   h1,
    h3 {
        text-align: center;
    }

    h1 {
        color: green;
    }
</style>

<body>
        <iframe class="pdf" 
                src=
"https://wjingxing.github.io/assets/pdf/qsft.pdf"
            width="800" height="500">
        </iframe>
</body>

</html>

**End**
