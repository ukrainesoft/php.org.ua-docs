---
navigation:
  - gmagick.getimagescene.md: '« Gmagick::getimagescene'
  - gmagick.getimagetype.md: 'Gmagick::getimagetype »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::getimagesignature'
---
# Gmagick::getimagesignature

(PECL gmagick >= Unknown)

Gmagick::getimagesignature — Створює підпис повідомлення SHA-256

### Опис

```methodsynopsis
public Gmagick::getimagesignature(): string
```

Створює підпис повідомлення SHA-256 потоку пікселів зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що містить хеш SHA-256 файлу.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
