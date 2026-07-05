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

<!-- 自定义增强样式 -->
<style>
  /* 全局平滑过渡 */
  * {
    scroll-behavior: smooth;
  }

  /* 项目/论文卡片悬浮效果 */
  .paper-box {
    transition: all 0.3s ease;
    border-radius: 12px;
    overflow: hidden;
    margin-bottom: 24px;
    border: 1px solid #eaecef;
    background: #fff;
  }
  .paper-box:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 24px rgba(0,0,0,0.08);
    border-color: #d0d7de;
  }
  .paper-box-image .badge {
    border-radius: 0 0 0 8px;
    font-size: 0.75rem;
    font-weight: 600;
    padding: 4px 10px;
  }

  /* 核心数据统计卡片 */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
    margin: 24px 0;
  }
  .stat-card {
    text-align: center;
    padding: 18px 12px;
    background: #f6f8fa;
    border-radius: 10px;
    border: 1px solid #eaecef;
    transition: all 0.3s ease;
  }
  .stat-card:hover {
    background: #ffffff;
    box-shadow: 0 6px 16px rgba(0,0,0,0.06);
  }
  .stat-number {
    font-size: 1.8rem;
    font-weight: 700;
    color: #0969da;
    line-height: 1.2;
  }
  .stat-label {
    font-size: 0.85rem;
    color: #57606a;
    margin-top: 4px;
  }
  @media (max-width: 640px) {
    .stats-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  /* 教育经历时间线 */
  .timeline {
    position: relative;
    padding-left: 28px;
    margin: 16px 0;
  }
  .timeline::before {
    content: '';
    position: absolute;
    left: 8px;
    top: 6px;
    bottom: 6px;
    width: 2px;
    background: #d0d7de;
  }
  .timeline-item {
    position: relative;
    margin-bottom: 22px;
  }
  .timeline-item::before {
    content: '';
    position: absolute;
    left: -24px;
    top: 6px;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: #0969da;
    border: 2px solid #ffffff;
    box-shadow: 0 0 0 2px #0969da;
  }
  .timeline-time {
    font-weight: 600;
    color: #0969da;
    font-size: 0.95rem;
    margin-bottom: 4px;
  }
  .timeline-title {
    font-weight: 600;
    font-size: 1rem;
    margin-bottom: 2px;
  }
  .timeline-sub {
    color: #57606a;
    font-size: 0.9rem;
  }

  /* 奖项卡片网格 */
  .awards-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 14px;
    margin: 16px 0;
  }
  .award-card {
    padding: 14px 16px;
    background: #f6f8fa;
    border-radius: 10px;
    border-left: 4px solid #0969da;
    transition: all 0.3s ease;
  }
  .award-card:hover {
    background: #ffffff;
    box-shadow: 0 6px 16px rgba(0,0,0,0.06);
  }
  .award-level {
    font-weight: 700;
    color: #cf222e;
    font-size: 0.9rem;
    margin-bottom: 4px;
  }
  .award-name {
    font-size: 0.95rem;
    line-height: 1.4;
  }
  .award-year {
    font-size: 0.85rem;
    color: #57606a;
    margin-top: 4px;
  }
  @media (max-width: 640px) {
    .awards-grid {
      grid-template-columns: 1fr;
    }
  }

  /* 技能标签 */
  .skills-section {
    margin: 16px 0;
  }
  .skill-category {
    margin-bottom: 14px;
  }
  .skill-category h4 {
    font-size: 0.95rem;
    color: #24292f;
    margin-bottom: 8px;
    font-weight: 600;
  }
  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .skill-tag {
    padding: 4px 12px;
    background: #ddf4ff;
    color: #0969da;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
    transition: all 0.2s ease;
  }
  .skill-tag:hover {
    background: #0969da;
    color: #ffffff;
  }

  /* 兴趣画廊优化 */
  .hobby-gallery {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-top: 12px;
  }
  .hobby-gallery img {
    width: calc(33.33% - 8px);
    min-width: 180px;
    border-radius: 10px;
    transition: all 0.3s ease;
    object-fit: cover;
    aspect-ratio: 4/3;
  }
  .hobby-gallery img:hover {
    transform: scale(1.03);
    box-shadow: 0 8px 20px rgba(0,0,0,0.1);
  }

  /* 分区标题统一风格 */
  h2 {
    border-bottom: 2px solid #eaecef;
    padding-bottom: 8px;
    margin-top: 40px;
    margin-bottom: 20px;
    font-size: 1.4rem;
  }

  /* 论文分区小标题 */
  .pub-subtitle {
    font-size: 1.05rem;
    font-weight: 600;
    margin: 20px 0 12px 0;
    color: #24292f;
    padding-left: 10px;
    border-left: 3px solid #0969da;
  }

  /* 合作论文列表 */
  .pub-list-item {
    padding: 10px 12px;
    margin-bottom: 8px;
    border-radius: 8px;
    transition: background 0.2s ease;
  }
  .pub-list-item:hover {
    background: #f6f8fa;
  }
