---
navigation:
  - functional.parallel.md: « Функціональний API
  - parallel.run.md: parallel\\run »
  - index.md: PHP Manual
  - functional.parallel.md: Функціональний API
title: parallel\\bootstrap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\bootstrap

(1.0.0)

parallel\\bootstrap — Початкове завантаження

### Опис

```methodsynopsis
parallel\bootstrap(string $file): void
```

Повинен використовувати наданий `file` для початкового завантаження всіх середовищ виконання, створених для автоматичного планування за допомогою [parallel\\run()](parallel.run.md)

### Список параметрів

`file`

Шлях до файлу для завантаження всіх середовищ виконання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**Увага**

Викидає parallel\\Runtime\\Error\\Bootstrap, якщо цей процес був раніше викликаний.

**Увага**

Викидає parallel\\Runtime\\Error\\Bootstrap, якщо викликається після [parallel\\run()](parallel.run.md)

### Дивіться також

-   [parallel\\Runtime::run](parallel-runtime.run.md)
