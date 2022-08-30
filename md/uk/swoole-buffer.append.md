Додає рядок або двійкові дані до кінця буфера пам'яті та повертає новий розмір виділеної пам'яті

-   [« SwooleBuffer](class.swoole-buffer.html)
    
-   [SwooleBuffer::clear »](swoole-buffer.clear.html)
    
-   [PHP Manual](index.md)
    
-   [SwooleBuffer](class.swoole-buffer.html)
    
-   Додає рядок або двійкові дані до кінця буфера пам'яті та повертає новий розмір виділеної пам'яті
    

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