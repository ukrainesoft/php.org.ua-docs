Клас SwooleBuffer

-   [« Swoole\\Atomic::sub](swoole-atomic.sub.html)
    
-   [Swoole\\Buffer::append »](swoole-buffer.append.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleBuffer
    

# Клас SwooleBuffer

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Buffer
     
     {


    /* Методы */
    
   public append(string $data): int
public clear(): void
public __destruct(): void
public expand(int $size): int
public read(int $offset, int $length): string
public recycle(): void
public substr(int $offset, int $length = ?, bool $remove = ?): string
public __toString(): string
public write(int $offset, string $data): void

   }
```

## Зміст

-   [Swoole\\Buffer::append](swoole-buffer.append.html) — Додає рядок або двійкові дані до кінця буфера пам'яті та повертає новий розмір виділеної пам'яті
-   [Swoole\\Buffer::clear](swoole-buffer.clear.html) — скидає буфер пам'яті
-   [Swoole\\Buffer::\_\_construct](swoole-buffer.construct.html) - Фіксований розмір блоку пам'яті
-   [Swoole\\Buffer::\_\_destruct](swoole-buffer.destruct.html) - Знищує буфер пам'яті Swoole
-   [Swoole\\Buffer::expand](swoole-buffer.expand.html) - Розширює розмір буфера пам'яті
-   [Swoole\\Buffer::read](swoole-buffer.read.html) — Читає дані з буфера пам'яті на основі усунення та довжини
-   [Swoole\\Buffer::recycle](swoole-buffer.recycle.html) — Звільняє пам'ять для ОС, яка не використовується буфером пам'яті
-   [Swoole\\Buffer::substr](swoole-buffer.substr.html) — Зчитує дані з буфера пам'яті на основі усунення та довжини. Або видаляє дані з буфера пам'яті
-   [Swoole\\Buffer::\_\_toString](swoole-buffer.tostring.html) — Отримує строкове значення буфера пам'яті
-   [Swoole\\Buffer::write](swoole-buffer.write.html) — Записує дані у буфер пам'яті. Пам'ять, виділена для буфера, не буде змінено