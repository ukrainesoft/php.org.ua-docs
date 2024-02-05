---
navigation:
  - gmagick.hasnextimage.md: '« Gmagick::hasnextimage'
  - gmagick.implodeimage.md: 'Gmagick::implodeimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::haspreviousimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::haspreviousimage

(PECL gmagick >= Unknown)

Gmagick::haspreviousimage — Перевіряє, чи є ще зображення в об'єкті під час ітерації назад

### Опис

```methodsynopsis
public Gmagick::haspreviousimage(): mixed
```

Повертає **`true`**, якщо при ітерації назад у списку є зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если при итерации назад по списку есть изображения и\*\*`false`\*\*, якщо ні.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
