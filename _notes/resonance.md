---
categories: "- '[[Projects]]'"
related: ""
title: Resonance
---

Resonance is a cyberpunk-themed game show shooter. Enter the arena, blast your opponents, and become the star of the show. I worked with a student team of 12 to create this game over multiple months. The game was selected as an **IEEE GameSig finalist**.

![](/assets/img/resonance.png)

The project was also part of the [[Chapman University]] game development capstone. No, I was not a part of the game development program. I just helped out because I had free time.

My core role was to implement the game’s networking logic using [[PurrNet]], an open-source library for Unity.

My first project was to implement networking for **Arena**, a free-for-all PVP game mode, where the player with the most eliminations wins. I learned how to isolate game logic on the server and synchronize state on each client.

Another project was the **build system**. Having a server dependency and Steam integration meant that the environment differed from development to production. We found it painful to prepare a build for each class-mandated playtest. I used Claude to create a two-step system including an editor script and a GitHub Actions pipeline.

I’m currently working on a client-side prediction model to match other FPS games on the market.

Even with our team size, the most important thing I learned was how to manage scope and scale. Each one of us pushed ourselves to the limits of our knowledge, going from bare theoretical understanding to practical working implementations. The goal was never to get things right on the first try; it was to learn and realize new ideas in multiple passes.
