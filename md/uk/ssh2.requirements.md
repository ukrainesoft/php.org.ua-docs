---
navigation:
  - ssh2.setup.md: '" Встановлення та налаштування'
  - ssh2.installation.md: Встановлення »
  - index.md: PHP Manual
  - ssh2.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Для встановлення SSH2 потрібна наявність встановлених бібліотек [» OpenSSL](http://www.openssl.org/) і [» libssh2](http://libssh2.org/). Переконайтеся, що вказані бібліотеки є в системі. Типовою назвою пакета може бути `openssl-dev`

Необхідна версія libssh2 1.2 або новіша. Однак можливо, що нові релізи pecl/ssh2 вимагатимуть нові версії (дивіться примітки до релізу).

Функция[ssh2\_auth\_agent()](function.ssh2-auth-agent.md) доступна лише з версією libssh >= 1.2.3.

Підтримка канальних потоків у [stream\_set\_timeout()](function.stream-set-timeout.md) доступна лише з версією libssh >= 1.2.9.

Libssh2 поставляється у двох варіантах: gcrypt або openssl. Деякі Linux-дистрибутиви збирають libssh2 з бібліотекою gcrypt, деякі з openssl. Libssh2 має деякі проблеми при компіляції з gcrypt, тому використовуйте версію openssl.
