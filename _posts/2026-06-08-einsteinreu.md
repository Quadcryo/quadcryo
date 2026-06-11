---
layout: post
title:  Einstein Institute of Mathematics REU
date:   2026-06-11 00:00-00
description: happenings this summer
tags: research
---

<style>
  /* ====== SHARED BASE IMAGE STYLES ====== */
  .grid-card {
    margin: 0;
    position: relative;
    overflow: hidden;
    border-radius: 8px;
    background-color: #f7f7f7;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    width: 100%;
  }

  .grid-card img {
    width: 100%;
    display: block;
    object-fit: cover;
  }

  .grid-card figcaption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 35px 15px 12px 15px;
    color: #ffffff;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    font-size: 14px;
    font-weight: 500;
    background: linear-gradient(transparent, rgba(0, 0, 0, 0.85));
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.6);
    pointer-events: auto; 
    z-index: 2;
  }

  .grid-card figcaption a {
    pointer-events: auto;
  }

  /* ====== CONTAINER 1: THE 2x2 GRID LAYER ====== */
  .mobile-friendly-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
    gap: 12px;
    max-width: 1000px;
    margin: 20px auto;
    padding: 10px;
    box-sizing: border-box;
  }

  /* ====== CONTAINER 2: STANDALONE IMAGE LAYER ====== */
  .standalone-image-container {
    max-width: 1000px;
    margin: 25px auto;
    padding: 0 10px;
    box-sizing: border-box;
  }

  /* ====== RESPONSIVE HEIGHT CONTROLS ====== */
  @media (min-width: 769px) {
    /* Grid-specific row balances */
    .mobile-friendly-grid {
      grid-template-columns: repeat(2, 1fr);
    }
    .mobile-friendly-grid .landscape-img img { height: 380px; }
    .mobile-friendly-grid .portrait-img img { height: 550px; }
    
    /* Standalone-specific sizing */
    .standalone-image-container .landscape-img img { height: 480px; } 
  }

  @media (max-width: 768px) {
    .mobile-friendly-grid {
      grid-template-columns: 1fr;
      gap: 16px;
    }
    .landscape-img img { height: 240px; }
    .portrait-img img { height: 420px; }
    .grid-card figcaption { font-size: 13px; }
  }
</style>

<p> This summer I am attending the Einstein Institute of Mathematics REU in Jerusalem, Israel. The program just began as of 8 June, so I will add many experiences and some pictures to this post as more things happen, but I'd like to start here by sort of describing the beginning of the program and some things I've experienced so far. </p>

<p> The elephant in the room at this current moment is the reality of long-standing geopolitical conflict in the region. I won't talk about details or politics as my goal here is to document my experiences, but the program began rather explosively with sirens, missile alerts, and a video of a missile being intercepted. More details <a href="https://www.aljazeera.com/video/newsfeed/2026/6/8/missiles-intercepted-over-occupied-east-jerusalem-and-west-bank-2">here</a>. This didn't really hinder much. </p>

<p> I was able to meet with my advisor, Dr. Shai Evra, and the project was broadly introduced to us. From what I currently understand, a large fragment of the REU is dedicated to understanding the <a href = "https://en.wikipedia.org/wiki/Solovay%E2%80%93Kitaev_theorem">Solovay-Kitaev theorem</a> for compact Lie groups, and potentially attempting to extend the algorithm to general groups. Depending on the direction, we might also attempt to work on an open problem in group theory, or possibly go in some other directions relating to quantum algorithms and algebraic number theory. I imagine objectives and interests will shift, but this is the basic skeleton of the program. </p>

<p> I've also had a lot of fun meeting the other people in the program, and it's nice to see how international our group is! We have people from China, South Korea, Greece, and the United States. </p>

<p> Anyway, some of us visited the campus today, and I have to say: the Hebrew University has a rather nice campus, and I really appreciate the combination of traditional and brutalist architecture. Here are some random pictures. </p>

<div class="mobile-friendly-grid">
  <figure class="grid-card landscape-img">
    <img src="/quadcryo/assets/img/solovaykitaev.jpg" alt="Flash presentation about the project">
    <figcaption>Flash presentation about the project</figcaption>
  </figure>
  
  <figure class="grid-card landscape-img">
    <img src="/quadcryo/assets/img/sabiche.jpg" alt="Sabich">
    <figcaption><a href="https://en.wikipedia.org/wiki/Sabich" target="_blank">Sabich</a>!</figcaption>
  </figure>

  <figure class="grid-card portrait-img">
    <img src="/quadcryo/assets/img/einsteinstatue.jpg" alt="Albert Einstein statue in front of the Ross Building">
    <figcaption>Albert Einstein statue in front of the Ross Building</figcaption>
  </figure>
  
  <figure class="grid-card portrait-img">
    <img src="/quadcryo/assets/img/einsteinpic.jpg" alt="The Einstein Institute of Mathematics at the Hebrew University of Jerusalem (HUJI)">
    <figcaption>The Einstein Institute of Mathematics at the Hebrew University of Jerusalem (HUJI)</figcaption>
  </figure>
</div>

<p> (8 June, 2026) </p>

<p> I suppose now that I have been here for a few more days, I should talk a bit more about the project and some of our goals. </p>

<p> Another few days later, and I've returned to campus one more time. The REU acquired a computer lab room for work in the future, though it does not have a chalkboard/whiteboard (the temperature may also be controlled and set to frighteningly low temperatures, much to one person's dismay). At the bottom is a picture of the mathematics library–lots and lots of textbooks. If this collection were aggregated and sold online, I can only imagine how valuable it would be–potentially millions, considering 90% of the books appeared to be Springer. </p>

<div class="standalone-image-container">
  <figure class="grid-card landscape-img">
    <img src="/quadcryo/assets/img/einsteinlibrary.jpg" alt="Mathematics library at the Institute">
    <figcaption>Mathematics library at the Institute</figcaption>
  </figure>
</div>

<p> (11 June, 2026) </p>