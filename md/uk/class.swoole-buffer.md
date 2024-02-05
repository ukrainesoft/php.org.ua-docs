---
navigation:
  - swoole-atomic.sub.md: '« Swoole\\Atomic::sub'
  - swoole-buffer.append.md: 'Swoole\\Buffer::append »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Buffer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Buffer

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

-   [Swoole\\Buffer::append](swoole-buffer.append.md)— Додає рядок або двійкові дані до кінця буфера пам'яті та повертає новий розмір виділеної пам'яті
-   [Swoole\\Buffer::clear](swoole-buffer.clear.md)— скидає буфер пам'яті
-   [Swoole\\Buffer::\_\_construct](swoole-buffer.construct.md) \- Фіксований розмір блоку пам'яті
-   [Swoole\\Buffer::\_\_destruct](swoole-buffer.destruct.md) \- Знищує буфер пам'яті Swoole
-   [Swoole\\Buffer::expand](swoole-buffer.expand.md) \- Розширює розмір буфера пам'яті
-   [Swoole\\Buffer::read](swoole-buffer.read.md)— Читає дані з буфера пам'яті на основі усунення та довжини
-   [Swoole\\Buffer::recycle](swoole-buffer.recycle.md)— Звільняє пам'ять для ОС, яка не використовується буфером пам'яті
-   [Swoole\\Buffer::substr](swoole-buffer.substr.md)— Зчитує дані з буфера пам'яті на основі усунення та довжини. Або видаляє дані з буфера пам'яті
-   [Swoole\\Buffer::\_\_function toString() { \[native code\] }](swoole-buffer.tostring.md)— Отримує строкове значення буфера пам'яті
-   [Swoole\\Buffer::write](swoole-buffer.write.md)— Записує дані у буфер пам'яті. Пам'ять, виділена для буфера, не буде змінено
