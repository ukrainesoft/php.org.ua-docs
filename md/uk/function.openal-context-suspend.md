---
navigation:
  - function.openal-context-process.md: « openal\_context\_process
  - function.openal-device-close.md: openal\_device\_close »
  - index.md: PHP Manual
  - ref.openal.md: Функції OpenAL
title: openal\_context\_suspend
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openal\_context\_suspend

(PECL openal >= 0.1.0)

openal\_context\_suspend — Зупинити вказаний контекст

### Опис

```methodsynopsis
openal_context_suspend(resource $context): bool
```

### Список параметрів

`context`

Ресурс[Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openal\_context\_create()](function.openal-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [openal\_context\_create()](function.openal-context-create.md) \- Створити контекст обробки звуку
-   [openal\_context\_current()](function.openal-context-current.md) \- Зробити вказаний контекст поточним
-   [openal\_context\_process()](function.openal-context-process.md) \- опрацювати зазначений контекст
