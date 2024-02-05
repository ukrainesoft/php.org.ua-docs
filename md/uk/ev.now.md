---
navigation:
  - ev.iteration.md: '« Ev::iteration'
  - ev.nowupdate.md: 'Ev::nowUpdate »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::now'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::now

(PECL ev >= 0.2.0)

Ev::now — Отримати час запуску останньої ітерації циклу за замовчуванням

### Опис

```methodsynopsis
final
   public
   static
   Ev::now(): float
```

Повертає час запуску останньої ітерації циклу за замовчуванням. Це час, на якому базуються таймери ( [EvTimer](class.evtimer.md) і [EvPeriodic](class.evperiodic.md)) і, зазвичай, звернення до цієї функції відбувається швидше, ніж виклик [Ev::time()](ev.time.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість секунд (фракцій), що становить час, коли була запущена остання ітерація циклу за замовчуванням.

### Дивіться також

-   [Ev::nowUpdate()](ev.nowupdate.md) \- Встановлює поточний час шляхом запиту до ядра в процесі оновлюючи час, який повертається Ev::now
