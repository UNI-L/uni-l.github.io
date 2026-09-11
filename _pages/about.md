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

  <div class="research-grid">

    <div class="research-card">
      <div class="research-icon">●</div>
      <h4>Federated AI</h4>
      <p>Collaborative learning across distributed systems.</p>
    </div>

    <div class="research-card">
      <div class="research-icon">✦</div>
      <h4>Agentic AI</h4>
      <p>Autonomous and collaborative AI agents.</p>
    </div>

    <div class="research-card">
      <div class="research-icon">⌁</div>
      <h4>Network Intelligence</h4>
      <p>AI-driven network understanding and control.</p>
    </div>

    <div class="research-card">
      <div class="research-icon">⌁</div>
      <h4>AI-RAN & 6G</h4>
      <p>AI-native intelligence for future networks.</p>
    </div>

    <div class="research-card">
      <div class="research-icon">◈</div>
      <h4>Foundation Models</h4>
      <p>Foundation models for network reasoning.</p>
    </div>

    <div class="research-card">
      <div class="research-icon">✓</div>
      <h4>Anomaly Detection</h4>
      <p>Intelligent detection of abnormal behaviors.</p>
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
  margin-top: 35px;
  margin-bottom: 40px;
}

.research-section h2 {
  margin-bottom: 24px;
}

.research-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

.research-card {
  background: #f7fbff;
  border: 1px solid #dce8f3;
  border-radius: 12px;
  padding: 22px;
  min-height: 150px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.research-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 18px rgba(0, 60, 110, 0.08);
}

.research-icon {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #e8f2fb;
  color: #0a4f87;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.15rem;
  font-weight: 700;
  margin-bottom: 12px;
}

.research-card h4 {
  margin: 0 0 7px 0;
  color: #0a4f87;
  font-size: 1.05rem;
  font-weight: 600;
}

.research-card p {
  margin: 0;
  color: #647587;
  font-size: 0.9rem;
  line-height: 1.45;
}

@media (max-width: 900px) {
  .research-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 650px) {
  .research-grid {
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

@media (max-width: 900px) {
  .research-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 650px) {
  .research-grid {
    grid-template-columns: 1fr;
  }

  .home-footer {
    flex-direction: column;
  }
}

.post-header {
  display: none;
}
</style>
