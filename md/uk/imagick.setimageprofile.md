---
navigation:
  - imagick.setimagepage.md: '« Imagick::setImagePage'
  - imagick.setimageproperty.md: 'Imagick::setImageProperty »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageProfile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageProfile

(PECL imagick 2, PECL imagick 3)

Imagick::setImageProfile — Додає іменований профіль до об'єкту Imagick

### Опис

```methodsynopsis
public Imagick::setImageProfile(string $name, string $profile): bool
```

Додає іменований профіль до об'єкту Imagick. Якщо профіль з такою назвою вже існує, він замінюється. Цей метод відрізняється від методу Imagick::ProfileImage() тим, що він не застосовує будь-які колірні профілі CMS.

### Список параметрів

`name`

`profile`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
