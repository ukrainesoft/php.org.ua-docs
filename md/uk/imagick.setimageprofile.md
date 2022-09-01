---
navigation:
  - imagick.setimagepage.html: '« Imagick::setImagePage'
  - imagick.setimageproperty.html: 'Imagick::setImageProperty »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::setImageProfile'
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
