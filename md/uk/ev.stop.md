---
navigation:
  - ev.sleep.md: '« Ev::sleep'
  - ev.supportedbackends.md: 'Ev::supportedBackends »'
  - index.md: PHP Manual
  - class.ev.md: Єв
title: 'Ev::stop'
---
# Ev::stop

(PECL ev >= 0.2.0)

Ev::stop — Зупинити цикл за замовчуванням

### Опис

```methodsynopsis
final
   public
   static
   Ev::stop(
    int
     $how
    = ?): void
```

Зупинити цикл подій за замовчуванням.

### Список параметрів

`how`

Одна з *Ev::BREAK* [констант](class.ev.md#ev.constants.break-flags)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::run()](ev.run.md) - Почати перевірку наявності подій та виклик callback-функцій циклу за умовчанням
