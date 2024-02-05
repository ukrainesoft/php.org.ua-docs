---
navigation:
  - ev.feedsignalevent.md: '« Ev::feedSignalEvent'
  - ev.now.md: 'Ev::now »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::iteration'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::iteration

(PECL ev >= 0.2.0)

Ev::iteration — Отримати кількість проведених опитувань циклу за умовчанням щодо нових подій

### Опис

```methodsynopsis
final
   public
   static
   Ev::iteration(): int
```

Повертає кількість опитувань циклу за умовчанням на предмет нових подій. Іноді корисно як лічильник генерацій.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Отримати кількість опитувань циклу за замовчуванням.

### Дивіться також

-   [Ev::depth()](ev.depth.md) \- Здобути глибину рекурсії
