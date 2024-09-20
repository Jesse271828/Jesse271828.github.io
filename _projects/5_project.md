---
layout: page
title: Multi-agent Reinforcement Learning for Trading
description: Sep 2023 - Dec 2023
img: assets/img/cover_image_5.png
importance: 3
category: machine learning
giscus_comments: false
---

<hr style="border: 1px solid black; width: 100%;">

This is a project I did with **Mert Cemri**, who was first year PhD student at BLISS. It's a final project for a class on **deep reinforcement learning**, and we ended up completing a report of **12 pages**, receiving a **96/100** for the project. **We are currently working on comparing the novel methods we developed with baselines in the field of trading with MDPs and possibly submitting to a conference or journal.**

<hr style="border: 1px solid black; width: 100%;">

The basic idea is to treat trading as a game where each player starts with a set amount of wealth. The market consists of two items and the relative price of them changes according to a fixed time series. We used real world data for this time series, which means that we assume its evolution doesn't depend on our agents' actions. Of course, our expectation wasn't that our agent would learn the fundamental structure of this time series, but that our agents would develop strategies against the uncertainty: for instance, they might adjust their frequency of trading. 

After we realized the importance of trading frequency, we wanted to combine this idea with collaborations between agents. We have many agents that specialize at trading on different frequencies (once per day, once per two days, once per four days, etc), but how do we design a system that put all of their specializations to good use? Here, we developed a hierarchical framework for information flow, where high frequency agents can learn from the actions of the lower frequency agents. Moreover, we train a seperate supervising agent that sees the behaviors of all the agents and decide which agent to employ. 

After adding a couple more novel twists to our framework, we compared it with our baseline models: single deep RL agents and confirmed that our framework has promising performance.


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
"https://wjingxing.github.io/assets/pdf/multiagent-trading.pdf"
            width="800" height="500">
        </iframe>
</body>

</html>
