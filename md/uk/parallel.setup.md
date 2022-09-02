---
navigation:
  - intro.parallel.md: « Введение
  - philosophy.parallel.md: Философия »
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Встановлення
---
# Встановлення

### Вимоги

Для роботи parallel потрібне складання PHP із включеним ZTS (Zend Thread Safety). Зробити це можна, вказавши при компіляції ключ **\-enable-zts** або на системах, відмінних від Windows до PHP 8.0.0, ключ **\-enable-maintainer-zts**

**Застереження**

Zend Thread Safety не можна увімкнути після складання; це варіант конфігурації під час збирання.

parallel слід збирати скрізь, де є робочий заголовок Posix Threads (pthread.h) та ZTS-складання PHP, включаючи Windows (з використанням проекту pthread-w32 від redhat).

### Встановлення

Випуски parallel розміщуються на PECL, а вихідний код - на [» GitHub](https://github.com/krakjoe/parallel), Найпростіший спосіб встановлення - це звичайний маршрут PECL: [» https://pecl.php.net/package/parallel](https://pecl.php.net/package/parallel)

Користувачі Windows можуть завантажити готові двійкові файли випуску із сайту [» PECL](https://windows.php.net/downloads/pecl/releases/parallel)

**Застереження**

Користувачі Windows повинні зробити додатковий крок, додавши pthreadVC2.dll (поширюється разом із випусками Windows) до їх PATH.
