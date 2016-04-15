---
title: Student Listing
layout: page
---

[Add yourself!](https://github.com/remi-daigle/2016-04-15-UCSB/tree/gh-pages/_data#introduce-yourself)

<!-- based on http://git.io/vvroy -->
<ul>
  {% assign students = site.data | sort %}
  {% for user_hash in students %}
    {% assign username = user_hash[0] %}
    {% assign user = user_hash[1] %}

    <li class="js-student" data-username="{{username}}">
      <div class="info">
        <a href="https://github.com/{{ username }}">
        <img class="js-avatar" src=""/>
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
