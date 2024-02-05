---
navigation:
  - ssh2.resources.md: « Типи ресурсів
  - ref.ssh2.md: Функції SSH2 »
  - index.md: PHP Manual
  - book.ssh2.md: SSH2
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SSH2_FINGERPRINT_MD5`**(int)

Прапор для отримання ідентифікатора сервера у вигляді хеш-суми MD5 функцією [ssh2\_fingerprint()](function.ssh2-fingerprint.md)

**`SSH2_FINGERPRINT_SHA1`**(int)

Прапор для отримання ідентифікатора сервера у вигляді хеш-суми SHA1 функцією [ssh2\_fingerprint()](function.ssh2-fingerprint.md)

**`SSH2_FINGERPRINT_HEX`**(int)

Флаг для получения идентификатора сервера функцией[ssh2\_fingerprint()](function.ssh2-fingerprint.md) у вигляді рядка шістнадцяткових символів.

**`SSH2_FINGERPRINT_RAW`**(int)

Флаг для получения идентификатора сервера функцией[ssh2\_fingerprint()](function.ssh2-fingerprint.md) у вигляді невідформатованого рядка восьмибітних символів.

**`SSH2_TERM_UNIT_CHARS`**(int)

Флаг для функции[ssh2\_shell()](function.ssh2-shell.md), Що визначає, що параметри `width`и`height` задаються як кількість символів.

**`SSH2_TERM_UNIT_PIXELS`**(int)

Флаг для функции[ssh2\_shell()](function.ssh2-shell.md), Що визначає, що параметри `width`и`height` задаються у пікселях.

**`SSH2_DEFAULT_TERM_WIDTH`**(int)

Значення ширини вікна терміналу, прийняте функцією, прийняте за умовчанням. [ssh2\_shell()](function.ssh2-shell.md)

**`SSH2_DEFAULT_TERM_HEIGHT`**(int)

Прийняте за умовчанням значення висоти вікна терміналу, яке приймає функція [ssh2\_shell()](function.ssh2-shell.md)

**`SSH2_DEFAULT_TERM_UNIT`**(int)

Прийнята за замовчуванням одиниця виміру значень ширини та висоти вікна терміналу, що приймаються функцією [ssh2\_shell()](function.ssh2-shell.md)

**`SSH2_STREAM_STDIO`**(int)

Флаг функции[ssh2\_fetch\_stream()](function.ssh2-fetch-stream.md), що запитує субканал STDIO

**`SSH2_STREAM_STDERR`**(int)

Флаг функции[ssh2\_fetch\_stream()](function.ssh2-fetch-stream.md), що запитує субканал STDERR.

**`SSH2_DEFAULT_TERMINAL`**(string)

Прийнятий за умовчанням тип терміналу (наприклад, vt102, ansi, xterm, vanilla), що запитується функцією [ssh2\_shell()](function.ssh2-shell.md)

**`SSH2_POLLIN`**(int)

**`SSH2_POLLEXT`**(int)

**`SSH2_POLLOUT`**(int)

**`SSH2_POLLERR`**(int)

**`SSH2_POLLHUP`**(int)

**`SSH2_POLLNVAL`**(int)

**`SSH2_POLL_SESSION_CLOSED`**(int)

**`SSH2_POLL_CHANNEL_CLOSED`**(int)

**`SSH2_POLL_LISTENER_CLOSED`**(int)
