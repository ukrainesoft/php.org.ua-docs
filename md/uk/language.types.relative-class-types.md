---
navigation:
  - language.types.never.md: « Never
  - language.types.value.md: Типи значень »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Відносні типи класів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Відносні типи класів

Ці оголошення типів можна використовувати лише усередині класів.

### self

Значення має бути [`instanceof`](language.operators.type.md) того ж класу, що і клас, у якому використовується оголошення типу.

### parent

Значення має бути [`instanceof`](language.operators.type.md) батьківського класу, успадкованого класом, у якому оголошується тип.

### static

static - це тип тільки для значення, що повертається, який вимагає, щоб повертане значення було [`instanceof`](language.operators.type.md) того ж класу, як і клас, в якому викликається метод. Наявна наукова з PHP 8.0.0.
