---
navigation:
  - swoole-buffer.tostring.html: '« SwooleBuffer::toString'
  - class.swoole-channel.html: SwooleChannel »
  - index.md: PHP Manual
  - class.swoole-buffer.html: SwooleBuffer
title: 'SwooleBuffer::write'
---
# SwooleBuffer::write

(PECL swoole >= 1.9.0)

SwooleBuffer::write — записує дані до буфера пам'яті. Пам'ять, виділена для буфера, не буде змінено

### Опис

```methodsynopsis
public Swoole\Buffer::write(int $offset, string $data): void
```

### Список параметрів

`offset`

Зміщення.

`data`

Дані для запису буфер пам'яті.

### Значення, що повертаються
