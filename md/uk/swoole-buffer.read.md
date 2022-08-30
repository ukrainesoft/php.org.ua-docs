Читає дані з буфера пам'яті на основі усунення та довжини

-   [« SwooleBuffer::expand](swoole-buffer.expand.html)
    
-   [SwooleBuffer::recycle »](swoole-buffer.recycle.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleBuffer](class.swoole-buffer.html)
    
-   Читає дані з буфера пам'яті на основі усунення та довжини
    

# SwooleBuffer::read

(PECL swoole >= 1.9.0)

SwooleBuffer::read — Читає дані з буфера пам'яті на основі зміщення та довжини

### Опис

```methodsynopsis
public Swoole\Buffer::read(int $offset, int $length): string
```

### Список параметрів

`offset`

Зміщення.

`length`

довжина.

### Значення, що повертаються

Дані, зчитані з буфера пам'яті.