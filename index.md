---
layout: default
---

# KR. Laboratories GitHub

Вітаємо на офіційній GitHub-сторінці IT-студії **KR. Laboratories**!

Тут плануємо публікувати короткі технічні дописи, замітки, витяги з коду. Зокрема вихідний код деяких _Open Source_ додатків та програм.

Підписуйтесь на нас у <a href="https://facebook.com/kr.laboratories">Facebook</a> та додавайтесь у друзі на <a href="https://linkedin.com/in/kr-laboratories">LinkedIn</a>!

Наша електронна адреса для зв'язку: <a href="mailto:info@kr-labs.com.ua">info@kr-labs.com.ua</a>

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

# Останні дописи

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
