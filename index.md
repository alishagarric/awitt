---
title: Curriculum Vitae 2018
layout: landing-page
---
{% include head.html %}
<div class="resume">
  <div class="flex-row">
    <div class="name">
      {{ site.data.information.full_name }}
    </div>
    <div class="contact">
      <p>{{ site.data.information.address_1 }}</p>
      <p>{{ site.data.information.city }}, {{ site.data.information.state }} {{ site.data.information.postal_code }}</p>
      <p>{{ site.data.information.phone }}</p>
      <p>{{ site.data.information..email }}</p>
    </div>
  </div>
  {% for item in site.people %}
    <div class="section">
      <div class="section-title">
        <span>{{ item.title }}</span>
      </div>
      {% for sub-item in item.section_items_full %}
        <div class="flex-row full-list">
          <div class="main">
            <div class="title">
              {{ sub-item.title }}
            </div>
            <div class="descriptor">
              {{ sub-item.descriptor }}
            </div>
            <div class="description">
              {{ sub-item.description }}
            </div>
          </div>
          <div class="date">
            {{ sub-item.date }}
          </div>
        </div>
      {% endfor %}
      {% for sub-item in item.sections_items_basic %}
        <div class="flex-row basic-list">
          <div class="main">
            <div class="title">
              {{ sub-item.title }},
            </div>
            <div class="description">
              {{ sub-item.description }}
            </div>
          </div>
          <div class="date">
            {{ sub-item.date }}
          </div>
        </div>
      {% endfor %}
      {% for sub-item in item.sections_items_list %}
        <div class="flex-row list">
          <div class="main">
            <div class="title">
              {{ sub-item.title }}
            </div>
            <div class="descriptor">
              {{ sub-item.descriptor }}
            </div>
            <div class="description">
              {{ sub-item.description }}
            </div>
          </div>
          <div class="date">
            {{ sub-item.date }}
          </div>
        </div>
      {% endfor %}
    </div>
  {% endfor %}
</div>
