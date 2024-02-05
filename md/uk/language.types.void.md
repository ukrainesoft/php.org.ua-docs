---
navigation:
  - language.types.mixed.md: « Mixed
  - language.types.never.md: Never »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Void
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Void

void - це тип, який можна вказати тільки для значення, що повертається; він повідомляє, що функція не повертає значення, але функція все одно може завершитися. Тому його не можна використовувати в [об'єднанні типів](language.types.type-system.md#language.types.type-system.composite.union)Доступно с PHP 7.1.0.

> **Зауваження**: Навіть якщо тип значення функції void, що повертається, вона все одно поверне значення і цим значенням буде **`null`**
