---
title: CTF Writeups
---

# rshi07 CTF Writeups

am noob ctf player. good at osint/misc/forensics, ok at web, terrible at pwn/rev/crypto although trying to improve. playing with yorkCTF (dead), UofTCTF, THEM?!, or solo

{% assign writeups = site.writeups | sort: "date" | reverse %}
{% if writeups.size > 0 %}
## Latest

<div class="writeup-list">
{% for writeup in writeups %}
  <a href="{{ writeup.url | relative_url }}">
    <strong>{{ writeup.title }}</strong>
    <span>{{ writeup.year }}{% if writeup.ctf %} / {{ writeup.ctf }}{% endif %}{% if writeup.date %} / {{ writeup.date | date: "%b %-d, %Y" }}{% endif %}</span>
  </a>
{% endfor %}
</div>
{% else %}
No writeups yet.
{% endif %}
