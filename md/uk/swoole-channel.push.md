---
navigation:
  - swoole-channel.pop.md: '« SwooleChannel::pop'
  - swoole-channel.stats.md: 'SwooleChannel::stats »'
  - index.md: PHP Manual
  - class.swoole-channel.md: SwooleChannel
title: 'SwooleChannel::push'
---
# SwooleChannel::push

(PECL swoole >= 1.9.0)

SwooleChannel::push — Записує та передає дані в канал Swoole

### Опис

```methodsynopsis
public Swoole\Channel::push(string $data): bool
```

Дані можуть бути будь-якою непустою змінною PHP, змінна буде серіалізована, якщо вона не є рядковим типом.

Якщо розмір даних перевищує 8 КБ, канал Swoole використовуватиме тимчасові сховища файлів.

Функція поверне true, якщо операцію запису виконано успішно або false, якщо недостатньо місця.

### Список параметрів

`data`

Дані для вставки у канал Swoole.

### Значення, що повертаються

Чи передалися дані до каналу Swoole.
