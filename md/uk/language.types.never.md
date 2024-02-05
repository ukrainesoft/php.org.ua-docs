---
navigation:
  - language.types.void.md: « Void
  - language.types.relative-class-types.md: Відносні типи класів »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Never
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Never

never - це тип, який можна вказати тільки для значення, що повертається; він повідомляє, що функція не завершується. Тобто вона або викликає конструкцію мови [exit()](function.exit.md)або викидає виняток, або це нескінченний цикл. Тому його не можна декларувати у [об'єднанні типів](language.types.type-system.md#language.types.type-system.composite.union)Доступно с PHP 8.1.0.

never - це, говорячи мовою теорії типів, нижній тип. Тобто він - підтип будь-якого іншого типу і може замінити будь-який інший тип значення, що повертається при успадкування.
