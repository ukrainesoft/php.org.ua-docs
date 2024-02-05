---
navigation:
  - ev.sleep.md: '« Ev::sleep'
  - ev.supportedbackends.md: 'Ev::supportedBackends »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::stop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Зупинити цикл за замовчуванням.

### Список параметрів

`how`

Одна из*Ev::BREAK\_\** [констант](class.ev.md#ev.constants.break-flags)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::run()](ev.run.md) \- Почати перевірку наявності подій та виклик callback-функцій циклу за умовчанням
