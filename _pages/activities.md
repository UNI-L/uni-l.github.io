

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
  gap: 30px;
  padding: 35px 0;
  border-bottom: 1px solid var(--global-divider-color, #ddd);
  align-items: start;
}

.activity-entry:first-of-type {
  padding-top: 15px;
}

.activity-info {
  padding-right: 10px;
}

.activity-date {
  font-size: 0.8rem;
  color: var(--global-theme-color);
  font-weight: 600;
  letter-spacing: 1px;
  margin-bottom: 12px;
}

.activity-title {
  font-size: 1.4rem;
  font-weight: 600;
  margin-bottom: 14px;
  color: var(--global-text-color);
}

.activity-description {
  font-size: 0.95rem;
  line-height: 1.75;
  color: var(--global-text-color);
  opacity: 0.85;
}

.activity-photos {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 8px;
}

.activity-photos img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 6px;
  display: block;
  transition: transform 0.2s ease;
}

.activity-photos img:hover {
  transform: scale(1.02);
}

.activity-photos img:first-child:nth-last-child(odd) {
  grid-column: 1 / -1;
  height: 220px;
}

@media (max-width: 768px) {
  .activity-entry {
    grid-template-columns: 1fr;
    gap: 16px;
    padding: 25px 0;
  }

  .activity-photos img {
    height: 120px;
  }

  .activity-photos img:first-child:nth-last-child(odd) {
    height: 180px;
  }
}
</style>

<!-- Activity 1: ICTC 2026 -->
<div class="activity-entry">

  <div class="activity-info">
    <div class="activity-date">OCTOBER 2026</div>
    <h3 class="activity-title">ICTC 2026</h3>
    <p class="activity-description">
      Our lab members presented two research papers
      at the International Conference on ICT
      Convergence (ICTC 2026).
    </p>
  </div>

  <div class="activity-photos">
    <img src="{{ '/assets/img/activities/ictc1.jpg' | relative_url }}" alt="ICTC 2026 group photo">
    <img src="{{ '/assets/img/activities/ictc2.jpg' | relative_url }}" alt="ICTC 2026 presentation">
    <img src="{{ '/assets/img/activities/ictc3.jpg' | relative_url }}" alt="ICTC 2026 conference">
  </div>

</div>

<!-- Activity 2: Lab Gathering -->
<div class="activity-entry">

  <div class="activity-info">
    <div class="activity-date">SEPTEMBER 2026</div>
    <h3 class="activity-title">Lab Gathering</h3>
    <p class="activity-description">
      A wonderful time together with our
      research group members.
    </p>
  </div>

  <div class="activity-photos">
    <img src="{{ '/assets/img/activities/gathering1.jpg' | relative_url }}" alt="Lab gathering 1">
    <img src="{{ '/assets/img/activities/gathering2.jpg' | relative_url }}" alt="Lab gathering 2">
  </div>

</div>
