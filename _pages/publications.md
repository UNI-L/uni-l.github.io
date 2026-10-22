
---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---

<style>
.pub-tabs > input[type="radio"] {
  position: absolute;
  opacity: 0;
  width: 1px;
  height: 1px;
}

.pub-tab-labels {
  display: flex;
  gap: 30px;
  border-bottom: 1px solid var(--global-divider-color, #ddd);
  margin-bottom: 25px;
}

.pub-tab-labels label {
  cursor: pointer;
  padding: 10px 5px;
  margin-bottom: -1px;
  color: var(--global-text-color);
  opacity: 0.6;
  border-bottom: 2px solid transparent;
  transition: all 0.2s ease;
}

.pub-tab-labels label:hover {
  opacity: 1;
  color: var(--global-theme-color);
}

#tab-papers:checked ~ .pub-tab-labels label[for="tab-papers"],
#tab-patents:checked ~ .pub-tab-labels label[for="tab-patents"] {
  opacity: 1;
  font-weight: 600;
  color: var(--global-theme-color);
  border-bottom-color: var(--global-theme-color);
}

.pub-panel {
  display: none;
}

#tab-papers:checked ~ .pub-panels #papers-panel,
#tab-patents:checked ~ .pub-panels #patents-panel {
  display: block;
}

.pub-panel h2 {
  margin-top: 30px;
  margin-bottom: 15px;
}

.pub-panel ol {
  padding-left: 25px;
}

.pub-panel li {
  margin-bottom: 12px;
  line-height: 1.7;
}

.pub-panel .award {
  color: #e63946;
  font-weight: 700;
}
</style>

<div class="pub-tabs">

  <input
    type="radio"
    name="pub-tab"
    id="tab-papers"
    checked
  >

  <input
    type="radio"
    name="pub-tab"
    id="tab-patents"
  >

  <div class="pub-tab-labels">
    <label for="tab-papers">Papers</label>
    <label for="tab-patents">Patents</label>
  </div>

  <div class="pub-panels">

    <div class="pub-panel" id="papers-panel">
      {% capture papers_content %}{% include papers_content.html %}{% endcapture %}
      {{ papers_content | markdownify }}
    </div>

    <div class="pub-panel" id="patents-panel">
      {% capture patents_content %}{% include patents_content.html %}{% endcapture %}
      {{ patents_content | markdownify }}
    </div>

  </div>

</div>
