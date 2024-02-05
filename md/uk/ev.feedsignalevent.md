---
navigation:
  - ev.feedsignal.md: '« Ev::feedSignal'
  - ev.iteration.md: 'Ev::iteration »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::feedSignalEvent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::feedSignalEvent

(No version information available, might only be in Git)

Ev::feedSignalEvent — Надіслати подію сигналу в цикл за замовчуванням

### Опис

```methodsynopsis
final
   public
   static
   Ev::feedSignalEvent(
    int
     $signum
   ): void
```

Надіслати подію сигналу в цикл за замовчуванням. Ev зреагує також, ніби було отримано зазначений сигнал `signal`

### Список параметрів

`signum`

Номер сигналу. Дивіться сторінку man `signal(7)`. Ви можете використовувати константи, експортовані з модуля `pcntl`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::feedSignal()](ev.feedsignal.md) \- Передаємо подію сигналу в Ev
