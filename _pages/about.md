---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

👋 Hi, I'm Liu Gan — I build capable aerial robots that thrive in tough, real-world conditions.

My research focuses on two frontiers: **operational aerial manipulators** and **signal-denied autonomous exploration**. Across 3 National Key R&D Program projects, I own the full pipeline from mechanical prototyping to algorithm deployment and field implementation. I’ve developed drone-mounted robotic arms for dense forest sampling and large facility inspection, and assembled a 3-UAV fleet that navigates and avoids obstacles purely with LiDAR in GNNS denied environment.
I deep-dive into UAV motion planning and control, with 2 first-author EI papers published/accepted and 2 more under external review. Beyond the lab, I’ve earned multiple national competition awards (including 1st and 2nd prizes), top-tier scholarships from UCAS, and honor titles from Wuhan University of Technology. Proficient in C/C++, Python and Linux, I bring end-to-end engineering experience spanning mechanical design, system integration, and algorithm optimization.

# 📖 Educations
- 2024.09 - now, Master's student, Key Laboratory of Robotics and Intelligent Systems, Shenyang Institute of Automation, Chinese Academy of Sciences. 
- 2020.09 - 2024.06, Bachelor Degree, Transportation and Logistics Engineering, Wuhan University of Technology. 

<span class='anchor' id='projects'></span>

# 📌 Projects
I have extensive experience in developing ground robots, underwater robots, and aerial robots, and I've participated in several key R&D projects and research competitions.

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Aerial Robot</div><img src='images/uav.gif' alt="UAV Obstacle Avoidance Demo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**UAV Obstacle Avoidance Trajectory Planning in Signal-Denied Environments**

Designed and implemented a LiDAR-based trajectory planning and real-time obstacle avoidance system for multi-UAV fleets in GPS-denied and signal-interference environments. Realized stable autonomous navigation without external positioning signals, completed field deployment and verification in complex scenarios.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Ground Robot</div><img src='images/qzj.gif' alt="Autonomous Handling Crane Demo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Autonomous Handling Crane**

Developed an autonomous intelligent crane system with high-precision positioning, visual cargo identification and stable transfer capabilities. This work won the National First Prize in the China College Students Mechanical Engineering Innovation and Creativity Competition.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">AUV</div><img src='images/auv.gif' alt="Drowning Rescue Robot Demo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Autonomous High-Speed Anti-Current Drowning Rescue Robot**

Built a water rescue robot platform with strong current resistance, integrating autonomous drowning person detection, high-speed approach and safe rescue functions. This work won the National Second Prize in the 12th National Ocean Vehicle Design and Production Competition.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Ship</div><img src='images/ship.gif' alt="Ship Navigation Decision Support System Demo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Ship Navigation Decision Support System Based on Dynamic Navigation Space**

Realized multi-ship collision avoidance trajectory planning in complex inland waterways based on the Velocity Obstacle method and Dynamic Window Approach, providing real-time decision support for safe and efficient ship navigation in restricted channel environments.

</div>
</div>

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ICUS 2025</div><img src='images/icus2025.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[PF-BiRRT: Potential Field Guided Bidirectional Locally Constrained RRT-Connect Path Planning Algorithm](https://ieeexplore.ieee.org/document/11295573)

**G. Liu**, L. Yang, X. Yin, S. Li and Z. Huang

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Journal of System Simulation 2026</div><img src='images/JSS2026.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[ Obstacle Avoidance Trajectory Planning for Flying Mechanical Arms Based on Bezier Curve](https://kns.cnki.net/kcms2/article/abstract?v=wTY03cmeYFolyIuN5i3Aw8OIafEhwgzvVFoPy7GaHBzFJLKSBVVtA7Zhjqm6cR4fslb9h6tPgxHwlbrb-JespuaPode1hdfKB71usG2Nd6kuB15GJ8LRruCDxiJdAGDpoBA3MjsHd3PlHh3vl3Z6diajnyx8v0AtLtKLSqeMqHpSmzi5Cbg96w==&uniplatform=NZKPT&language=CHS)

