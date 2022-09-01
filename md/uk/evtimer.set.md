---
navigation:
  - evtimer.createstopped.md: '« EvTimer::createStopped'
  - class.evwatcher.md: EvWatcher »
  - index.md: PHP Manual
  - class.evtimer.md: EvTimer
title: 'EvTimer::set'
---
# EvTimer::set

(PECL ev >= 0.2.0)

EvTimer::set — Налаштовує спостерігача

### Опис

```methodsynopsis
public
   EvTimer::set(
    float
     $after
   , 
    float
     $repeat
   ): void
```

Налаштовує спостерігача

### Список параметрів

`after`

Налаштовує таймер для запуску через `after` секунд.

`repeat`

Якщо час повтору дорівнює **`0.0`**, то він буде автоматично зупинено після закінчення часу очікування. Якщо позитивне, таймер буде автоматично налаштований на повторний запуск кожні повторювані секунди, доки не буде зупинено вручну.

### Значення, що повертаються

Функція не повертає значення після виконання.
