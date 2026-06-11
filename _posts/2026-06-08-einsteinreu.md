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

<p> I suppose now that I have been here for a few more days, I should talk a bit more about the project. I mentioned before that the aim of the REU was to generalize the Solovay-Kitaev theorem to more general groups. The SK Theorem was particularly revolutionary for quantum computing as it established a method for approximating <i> any </i> quantum gate to a very high accuracy and in polylogarithmic time and length. </p>

<p> A paper from Dawson and Nielsen established the main results and provided an algorithmic proof, introducing, loosely, the concept of a <i> balanced group commutator </i> for \(\textrm{SU}(2)\) and \(\textrm{SU}(d)\). It turns out that the existence of the balanced group commutator is a useful tool that comes from compact Lie groups, notably in the inverse mapping from the Lie group to the Lie algebra of \(\textrm{SU}(d)\). Dawson and Nielsen mention an error that is exactly the balanced group commutator, and I learned that it is possible to derive from the <a href="https://en.wikipedia.org/wiki/Baker%E2%80%93Campbell%E2%80%93Hausdorff_formula">BCH formula</a>.  </p>

<p> To think in the minds of people attempting to expand the field of quantum computation, it would seem reasonable to attempt to extend the SK Theorem beyond just compact Lie groups, or perhaps to theoretically suggest an algorithm with a shorter quantum gate sequence and shorter computational time. My mentor suggested a 2002 paper that covered this, and the SK Theorem was improved slightly for specific non-general groups.  </p>

<p> I am still in the early stages of learning the tools, but it turns out that a conceptual approach to generalizing the SK Theorem (but first and foremost, something more theoretical at the intersection of representation theory, Lie theory, and analysis that I cannot grasp quite yet) involves something known as an <a href="https://en.wikipedia.org/wiki/Expander_graphs">expander graph</a>, particularly a <a href="https://en.wikipedia.org/wiki/Cayley_graph">Cayley graph</a>. While I am still sorting out the details of expander graphs, I understand them currently as a graph that has nice connectivity properties–this means that the <a href="https://en.wikipedia.org/wiki/Diameter_(graph_theory)">diameter</a> of the graph is bounded favorably and possesses a value known as the <a href="https://en.wikipedia.org/wiki/Spectral_gap">spectral gap</a>, which measures connectivity–the larger the spectral gap, the more connected a graph is. I've seen \(k\)-regular graphs used largely in this context. Cayley graphs, on the other hand, coming from Cayley's Theorem in group theory, represent group structure in a graph nicely, generating an entire finite group from a generating set; we can denote such graphs as \(\textrm{Cay}(G,S)\) for some group \(G\) and a generating set \(S\). The idea is that the vertices in a Cayley graph represent elements of a quantum gate set, and the edges represent a finite generating set–the choice of this generating set is important, and there are many collections. One that I have seen notably is the Clifford\(+T\) set, containing the \(H\) and \(T\) gates, or the Hadamard and \(\pi/8\) gates respectively. Since Cayley graphs are well connected (this is a non-rigorous way to say it), we might ask how we can formulate a short <a href="https://en.wikipedia.org/wiki/Word_(group_theory)">word</a> from the generating set so as to approximate an arbitrary quantum gate. </p>

<p> Groups in general are discrete objects. This means that there is going to be a feasible word that can be applied to a given quantum gate to reach a target quantum gate. However, in the case of \(\textrm{SU}(2)\), which is a smooth manifold, such a generating set can be difficult and intensive to obtain.  A 2018 survey paper from Lubotzky and Breuillard that I was instructed to read (and still need to read more of) mentions a new operator, known as a <a href="https://en.wikipedia.org/wiki/Hecke_operator">Hecke operator</a> or "averaging operator" that is needed for a curved space such as \(\textrm{SU}(2)\). I still have to figure out what exactly this operator is in the context of expander graphs, but I'll treat it (and about 80% of the rest of the paper) as a black box for now. One tool, mentioned also in Lubotzky and Breuillard's survey paper, is the idea of golden gates. Golden gates were introduced by Ross and Selinger in a 2014 paper, and, as the name suggests, they are the "golden" approach for generating a group like \(\textrm{SU}(2)\). I still need to read the paper, but surprisingly, there is a decent amount of algebraic number theory at play and I'm excited to see where that goes. I think my mentor has worked closely with golden gates in his recent research. Lots more to read. </p>

<p> Before anything, I think I should mention that I've never read a math research paper at the frontier of math before. Even these papers are a few years old (though constantly re-referenced and cited), but they contain so many ideas that I could not possibly fit into 2 years of undergraduate study, much less 2 months of an REU. I guess I had an idea that math research should be cumulative, as in I should understand all of the vast literature before and have learned every single idea and term mentioned. I think reading through some of these papers, I've learned that I do not understand a million things. And I felt uncomfortable. So many rabbit holes to go down on Wikipedia... and then I see another textbook that I should download. I think ultimately, the main takeaway that I should apply to my work in this REU and future research is the importance of the black box: it shouldn't be used for everything, but "<a href="https://math.stackexchange.com/questions/2016185/is-it-normal-to-treat-math-theorems-as-black-boxes">[n]o new research would ever get done if the researcher tried to intimately understand the entire path from Pythagoras to the state of the art.</a>" I'm an undergraduate, after all. </p>

<div class="standalone-image-container">
  <figure class="grid-card landscape-img">
    <img src="/quadcryo/assets/img/einsteinlibrary.jpg" alt="Mathematics library at the Manchester Building">
    <figcaption>Mathematics library at the Manchester Building</figcaption>
  </figure>
</div>

<p> In these few days, I've returned to campus one more time. The REU acquired a computer lab room for work in the future, though it does not have a chalkboard/whiteboard (the temperature may also be controlled and set to frighteningly low temperatures, much to one person's dismay). Above is a picture of the mathematics library–lots and lots of textbooks. If this collection were aggregated and sold online, I can only imagine how valuable it would be–potentially millions, considering 90% of the books appeared to be Springer. </p>

<p> As part of REUs, I think there is a tradition of bringing students to conferences taking place locally. My mentor suggested we attend the <a href="https://iias.huji.ac.il/event/25th-midrasha-mathematicae-groups-expanders-and-codes">Midrasha Mathematicae on Groups, Expanders, and Codes</a> next week, a conference at the Einstein Institute for researchers in the field of quantum computation and the exact area that my REU project is on (without surprise, my mentor is one of the organizers). I expect to understand 1% of the material from the talks, but I hope to be able to appreciate the atmosphere and get a taste of what a conference should feel like. Maybe I can ask some good questions if I read more diligently this week!</p>

<p> (11 June, 2026) </p>