</style>

<span class='anchor' id='about-me'></span>

👋 Hi, I'm Liu Gan — I build capable aerial robots that thrive in tough, real-world conditions.

My research focuses on two frontiers: **operational aerial manipulators** and **signal-denied autonomous exploration**. Across 3 National Key R&D Program projects, I own the full pipeline from mechanical prototyping to algorithm deployment and field implementation. I’ve developed drone-mounted robotic arms for dense forest sampling and large facility inspection, and assembled a 3-UAV fleet that navigates and avoids obstacles purely with LiDAR in GNSS-denied environments.

I deep-dive into UAV motion planning and control, with 2 first-author EI papers published/accepted and 2 more under external review. Beyond the lab, I’ve earned multiple national competition awards (including 1st and 2nd prizes), top-tier scholarships from UCAS, and honor titles from Wuhan University of Technology. Proficient in C/C++, Python and Linux, I bring end-to-end engineering experience spanning mechanical design, system integration, and algorithm optimization.

<!-- 核心成果数据看板 -->
<div class="stats-grid">
  <div class="stat-card">
    <div class="stat-number">4+</div>
    <div class="stat-label">First-author Papers</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">3</div>
    <div class="stat-label">National R&D Projects</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">5+</div>
    <div class="stat-label">National Awards</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">Full</div>
    <div class="stat-label">End-to-End Engineering</div>
  </div>
</div>

# 📖 Educations
<div class="timeline">
  <div class="timeline-item">
    <div class="timeline-time">2024.09 - Present</div>
    <div class="timeline-title">Master's Student</div>
    <div class="timeline-sub">Key Laboratory of Robotics and Intelligent Systems, Shenyang Institute of Automation, Chinese Academy of Sciences</div>
  </div>
  <div class="timeline-item">
    <div class="timeline-time">2020.09 - 2024.06</div>
    <div class="timeline-title">Bachelor of Engineering</div>
    <div class="timeline-sub">Transportation and Logistics Engineering, Wuhan University of Technology</div>
  </div>
</div>

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

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Marine Robot</div><img src='images/auv.gif' alt="Drowning Rescue Robot Demo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Autonomous High-Speed Anti-Current Drowning Rescue Robot**

Built a water rescue robot platform with strong current resistance, integrating autonomous drowning person detection, high-speed approach and safe rescue functions. This work won the National Second Prize in the 12th National Ocean Vehicle Design and Production Competition.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Maritime Intelligence</div><img src='images/ship.gif' alt="Ship Navigation Decision Support System Demo" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Ship Navigation Decision Support System Based on Dynamic Navigation Space**

Realized multi-ship collision avoidance trajectory planning in complex inland waterways based on the Velocity Obstacle method and Dynamic Window Approach, providing real-time decision support for safe and efficient ship navigation in restricted channel environments.

</div>
</div>

# 📝 Publications 

