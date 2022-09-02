---
navigation:
  - class.swoole-buffer.md: « SwooleBuffer
  - swoole-buffer.clear.md: 'SwooleBuffer::clear »'
  - index.md: PHP Manual
  - class.swoole-buffer.md: SwooleBuffer
title: 'SwooleBuffer::append'
---
# SwooleBuffer::append

(PECL swoole >= 1.9.0)

SwooleBuffer::append — Додає рядок або двійкові дані до кінця буфера пам'яті і повертає новий розмір виділеної пам'яті

### Опис

```methodsynopsis
public Swoole\Buffer::append(string $data): int
```

### Список параметрів

`data`

Рядок або двійкові дані, що додаються до кінця буфера пам'яті.

### Значення, що повертаються

Новий розмір буфера пам'яті.
