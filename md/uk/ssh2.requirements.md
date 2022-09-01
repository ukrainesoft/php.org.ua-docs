---
navigation:
  - ssh2.setup.html: « Встановлення та налаштування
  - ssh2.installation.html: Установка »
  - index.html: PHP Manual
  - ssh2.setup.html: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Для встановлення SSH2 потрібна наявність встановлених бібліотек [» OpenSSL](http://www.openssl.org/) і [» libssh2](http://libssh2.org/). Переконайтеся, що вказані бібліотеки є в системі. Типовою назвою пакета може бути `openssl-dev`

Необхідна версія libssh2 1.2 або новіша. Однак можливо, що нові релізи pecl/ssh2 вимагатимуть нові версії (дивіться примітки до релізу).

Функція [ssh2authagent()](function.ssh2-auth-agent.html) доступна лише з версією libssh >= 1.2.3.

Підтримка канальних потоків у [streamsettimeout()](function.stream-set-timeout.html) доступна лише з версією libssh >= 1.2.9.

Libssh2 поставляється у двох варіантах: gcrypt або openssl. Деякі Linux-дистрибутиви збирають libssh2 з бібліотекою gcrypt, деякі з openssl. Libssh2 має деякі проблеми при компіляції з gcrypt, тому використовуйте версію з openssl.