<div class="pub-subtitle">First-author Papers</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ICUS 2025 · EI Conference</div><img src='images/icus2025.png' alt="PF-BiRRT paper preview" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[PF-BiRRT: Potential Field Guided Bidirectional Locally Constrained RRT-Connect Path Planning Algorithm](https://ieeexplore.ieee.org/document/11295573)

**G. Liu**, L. Yang, X. Yin, S. Li and Z. Huang

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Journal of System Simulation 2026 · EI Journal</div><img src='images/JSS2026.png' alt="Bezier trajectory planning paper preview" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Obstacle Avoidance Trajectory Planning for Flying Mechanical Arms Based on Bezier Curve](https://kns.cnki.net/kcms2/article/abstract?v=wTY03cmeYFolyIuN5i3Aw8OIafEhwgzvVFoPy7GaHBzFJLKSBVVtA7Zhjqm6cR4fslb9h6tPgxHwlbrb-JespuaPode1hdfKB71usG2Nd6kuB15GJ8LRruCDxiJdAGDpoBA3MjsHd3PlHh3vl3Z6diajnyx8v0AtLtKLSqeMqHpSmzi5Cbg96w==&uniplatform=NZKPT&language=CHS)

**G. Liu**, L. Yang, S. Li, et al.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">SIVP · SCI · Under Review</div><img src='images/SIVP.png' alt="VA-RRT paper preview" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

VA-RRT: A Neural Adaptive RRT-Connect Path Planning Algorithm Guided by Visual Attention Mechanisms

**G. Liu**, L. Yang, Z. Huang, et al.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ICUS 2026 · EI · Under Review</div><img src='images/icus2026.png' alt="MPC aerial grasping paper preview" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

MPC-Based Motion Planning for Aerial Grasping of Vegetation Canopy Samples

**G. Liu**, L. Yang, S. Li, et al.

</div>
</div>

<div class="pub-subtitle">Co-authored Publications</div>

<div class="pub-list-item">
  <a href="https://ieeexplore.ieee.org/document/11478300">Coupled-Layer Diffusion for Kinodynamic Trajectory Generation</a><br>
  Pinhui Zhao, Decai Li, Minjiang Wu, et al. · <em>IEEE Robotics and Automation Letters (SCI, JCR Q1)</em>
</div>

<div class="pub-list-item">
  <a href="https://www.mdpi.com/2077-1312/11/2/337">Path Planning for Ferry Crossing Inland Waterways Based on Deep Reinforcement Learning</a><br>
  Xiaoli Yuan, Chengji Yuan, Wuliu Tian, <strong>Gan Liu</strong> · <em>Journal of Marine Science and Engineering (SCI)</em>
</div>

<div class="pub-list-item">
  A* Pre-Guided Ant Colony Path Planning Algorithm Integrated with Q-learning<br>
  Yin Xiaotian, Yang Liying, <strong>Liu Gan</strong>, et al. · <em>Sensors and Microsystems</em>
</div>

<span class='anchor' id='competition-awards'></span>

# 🏅 Competition Awards
<div class="awards-grid">
  <div class="award-card">
    <div class="award-level">National First Prize</div>
    <div class="award-name">Crane Innovation Competition, China College Students Mechanical Engineering Innovation and Creativity Competition</div>
    <div class="award-year">2023</div>
  </div>
  <div class="award-card">
    <div class="award-level">National Second Prize</div>
    <div class="award-name">The 12th National Ocean Vehicle Design and Production Competition</div>
    <div class="award-year">2023</div>
  </div>
  <div class="award-card">
    <div class="award-level">National Third Prize</div>
    <div class="award-name">"Huawei Cup" China Postgraduate Mathematical Contest in Modeling</div>
    <div class="award-year">2024</div>
  </div>
  <div class="award-card">
    <div class="award-level">National Third Prize</div>
    <div class="award-name">The 5th National College Students Smart Supply Chain Innovation and Entrepreneurship Challenge</div>
    <div class="award-year">2022</div>
  </div>
</div>

<span class='anchor' id='honors-and-awards'></span>

# 🎓 Honors & Scholarships
<div class="awards-grid">
  <div class="award-card">
    <div class="award-level">First-Class Academic Scholarship</div>
    <div class="award-name">University of Chinese Academy of Sciences</div>
    <div class="award-year">2025</div>
  </div>
  <div class="award-card">
    <div class="award-level">National Encouragement Scholarship</div>
    <div class="award-name">Ministry of Education of China</div>
    <div class="award-year">2021 & 2022</div>
  </div>
  <div class="award-card">
    <div class="award-level">Outstanding Graduate</div>
    <div class="award-name">Wuhan University of Technology</div>
    <div class="award-year">2024</div>
  </div>
  <div class="award-card">
    <div class="award-level">Merit Student</div>
    <div class="award-name">Wuhan University of Technology</div>
    <div class="award-year">2021, 2022 & 2023</div>
  </div>
</div>


<span class='anchor' id='skills'></span>

# 💻 Skills
<div class="skills-section">
  <div class="skill-category">
    <h4>Programming & Languages</h4>
    <div class="skill-tags">
      <span class="skill-tag">C/C++</span>
      <span class="skill-tag">Python</span>
      <span class="skill-tag">MATLAB</span>
      <span class="skill-tag">CMake</span>
      <span class="skill-tag">Shell</span>
    </div>
  </div>
  <div class="skill-category">
    <h4>Robotics & Algorithms</h4>
    <div class="skill-tags">
      <span class="skill-tag">UAV</span>
      <span class="skill-tag">AUV</span>
      <span class="skill-tag">SHIP</span>
      <span class="skill-tag">CRANE</span>
      <span class="skill-tag">Motion Planning</span>
      <span class="skill-tag">MPC</span>
      <span class="skill-tag">RRT Series</span>
      <span class="skill-tag">Reinforcement Learning</span>
      <span class="skill-tag">Trajectory Optimization</span>
      <span class="skill-tag">LiDAR Perception</span>
    </div>
  </div>
  <div class="skill-category">
    <h4>Platforms & Tools</h4>
    <div class="skill-tags">
      <span class="skill-tag">ROS</span>
      <span class="skill-tag">Linux</span>
      <span class="skill-tag">Gazebo</span>
      <span class="skill-tag">PX4</span>
      <span class="skill-tag">SolidWorks</span>
      <span class="skill-tag">Ardunio</span>
      <span class="skill-tag">Git</span>
    </div>
  </div>
</div>

<span class='anchor' id='interests'></span>

# 🔥 Interests
- 🏸 &nbsp; **Badminton**: Regular weekly play, enjoy competitive doubles matches and racket sport training.
- 🚴 &nbsp; **Cycling**: Passionate about long-distance outdoor cycling and recreational city rides.
- 🏊 &nbsp; **Swimming**: Casual enthusiast, focus on endurance building and full-body fitness through regular swimming sessions.

<div class="hobby-gallery">
  <img src="images/badminton.png" alt="Badminton">
  <img src="images/cycling1.png" alt="Cycling">
  <img src="images/cycling2.png" alt="Cycling">
</div>