---
title: Student Listing
layout: page
---

[Add yourself!](https://github.com/ucsb-bren/env-info#readme)

<!-- based on http://git.io/vvroy -->
<ul>
  {% assign students = site.data | sort %}
  {% for user_hash in students %}
    {% assign username = user_hash[0] %}
    {% assign user = user_hash[1] %}

    <li class="js-student" data-username="{{username}}">
      <a href="https://github.com/{{ username }}">
        <!-- TODO add loading image -->
        <img class="js-avatar" src=""/>
      </a>
      <div class="info">
        <a href="https://github.com/{{ username }}">
          <div>
            <span class="github-username">@{{ username }}</span>
          </div>
          <div>
            <span class="js-name"></span>
          </div>
          <div>
            <p><span class="octicon octicon-info"></span> {{ user.info }}</p>
          </div>
        </a>
      </div>
    </li>
  {% endfor %}
</ul>
