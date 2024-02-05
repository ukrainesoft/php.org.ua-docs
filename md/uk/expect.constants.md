---
navigation:
  - expect.resources.md: « Типи ресурсів
  - expect.examples.md: Приклади »
  - index.md: PHP Manual
  - book.expect.md: Expect
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`EXP_GLOB`**(int)

Вказує на те, що шаблон є шаблоном пошуку файлу (glob).

**`EXP_EXACT`**(int)

Вказує, що шаблон є точним рядком.

**`EXP_REGEXP`**(int)

Вказує, що шаблон є регулярним виразом.

**`EXP_EOF`**(int)

Значение, возвращаемое[expect\_expectl()](function.expect-expectl.md), коли досягнуто кінець файлу.

**`EXP_TIMEOUT`**(int)

Значение, возвращаемое[expect\_expectl()](function.expect-expectl.md)после исчерпания времени ожидания, заданного в[expect.timeout](expect.configuration.md#ini.expect.timeout)

**`EXP_FULLBUFFER`**(int)

Значение, возвращаемое[expect\_expectl()](function.expect-expectl.md)коли збігів з шаблоном не знайдено.
