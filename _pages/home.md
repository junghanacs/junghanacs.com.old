---
layout: splash
classes:
  - landing
permalink: /
author_profile: true
---

<br>

<!-- ![image-left](/assets/images/site/headshotsmall.jpg){: .align-left} -->

# 텍스트 마스터

📜 Don't be the best. Be the only. 최고가 되지 말고, 유일한 사람이 되세요. - Kevin Kelly

불사의 검을 만들던 이름 모를 대장장이가 텍스트 장인이 되어 돌아왔다.

[Here](https://notes.junghanacs.com/now) is what I'm up to now.

<a href="/about/" class="btn btn--primary">More about me</a> <a href="mailto:junghanacs@gmail.com" class="btn btn--primary">Contact me</a>
<br>

<!-- {% include feature_row %} -->

<h2>Recent Posts</h2>
{% for post in site.posts limit:5 %}
{% include post-card.html %}
{% endfor %}
