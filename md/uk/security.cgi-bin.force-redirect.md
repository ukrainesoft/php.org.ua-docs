---
navigation:
  - security.cgi-bin.default.md: 'Варіант 1: обслуговуються лише загальнодоступні файли'
  - security.cgi-bin.doc-root.md: 'Варіант 3: використання опцій doc\_root або user\_dir »'
  - index.md: PHP Manual
  - security.cgi-bin.md: Якщо PHP встановлено як CGI
title: 'Вариант 2: использование`cgi.force_redirect`'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вариант 2: использование`cgi.force_redirect`

Конфігураційна директива [cgi.force\_redirect](ini.core.md#ini.cgi.force-redirect) запобігає спробам безпосереднього виклику PHP за адресою виду [http://my.host/cgi-bin/php/secretdir/script.php](http://my.host/cgi-bin/php/secretdir/script.php). Замість цього PHP оброблятиме запит лише в тому випадку, якщо він був перенаправлений веб-сервером.

Зазвичай перенаправлення в конфігурації Apache налаштовується за допомогою таких опцій:

Action php-script /cgi-bin/php AddHandler php-script .php

Ця опція перевірена лише з веб-сервером Apache, її робота ґрунтується на установці у разі перенаправлення нестандартної змінної REDIRECT\_STATUS, що знаходиться в CGI-оточенні. У випадку, якщо ваш веб-сервер не надає можливості однозначно ідентифікувати, чи є цей запит перенаправленим, ви не можете використовувати опцію, що описується в цьому розділі, і повинні скористатися будь-яким іншим методом роботи з CGI-додатками.
