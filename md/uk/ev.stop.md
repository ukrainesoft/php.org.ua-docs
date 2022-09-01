---
navigation:
  - ev.sleep.html: '« Ev::sleep'
  - ev.supportedbackends.html: 'Ev::supportedBackends »'
  - index.html: PHP Manual
  - class.ev.html: Єв
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

Одна з *Ev::BREAK* [констант](class.ev.html#ev.constants.break-flags)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::run()](ev.run.html) - Почати перевірку наявності подій та виклик callback-функцій циклу за умовчанням
