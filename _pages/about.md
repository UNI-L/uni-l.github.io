---
layout: page
title: Home
permalink: /
nav: false
---

<div class="unil-banner">
  <img src="/assets/img/banner_image.png" alt="UNI.L">
</div>

<section class="home-intro">
  <h1>Welcome to UNI.L</h1>
  <h3>Ultimate Network Intelligence Lab.</h3>

  <p>
    The Ultimate Network Intelligence Lab. (UNI.L), led by Prof. Jungmin Kwon,
    conducts research at the intersection of artificial intelligence,
    distributed learning, and next-generation communication networks.
  </p>

  <p>
    Our research focuses on developing intelligent and collaborative AI systems
    that can learn, adapt, and make decisions across distributed network
    environments. We are particularly interested in federated and decentralized
    learning, agentic AI, and AI-native network intelligence, with applications
    to next-generation networks such as AI-RAN and 6G systems.
  </p>
</section>


<hr>
<section class="research-section">
  <h2>Research Areas</h2>

  <h3 class="research-group-title">AI for Networked Systems</h3>

  <div class="research-grid network-grid">

    <div class="research-card">
      <h4>Network Intelligence</h4>
      <p>AI-driven network modeling, optimization, and control.</p>
    </div>

    <div class="research-card">
      <h4>AI-RAN & 6G</h4>
      <p>AI-native intelligence for next-generation networks.</p>
    </div>

  </div>


  <h3 class="research-group-title">Learning & Data Intelligence</h3>

  <div class="research-grid learning-grid">

    <div class="research-card">
      <h4>Federated AI</h4>
      <p>Distributed learning across heterogeneous systems.</p>
    </div>

    <div class="research-card">
      <h4>Agentic AI</h4>
      <p>Autonomous reasoning and multi-agent collaboration.</p>
    </div>

    <div class="research-card">
      <h4>Time-Series Analysis</h4>
      <p>Learning and analysis of temporal and sequential data.</p>
    </div>

    <div class="research-card">
      <h4>Anomaly Detection</h4>
      <p>Data-driven detection and analysis of abnormal behaviors.</p>
    </div>

  </div>
</section>
<hr>


<section>
  <h2>Latest News</h2>

  <div class="news">
    {% assign news = site.news | sort: "date" | reverse %}

    <div class="table-responsive">
      <table class="table table-sm table-borderless">
        {% for item in news limit:3 %}
          <tr>
            <th scope="row" style="width: 130px;">
              {{ item.date | date: "%b %d, %Y" }}
            </th>
            <td>
              {% if item.inline %}
                {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
              {% else %}
                <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table>
    </div>
  </div>

  <p class="view-all">
    <a href="/news/">View all news →</a>
  </p>
</section>


<hr>

<footer class="home-footer">

  <div class="footer-logo">
    <img src="/assets/img/unil_image.png" alt="UNI.L">
  </div>

  <div class="footer-info">
    Department of Electrical and Electronic Engineering<br>
    Kangwon National University<br>
    Engineering Building 5, Room 514-2<br>
    Chuncheon, Republic of Korea
  </div>

</footer>


<style>
.home-intro h1 {
  color: #0a4f87;
  font-weight: 700;
}
  
.home-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;
  margin-top: 35px;
  margin-bottom: 20px;
  padding-top: 20px;
  font-size: 0.95rem;
  line-height: 1.6;
}

.footer-logo img {
  width: 180px;
  height: auto;
  display: block;
}

.footer-info {
  text-align: left;
}

@media (max-width: 650px) {
  .home-footer {
    flex-direction: column;
    align-items: flex-start;
  }

  .footer-logo img {
    width: 160px;
  }
}


  
.unil-banner {
  width: 100%;
  margin: 10px 0 45px 0;
}

.unil-banner img {
  width: 100%;
  height: auto;
  display: block;
}

.home-intro {
  max-width: 760px;
  margin-bottom: 40px;
}

.home-intro h1 {
  margin-bottom: 5px;
}

.home-intro h3 {
  margin-top: 0;
  margin-bottom: 25px;
  font-weight: 400;
  color: #5f6f85;
}


  .research-section {
  margin-top: 40px;
  margin-bottom: 45px;
}

.research-section h2 {
  margin-bottom: 28px;
}

.research-group-title {
  color: #003b70;
  font-size: 1.05rem;
  font-weight: 600;
  margin-top: 28px;
  margin-bottom: 14px;
  padding-bottom: 7px;
  border-bottom: 2px solid #dce8f3;
}

.research-grid {
  display: grid;
  gap: 16px;
  margin-bottom: 32px;
}

.network-grid {
  grid-template-columns: repeat(2, 1fr);
}

.learning-grid {
  grid-template-columns: repeat(2, 1fr);
}

.research-card {
  background: #f7fbff;
  border: 1px solid #dce8f3;
  border-radius: 10px;
  padding: 18px 20px;
}

.research-card h4 {
  color: #0a4f87;
  font-size: 1rem;
  font-weight: 600;
  margin: 0 0 7px 0;
}

.research-card p {
  color: #647587;
  font-size: 0.9rem;
  line-height: 1.45;
  margin: 0;
}

.research-card:hover {
  border-color: #9fc3df;
  box-shadow: 0 4px 14px rgba(0, 59, 112, 0.07);
}

@media (max-width: 650px) {
  .network-grid,
  .learning-grid {
    grid-template-columns: 1fr;
  }
}

.view-all {
  text-align: right;
  margin-top: 10px;
}

.home-footer {
  display: flex;
  justify-content: space-between;
  gap: 40px;
  margin-top: 35px;
  margin-bottom: 20px;
  padding-top: 10px;
  font-size: 0.95rem;
  line-height: 1.6;
}

.post-header {
  display: none;
}
</style>
