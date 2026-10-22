
---
layout: page
title: Activities
permalink: /activities/
nav: true
nav_order: 7
---

<style>
.activity-entry {
  display: grid;
  grid-template-columns: 35% minmax(0, 1fr);
  gap: 32px;
  padding: 35px 0;
  border-bottom: 1px solid var(--global-divider-color, #ddd);
  align-items: start;
}

.activity-date {
  font-size: 0.8rem;
  color: var(--global-theme-color);
  font-weight: 600;
  letter-spacing: 1px;
  margin-bottom: 12px;
}

.activity-title {
  font-size: 1.35rem;
  font-weight: 600;
  margin-bottom: 14px;
}

.activity-description {
  font-size: 0.95rem;
  line-height: 1.75;
  opacity: 0.85;
}

.activity-photos {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 8px;
}

.activity-photos a {
  display: block;
  overflow: hidden;
  border-radius: 6px;
}

.activity-photos img {
  display: block;
  width: 100%;
  height: 180px;
  object-fit: cover;
  transition: transform 0.2s ease;
}

.activity-photos a:hover img {
  transform: scale(1.04);
}

.activity-photos a:first-child:nth-last-child(odd) {
  grid-column: 1 / -1;
}

.activity-photos a:first-child:nth-last-child(odd) img {
  height: 260px;
}

@media (max-width: 768px) {
  .activity-entry {
    grid-template-columns: 1fr;
    gap: 18px;
    padding: 25px 0;
  }

  .activity-photos img {
    height: 140px;
  }

  .activity-photos a:first-child:nth-last-child(odd) img {
    height: 200px;
  }
}
</style>

<!-- Activity 1: ICTC 2026 -->
<div class="activity-entry">
  <div class="activity-info">
    <div class="activity-date">OCTOBER 2026</div>
    <h3 class="activity-title">ICTC 2026</h3>
    <p class="activity-description">
      Suhyun Han and Dahae Lee presented their research
      on federated LLM fine-tuning and ROS2 intrusion
      detection at the International Conference on
      ICT Convergence (ICTC 2026) in Jeju, Korea.
    </p>
  </div>

  <div class="activity-photos">
    <a href="{{ '/assets/img/activities/ictc_1.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_1.jpg' | relative_url }}" alt="Dahae Lee at ICTC 2026" loading="lazy">
    </a>
    <a href="{{ '/assets/img/activities/ictc_2.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_2.jpg' | relative_url }}" alt="Poster discussion at ICTC 2026" loading="lazy">
    </a>
    <a href="{{ '/assets/img/activities/ictc_3.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_3.jpg' | relative_url }}" alt="Suhyun Han presenting at ICTC 2026" loading="lazy">
    </a>
    <a href="{{ '/assets/img/activities/ictc_4.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_4.jpg' | relative_url }}" alt="Suhyun Han at ICTC 2026" loading="lazy">
    </a>
  </div>
</div>

<!-- Activity 2: Research Group Gathering -->
<div class="activity-entry">
  <div class="activity-info">
    <div class="activity-date">OCTOBER 2026</div>
    <h3 class="activity-title">Research Group Gathering at ICTC 2026</h3>
    <p class="activity-description">
      A memorable time with members of our
      collaborating research groups during ICTC 2026.
      We enjoyed dinner together and an evening
      of stargazing in Jeju.
    </p>
  </div>

  <div class="activity-photos">
    <a href="{{ '/assets/img/activities/ictc_gathering_1.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_gathering_1.jpg' | relative_url }}" alt="Research group photo at ICTC 2026" loading="lazy">
    </a>
    <a href="{{ '/assets/img/activities/ictc_gathering_2.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_gathering_2.jpg' | relative_url }}" alt="Stargazing in Jeju" loading="lazy">
    </a>
    <a href="{{ '/assets/img/activities/ictc_gathering_3.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ '/assets/img/activities/ictc_gathering_3.jpg' | relative_url }}" alt="Research group dinner" loading="lazy">
    </a>
  </div>
</div>
