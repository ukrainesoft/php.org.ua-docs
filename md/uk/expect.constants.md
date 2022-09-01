---
navigation:
  - expect.resources.html: « Типи ресурсів
  - expect.examples.html: Приклади »
  - index.html: PHP Manual
  - book.expect.html: Expect
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`EXP_GLOB`** (int)

Вказує на те, що шаблон є шаблоном пошуку файлу (glob).

**`EXP_EXACT`** (int)

Вказує, що шаблон є точним рядком.

**`EXP_REGEXP`** (int)

Вказує, що шаблон є регулярним виразом.

**`EXP_EOF`** (int)

Значення, що повертається [expectexpectl()](function.expect-expectl.html), коли досягнуто кінець файлу.

**`EXP_TIMEOUT`** (int)

Значення, що повертається [expectexpectl()](function.expect-expectl.html) після вичерпання часу очікування, заданого в [expect.timeout](expect.configuration.html#ini.expect.timeout)

**`EXP_FULLBUFFER`** (int)

Значення, що повертається [expectexpectl()](function.expect-expectl.html), коли збігів із шаблоном не знайдено.
