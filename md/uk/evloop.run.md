---
navigation:
  - evloop.resume.md: '« EvLoop::resume'
  - evloop.signal.md: 'EvLoop::signal »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::run'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::run

(PECL ev >= 0.2.0)

EvLoop::run — Перевіряє події та викликає callback-функції у циклі

### Опис

```methodsynopsis
public
   EvLoop::run(
    int
     $flags
     = 0
   ): void
```

Перевіряє події та викликає callback-функції для поточного циклу подій. Повертає, коли зворотній виклик викликає метод [Ev::stop()](ev.stop.md), або якщо прапори ненульові (у цьому випадку повертається значення буде true) або коли немає активних спостерігачів, які посилаються на цикл ([EvWatcher::keepalive()](evwatcher.keepalive.md)имеет значение\*\*`true`\*\*), у цьому випадку повертається значення **`false`**. Значення, що повертається, як правило, можна інтерпретувати так, *якби воно було **`true`** і залишилося зробити ще багато роботи*

### Список параметрів

`flags`

Необов'язковий параметр `flags` може бути наступним:

**Список можливих значень `flags`**

| `flags` | Опис |
| --- | --- |
|  | Стандартна поведінка, описана вище |
| **`Ev::RUN_ONCE`** | Блокує не більше одного (чекає, але не зациклює) |
| **`Ev::RUN_NOWAIT`** | Не блокує нічого (витягує/обробляє події, але не чекає) |

Смотрите[константи прапора запуску](class.ev.md#ev.constants.run-flags)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::stop()](evloop.stop.md) \- зупиняє цикл подій
-   [Ev::run()](ev.run.md) \- Почати перевірку наявності подій та виклик callback-функцій циклу за умовчанням
