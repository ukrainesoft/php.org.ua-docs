---
navigation:
  - class.swoole-channel.md: « Swoole\\Channel
  - swoole-channel.destruct.md: 'Swoole\\Channel::\_\_destruct »'
  - index.md: PHP Manual
  - class.swoole-channel.md: Swoole\\Channel
title: 'Swoole\\Channel::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Channel::\_\_construct

(PECL swoole >= 1.9.0)

Swoole\\Channel::\_\_construct — Створює канал Swoole

### Опис

public**Swoole\\Channel::\_\_construct**(string`$size`) .

Канал Swoole - це структура даних у пам'яті, яка працює як Chan в Golang, реалізована на основі пам'яті, що розділяється, і мьютексів. Може використовуватись як високопродуктивна черга повідомлень у пам'яті. Створення каналу Swoole із фіксованим розміром. Мінімальний розмір каналу Swoole складає 64 КБ. Викинуть винятки, якщо недостатньо пам'яті.

### Список параметрів

`size`

Розмір каналу Swoole.
