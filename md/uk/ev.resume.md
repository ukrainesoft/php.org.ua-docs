---
navigation:
  - ev.recommendedbackends.md: '« Ev::recommendedBackends'
  - ev.run.md: 'Ev::run »'
  - index.md: PHP Manual
  - class.ev.md: Єв
title: 'Ev::resume'
---
# Ev::resume

(PECL ev >= 0.2.0)

Ev::resume — Відновити виконання призупиненого раніше циклу подій за умовчанням

### Опис

```methodsynopsis
final
   public
   static
   Ev::resume(): void
```

Методи [Ev::suspend()](ev.suspend.md) і \*\*Ev::resume()\*\*відповідно припиняють і відновлюють роботу подієвого циклу.

Всі спостерігачі таймери будуть затримані на час, що минув між *suspend* і *resume*, і всі спостерігачі типу *periodic* будуть переплановані watchers will be rescheduled(тобто будуть втрачені всі події, що сталися під час припинення).

Після виклику [Ev::suspend()](ev.suspend.md) заборонено викликати будь-які функції циклу крім **Ev::resume()**. Також забороняється викликати **Ev::resume()** якщо раніше не викликався [Ev::suspend()](ev.suspend.md)

Виклик *suspend* *resume* мають побічні ефекти для оновлення часу подієвого циклу (див. [Ev::nowUpdate()](ev.nowupdate.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::suspend()](ev.suspend.md) - Зупинити подійний цикл за замовчуванням
