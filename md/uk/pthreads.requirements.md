---
navigation:
  - pthreads.setup.html: « Встановлення та налаштування
  - pthreads.installation.html: Установка »
  - index.html: PHP Manual
  - pthreads.setup.html: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Для pthreads необхідне потокобезпечне складання PHP, тобто. ZTS (Zend Thread Safety). Зробити це можна, вказавши при компіляції ключ **\-enable-zts** або на системах, відмінних від Windows до PHP 8.0.0, ключ **\-enable-maintainer-zts**

**Застереження**

Після компіляції потокобезопасность не можна включити - це лише опція, що встановлюється на етапі компіляції.

pthreads можна зібрати скрізь, де є заголовні файли Posix Threads (pthread.h) і потокобезопасная збірка PHP, включаючи Windows (використовуючи проект pthread-w32 з redhat).
