
---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---

<style>
.pub-tabs {
  display: flex;
  gap: 30px;
  border-bottom: 1px solid #ddd;
  margin-bottom: 25px;
}

.pub-tab {
  background: transparent;
  border: none;
  border-bottom: 2px solid transparent;
  padding: 10px 5px;
  cursor: pointer;
  color: var(--global-text-color);
  opacity: 0.6;
}

.pub-tab.active {
  opacity: 1;
  font-weight: 600;
  color: var(--global-theme-color);
  border-bottom-color: var(--global-theme-color);
}

.pub-content {
  display: none;
}

.pub-content.active {
  display: block;
}
</style>

<div class="pub-tabs">
  <button type="button" class="pub-tab active"
    onclick="switchPubTab('papers', this)">
    Papers
  </button>

  <button type="button" class="pub-tab"
    onclick="switchPubTab('patents', this)">
    Patents
  </button>
</div>

<div id="papers" class="pub-content active">
  <h3>International Journals</h3>
  <p>Paper list test.</p>
</div>

<div id="patents" class="pub-content">
  <h3>Patents</h3>
  <p>Patent list test.</p>
</div>

<script>
function switchPubTab(tab, button) {
  document.querySelectorAll('.pub-content')
    .forEach(el => el.classList.remove('active'));

  document.querySelectorAll('.pub-tab')
    .forEach(el => el.classList.remove('active'));

  document.getElementById(tab).classList.add('active');
  button.classList.add('active');
}
</script>
