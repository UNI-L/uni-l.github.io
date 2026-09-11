---
layout: page
title: Home
permalink: /
nav: true
nav_order: 1
---

<div class="unil-banner">
  <img src="/assets/img/banner_image.jpg" alt="UNI.L">
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


<section>
  <h2>Research Areas</h2>

  <div class="research-grid">

    <div class="research-card">
      <h4>Federated & Collaborative AI</h4>
      <p>
        Distributed and collaborative learning across heterogeneous networked systems.
      </p>
    </div>

    <div class="research-card">
      <h4>Agentic AI</h4>
      <p>
        Autonomous and collaborative AI agents for intelligent decision-making.
      </p>
    </div>

    <div class="research-card">
      <h4>AI-Native Network Intelligence</h4>
      <p>
        Data-driven learning and intelligence for network understanding and control.
      </p>
    </div>

    <div class="research-card">
      <h4>AI-RAN & 6G Networks</h4>
      <p>
        AI-native architectures and intelligent control for next-generation networks.
      </p>
    </div>

    <div class="research-card">
      <h4>Network Foundation Models</h4>
      <p>
        Foundation models for network understanding, reasoning, and optimization.
      </p>
    </div>

    <div class="research-card">
      <h4>AI-based Anomaly Detection</h4>
      <p>
        Intelligent detection and analysis of anomalous behaviors in networked systems.
      </p>
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
        {% for item in news limit:5 %}
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
  <div>
    <strong>UNI.L — Ultimate Network Intelligence Lab.</strong>
  </div>

  <div>
    Department of Electrical and Electronic Engineering<br>
    Kangwon National University<br>
    Engineering Building 5, Room 514-2<br>
    Chuncheon, Republic of Korea
  </div>
</footer>


<style>
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

.research-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
  margin-top: 25px;
  margin-bottom: 35px;
}

.research-card {
  border: 1px solid #e2e8f0;
  border-radius: 10px;
  padding: 20px;
  min-height: 145px;
}

.research-card h4 {
  margin-top: 0;
  margin-bottom: 12px;
  font-weight: 600;
}

.research-card p {
  margin-bottom: 0;
  font-size: 0.95rem;
  line-height: 1.55;
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
</style>
