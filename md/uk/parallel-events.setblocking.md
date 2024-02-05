---
navigation:
  - class.parallel-events.md: « parallel\\Events
  - parallel-events.settimeout.md: 'parallel\\Events::setTimeout »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallel\\Events
title: 'parallel\\Events::setBlocking'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events::setBlocking

(0.9.0)

parallel\\Events::setBlocking — Поведінка

### Опис

За замовчуванням, коли опитуються події, блокування відбуватиметься (на рівні PHP) доти, доки не буде повернена перша подія: встановлення режиму блокування в **`false`** призведе до того, що опитування поверне управління, якщо перша мета не готова.

Отличается от установки времени ожидания 0 с помощью[parallel\\Events::setTimeout()](parallel-events.settimeout.md), оскільки час очікування 0, хоч і дозволено, викине виняток, який може бути надзвичайно повільним або марнотратним, якщо дійсно потрібна неблокуюча поведінка.

Неблокирующий цикл влияет на возвращаемое значение[parallel\\Events::poll()](parallel-events.poll.md)так воно може бути **`null`** до того, як усі події будуть опрацьовані.

```methodsynopsis
public parallel\Events::setBlocking(bool $blocking): void
```

Встановлює режим блокування

### Помилки

**Увага**

Викидає parallel\\Events\\Error, якщо для циклу встановлено час очікування.
