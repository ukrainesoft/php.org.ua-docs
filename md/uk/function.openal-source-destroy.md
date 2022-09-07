---
navigation:
  - function.openal-source-create.md: « openalsourcecreate
  - function.openal-source-get.md: openalsourceget »
  - index.md: PHP Manual
  - ref.openal.md: Функции OpenAL
title: openalsourcedestroy
---
# openalsourcedestroy

(PECL openal >= 0.1.0)

openalsourcedestroy - Знищення ресурсу джерела

### Опис

```methodsynopsis
openal_source_destroy(resource $source): bool
```

### Список параметрів

`source`

Ресурс [Open AL(Source)](openal.resources.md) (Створений раніше за допомогою [openalsourcecreate()](function.openal-source-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalsourcecreate()](function.openal-source-create.md) - Згенерувати джерело ресурсу