**G. Liu**, L. Yang, S. Li, et al

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">SIVP</div><img src='images/SIVP.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[ VA-RRT: A Neural Adaptive RRT-Connect Path Planning Algorithm Guided by Visual Attention Mechanisms(Under Review)](https://ucas-lg.github.io/)

**G. Liu**, L. Yang, Z. Huang, et al

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">icus2026</div><img src='images/icus2026.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[MPC-Based Motion Planning for Aerial Grasping of Vegetation Canopy Samples(Under Review)](https://ucas-lg.github.io/)

**G. Liu**, L. Yang, S. Li, et al

</div>
</div>

- [Coupled-Layer Diffusion for Kinodynamic Trajectory Generation](https://ieeexplore.ieee.org/document/11478300), Pinhui Zhao, Decai Li, Minjiang Wu, **et al**, **IEEE Robotics and Automation Letters**
- [Path Planning for Ferry Crossing Inland Waterways Based on Deep Reinforcement Learning](https://www.mdpi.com/2077-1312/11/2/337), Xiaoli Yuan, Chengji Yuan, Wuliu Tian, **Gan Liu**, **Journal of Marine Science and Engineering**
- [A* Pre-Guided Ant Colony Path Planning Algorithm Integrated with Q-learning ](https://kns.cnki.net/kcms2/article/abstract?v=wTY03cmeYFpeQqJlZqFtGPv4dQNbCGWncxG9kpL0HKJCI9aIwJ45quPR9wwSVnTK7Qa2PLMvxLZlDoasn7uJWXqn2PGQeyXplJTVOC5pp3LXcNFB5nMhEbFA1N_KjYBYFI4l9oZt4qAoUGagfOjWK5sxGhnu2wAz96_Qqc7GUvTS2bsNzaLlVA==&uniplatform=NZKPT&language=CHS), Yin Xiaotian, Yang Liying, **Liu Gan**, et al., **Sensors and Microsystems**

<span class='anchor' id='competition-awards'></span>

# 🏅 Competition Awards
- **National First Prize** · Crane Innovation Competition, China College Students Mechanical Engineering Innovation and Creativity Competition · 2023
- **National Second Prize** · The 12th National Ocean Vehicle Design and Production Competition · 2023
- **National Third Prize** · "Huawei Cup" China Postgraduate Mathematical Contest in Modeling · 2024
- **National Third Prize** · The 5th National College Students Smart Supply Chain Innovation and Entrepreneurship Challenge · 2022

<span class='anchor' id='honors-and-awards'></span>

# 🎓 Honors and Awards
- National Encouragement Scholarship · 2021 & 2022
- First-Class Academic Scholarship, University of Chinese Academy of Sciences · 2025
- Merit Student, Wuhan University of Technology · 2021, 2022 & 2023
- Excellent Communist Youth League Member, Wuhan University of Technology · 2023
- Outstanding Graduate, Wuhan University of Technology · 2024

<span class='anchor' id='love'></span>

# 🔥 Love
- 🏸 &nbsp; **Badminton**: Regular weekly play, enjoy competitive doubles matches and racket sport training.
- 🚴 &nbsp; **Cycling**: Passionate about long-distance outdoor cycling and recreational city rides.
- 🏊 &nbsp; **Swimming**: Casual enthusiast, focus on endurance building and full-body fitness through regular swimming sessions.

<div style="display:flex; gap:12px; flex-wrap:wrap; margin-top:8px;">
  <img src="images/badminton.png" alt="Badminton" style="width:32%; min-width:180px; border-radius:8px;">
  <img src="images/cycling1.png" alt="Cycling 1" style="width:32%; min-width:180px; border-radius:8px;">
  <img src="images/cycling2.png" alt="Cycling 2" style="width:32%; min-width:180px; border-radius:8px;">
</div>
