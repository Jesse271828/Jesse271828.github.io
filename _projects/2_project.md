---
layout: page
title: Representation Theory and Random Walks on Groups. 
description: August 2022 - May 2023
img: assets/img/rep.jpg
importance: 2
category: statistics/mathematics
giscus_comments: false
---

This project was completed through a selective program **<a href='https://wp.math.berkeley.edu/drp/program-overview/'> Berkeley Mathematics Directed Reading Program</a>**, where I was paired with **Gabriel Ramirez Raposo**, who was then a PhD student under professor Vadim Gorin. In the end, a writeup was completed, and it includes major results we proved along with, sometimes, the proofs themselves. The writeup is meant to provide an intuitive understanding of the subject. Of course, all the results are in the book, but I try to voice the narration by how I first approached the subject and the order in which I was revealed to the main ideas. Later on, I found connections between the subject and my main research, so I added another brief section discussing that as well. 

Our starting point was the card shuffling question: suppose I give you an ordered deck of cards without the jokers. Now, you must shuffle it until it becomes uniformly random. The question is how many times it takes for that to be accomplished. The answer is 7. And the curve converges very quickly between 6 and 7, which means after I shuffle six times the deck is still very un-uniform, but once I shuffle the seventh time the cards are very uniform. This result comes from the two bounds provided in section 2.4 of the writeup: basically, we treat all possible ways of shuffling as elements of a group. We measure the uniform-ness by looking at the **total variation** between random walks done on this group and the uniform distribution. We then bound them with numerical methods. 

The key is that by introducing **characters**, a key element of representation theory, we're able to overcome the complexity introduced by **convolution**, a necessary step in analyzing any kind of **random walks**. In SP, similarly, we're able to overcome the same difficulty by switching between the frequency domain and the time domain, and thus between convolution and multiplication. I believe these two methodologies are the same in essence, as the content of section 3 implies. 

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
"https://jesse271828.github.io/assets/pdf/rep.pdf"
            width="800" height="500">
        </iframe>
</body>

</html>


