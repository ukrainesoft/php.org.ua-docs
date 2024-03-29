---
navigation:
  - ev.supportedbackends.md: '« Ev::supportedBackends'
  - ev.time.md: 'Ev::time »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::suspend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::suspend

(PECL ev >= 0.2.0)

Ev::suspend — Зупинити цикл подій за замовчуванням

### Опис

```methodsynopsis
final
   public
   static
   Ev::suspend(): void
```

Методи \*\*Ev::suspend()\*\*и[Ev::resume()](ev.resume.md)відповідно припиняють і відновлюють роботу подієвого циклу.

Всі спостерігачі таймери будуть затримані на час, що минув між *suspend*и*resume*, і всі спостерігачі типу *periodic* будуть переплановані (тобто будуть втрачені всі події, що сталися під час припинення).

Після виклику **Ev::suspend()** заборонено викликати будь-які функції циклу крім [Ev::resume()](ev.resume.md). Також забороняється викликати [Ev::resume()](ev.resume.md)якщо раніше не викликався **Ev::suspend()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::resume()](ev.resume.md) \- Відновити виконання призупиненого раніше циклу подій за умовчанням
