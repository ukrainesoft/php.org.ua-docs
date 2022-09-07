---
navigation:
  - expect.resources.md: « Типи ресурсів
  - expect.examples.md: Приклади »
  - index.md: PHP Manual
  - book.expect.md: Expect
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

Значення, що повертається [expectexpectl()](function.expect-expectl.md), коли досягнуто кінець файлу.

**`EXP_TIMEOUT`** (int)

Значення, що повертається [expectexpectl()](function.expect-expectl.md) після вичерпання часу очікування, заданого в [expect.timeout](expect.configuration.md#ini.expect.timeout)

**`EXP_FULLBUFFER`** (int)

Значення, що повертається [expectexpectl()](function.expect-expectl.md), коли збігів із шаблоном не знайдено.
