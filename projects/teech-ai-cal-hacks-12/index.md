---
title: teech.ai
layout: project
---

<iframe width="100%" height="480" src="https://www.youtube-nocookie.com/embed/luVIdLB9id0?si=1sTE9Z3MeyWntRmd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**A proof-of-concept tutoring app for students learning math.** Using the phone camera, the app sees and understands math problems, guiding students through problems with hints and step-by-step questions. We added text-to-speech (TTS) to give our app a voice, further engaging students and making it feel like a more personal experience.

[Tri Vu](https://www.linkedin.com/in/tri-q-vu/) built a web interface prototype and Python-based backend utilizing the Gemini Vision API and Fish Audio for TTS.

I built a native proof-of-concept using SwiftUI, AVFoundation, and other native frameworks. In the app, I built a chat and camera interface, integrating with Tri's backend by sending image and prompt data. Swiping to the right reveals the user's chat history, which is also continuously synced with the backend. Design-wise, I decided to use this gesture-based approach in order to bring the camera interface front and center.

The app was built in 48 hours for **Cal Hacks 12.0**, the world's largest collegiate hackathon.

[GitHub](https://github.com/brendan-ch/teecher-ios){: .primary-action }
[Devpost](https://devpost.com/software/teech-ai){: .secondary-action }
[Cal Hacks](https://www.calhacks.io){: .secondary-action }
{: .horizontal-wrapper }
