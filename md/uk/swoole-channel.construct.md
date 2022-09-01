---
navigation:
  - class.swoole-channel.html: « SwooleChannel
  - swoole-channel.destruct.html: 'SwooleChannel::destruct »'
  - index.md: PHP Manual
  - class.swoole-channel.html: SwooleChannel
title: 'SwooleChannel::construct'
---
# SwooleChannel::construct

(PECL swoole >= 1.9.0)

SwooleChannel::construct — Створює канал Swoole

### Опис

public **SwooleChannel::construct**(string `$size`

Канал Swoole - це структура даних у пам'яті, яка працює як Chan в Golang, реалізована на основі пам'яті, що розділяється, і мьютексів. Може використовуватись як високопродуктивна черга повідомлень у пам'яті. Створення каналу Swoole із фіксованим розміром. Мінімальний розмір каналу Swoole складає 64 КБ. Викинуть винятки, якщо недостатньо пам'яті.

### Список параметрів

`size`

Розмір каналу Swoole.
