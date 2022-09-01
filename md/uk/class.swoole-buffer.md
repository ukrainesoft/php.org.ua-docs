---
navigation:
  - swoole-atomic.sub.html: '« SwooleAtomic::sub'
  - swoole-buffer.append.html: 'SwooleBuffer::append »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleBuffer
---
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

-   [SwooleBuffer::append](swoole-buffer.append.html) — Додає рядок або двійкові дані до кінця буфера пам'яті та повертає новий розмір виділеної пам'яті
-   [SwooleBuffer::clear](swoole-buffer.clear.html) — скидає буфер пам'яті
-   [SwooleBuffer::construct](swoole-buffer.construct.html) - Фіксований розмір блоку пам'яті
-   [SwooleBuffer::destruct](swoole-buffer.destruct.html) - Знищує буфер пам'яті Swoole
-   [SwooleBuffer::expand](swoole-buffer.expand.html) - Розширює розмір буфера пам'яті
-   [SwooleBuffer::read](swoole-buffer.read.html) — Читає дані з буфера пам'яті на основі усунення та довжини
-   [SwooleBuffer::recycle](swoole-buffer.recycle.html) — Звільняє пам'ять для ОС, яка не використовується буфером пам'яті
-   [SwooleBuffer::substr](swoole-buffer.substr.html) — Зчитує дані з буфера пам'яті на основі усунення та довжини. Або видаляє дані з буфера пам'яті
-   [SwooleBuffer::toString](swoole-buffer.tostring.html) — Отримує строкове значення буфера пам'яті
-   [SwooleBuffer::write](swoole-buffer.write.html) — Записує дані у буфер пам'яті. Пам'ять, виділена для буфера, не буде змінено
