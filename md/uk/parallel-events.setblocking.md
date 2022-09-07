---
navigation:
  - class.parallel-events.md: « parallelEvents
  - parallel-events.settimeout.md: 'parallelEvents::setTimeout »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallelEvents
title: 'parallelEvents::setBlocking'
---
# parallelEvents::setBlocking

parallelEvents::setBlocking — Поведінка

### Опис

За замовчуванням, коли опитуються події, блокування відбуватиметься (на рівні PHP) доти, доки не буде повернена перша подія: встановлення режиму блокування в **`false`** призведе до того, що опитування поверне управління, якщо перша мета не готова.

Відрізняється від часу очікування 0 за допомогою [parallelEvents::setTimeout()](parallel-events.settimeout.md), оскільки час очікування 0, хоч і дозволено, викине виняток, який може бути надзвичайно повільним або марнотратним, якщо дійсно потрібна неблокуюча поведінка.

Неблокуючий цикл впливає на значення, що повертається [parallelEvents::poll()](parallel-events.poll.md)так воно може бути **`null`** до того, як усі події будуть опрацьовані.

```methodsynopsis
public parallel\Events::setBlocking(bool $blocking): void
```

Встановлює режим блокування

### Помилки

**Увага**

Викидає parallelEventsError, якщо для циклу встановлено час очікування.
