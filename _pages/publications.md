
---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 3
---

<h2>TEST - Publications Tab</h2>

<style>
.publication-tabs {
  display: flex;
  gap: 30px;
  border-bottom: 1px solid var(--global-divider-color);
  margin-bottom: 25px;
}

.publication-tab {
  background: none;
  border: none;
  border-bottom: 2px solid transparent;
  padding: 10px 5px;
  cursor: pointer;
  color: var(--global-text-color);
  opacity: 0.6;
}

.publication-tab.active {
  opacity: 1;
  font-weight: 600;
  border-bottom-color: var(--global-theme-color);
}
</style>

<div class="publication-tabs">
  <button class="publication-tab active" type="button"
          onclick="showPublicationTab('papers', this)">
    Papers
  </button>

  <button class="publication-tab" type="button"
          onclick="showPublicationTab('patents', this)">
    Patents
  </button>
</div>

<div id="papers-content">
  {% include papers_content.html %}
</div>

<div id="patents-content" style="display: none;">
  {% include patents_content.html %}
</div>

<script>
function showPublicationTab(tab, button) {
  document.getElementById('papers-content').style.display =
    tab === 'papers' ? 'block' : 'none';

  document.getElementById('patents-content').style.display =
    tab === 'patents' ? 'block' : 'none';

  document.querySelectorAll('.publication-tab')
    .forEach(el => el.classList.remove('active'));

  button.classList.add('active');
}
</script>
