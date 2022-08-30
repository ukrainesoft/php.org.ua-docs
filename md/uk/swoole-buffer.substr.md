Зчитує дані з буфера пам'яті на основі зміщення та довжини. Або видаляє дані з буфера пам'яті

-   [« SwooleBuffer::recycle](swoole-buffer.recycle.html)
    
-   [SwooleBuffer::toString »](swoole-buffer.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleBuffer](class.swoole-buffer.html)
    
-   Зчитує дані з буфера пам'яті на основі зміщення та довжини. Або видаляє дані з буфера пам'яті
    

# SwooleBuffer::substr

(PECL swoole >= 1.9.0)

SwooleBuffer::substr — Зчитує дані з буфера пам'яті на основі усунення та довжини. Або видаляє дані з буфера пам'яті

### Опис

```methodsynopsis
public Swoole\Buffer::substr(int $offset, int $length = ?, bool $remove = ?): string
```

Якщо для $remove встановлено значення true, а для $offset встановлено значення 0, дані будуть видалені з буфера. Пам'ять для зберігання даних буде звільнено під час знищення об'єкта буфера.

### Список параметрів

`offset`

Зміщення.

`length`

довжина.

`remove`

Визначає, чи видалити дані з буфера пам'яті.

### Значення, що повертаються

Дані або рядок прочитані з буфера пам'яті.