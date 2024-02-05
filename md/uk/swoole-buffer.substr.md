---
navigation:
  - swoole-buffer.recycle.md: '« Swoole\\Buffer::recycle'
  - swoole-buffer.tostring.md: 'Swoole\\Buffer::\_\_toString »'
  - index.md: PHP Manual
  - class.swoole-buffer.md: Swoole\\Buffer
title: 'Swoole\\Buffer::substr'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Buffer::substr

(PECL swoole >= 1.9.0)

Swoole\\Buffer::substr — Зчитує дані з буфера пам'яті на основі усунення та довжини. Або видаляє дані з буфера пам'яті

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
