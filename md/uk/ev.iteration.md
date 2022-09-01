---
navigation:
  - ev.feedsignalevent.html: '« Ev::feedSignalEvent'
  - ev.now.html: 'Ev::now »'
  - index.html: PHP Manual
  - class.ev.html: Єв
title: 'Ev::iteration'
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

-   [Ev::depth()](ev.depth.md) - Здобути глибину рекурсії
