---
layout: post
title: Robots.txt for WordPress
description: Ideal file robots.txt for CMS WordPress
---

# Robots.txt for CMS WordPress

```
User Agent: * # оголошуємо назву пошукового робота (юзер-агента), наприклад Googlebot або Yandexbot. Це може також бути будь-який інший краулер, навіть приватний. Зірочка позначає усіх пошукових ботів відразу. Disallow: /cgi-bin # системна папка сервера, яка відповідає за виконання скриптів, обов’язково закриваємо від пошуковиків
Disallow: /wp-admin/ # системна папка WordPress, закриваємо від пошуку в обов’язковому порядку
Disallow: /wp-cron.php # системний файл, планувальник завдань WordPress, закриваємо
Disallow: /xmlrpc.php # системний файл, відповідає за віддалене RPC-підключення до WordPress, вразливий до хакерських атак, закриваємо від пошуку і бажано обмежити права доступу
Disallow: */trackback # функція сповіщення про згадування вашого домену на інших сайтах, є часто зайвою, закриваємо її від пошуку, а в налаштуваннях WordPress бажано відключити
Disallow: */feed # RSS посилання, дублюють сторінки сайту, тому бажано закривати від пошуку
Disallow: */rss # аналогічно попередньому
Disallow: */embed # посилання вбудованого коду чи компонентів на сайті, бажано закривати, щоби не індексувалися
Disallow: /author/* # закриваємо від пошуку публікації автора, що дублюють сторінки сайту
Disallow: /tag/ # закриваємо від пошуку теги, які також дублюють інші сторінки сайту
Disallow: /? # закриваємо від пошуку технічні або динамічні URL-адреси
Disallow: *?s # аналогічно
Disallow: *&amp;s # аналогічно
Disallow: *utm*= # закриваємо від пошуку посилання з utm-мітками
Disallow: *openstat= # блокуємо посилання з мітками openstat
Disallow: ?*replytocom # закриваємо від пошуку посилання відповідей на коментарі, є зайвими і не потрібними для пошуку
Allow: */uploads # відкриваємо для пошуку папку із завантаженнями, зображеннями
Allow: /*/*.js # відкриваємо доступ до скриптів. Якщо ж закрити, можуть бути проблеми з обробкою та відображенням сайту пошуковиками. Як наслідок — виникатимуть помилки неоптимізованого контенту і таке інше
Allow: /*/*.css # аналогічно відкриваємо доступ до стилів, щоби пошуковики могли коректно зрендерити верстку сторінки і коректно перевірити оптимізацію
Allow: /wp-*.png # далі відкриваємо для пошуковиків зображення в різних форматах
Allow: /wp-*.jpg
Allow: /wp-*.jpeg
Allow: /wp-*.gif
Allow: /wp-*.svg
Allow: /wp-*.pdf # відкриваємо pdf-файли для індексації
Allow: /wp-admin/admin-ajax.php # аналогічно, може використовуватися пошуковими системами для рендерінгу, чимало фахівців рекомендують відкрити
Sitemap: https://example.com/sitemap.xml # вказуємо повний шлях до XML мапи сайту, покращує індексацію сайту
```
[back]({{ site.url }})