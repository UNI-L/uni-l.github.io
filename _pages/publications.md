
---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---

<style>
.pub-tabs input {
  position: absolute;
  opacity: 0;
}

.pub-tab-labels {
  display: flex;
  gap: 30px;
  border-bottom: 1px solid #ddd;
  margin-bottom: 25px;
}

.pub-tab-labels label {
  cursor: pointer;
  padding: 10px 5px;
  color: var(--global-text-color);
  opacity: 0.6;
  border-bottom: 2px solid transparent;
}

#tab-papers:checked ~ .pub-tab-labels label[for="tab-papers"],
#tab-patents:checked ~ .pub-tab-labels label[for="tab-patents"] {
  opacity: 1;
  font-weight: 600;
  border-bottom-color: var(--global-theme-color);
}

.pub-panel {
  display: none;
}

#tab-papers:checked ~ .pub-panels #papers-panel,
#tab-patents:checked ~ .pub-panels #patents-panel {
  display: block;
}
</style>

<div class="pub-tabs">
  <input type="radio" name="pub-tab" id="tab-papers" checked>
  <input type="radio" name="pub-tab" id="tab-patents">

  <div class="pub-tab-labels">
    <label for="tab-papers">Papers</label>
    <label for="tab-patents">Patents</label>
  </div>

  <div class="pub-panels">
    <div class="pub-panel" id="papers-panel">
      {% include papers_content.html %}
    </div>

    <div class="pub-panel" id="patents-panel">
      {% include patents_content.html %}
    </div>
  </div>
</div>
