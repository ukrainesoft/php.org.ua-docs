---
navigation:
  - gmagick.setimageiterations.md: '« Gmagick::setimageiterations'
  - gmagick.setimageredprimary.md: 'Gmagick::setimageredprimary »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimageprofile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setimageprofile

(PECL gmagick >= Unknown)

Gmagick::setimageprofile — Додає іменований профіль до об'єкту Gmagick

### Опис

```methodsynopsis
public Gmagick::setimageprofile(string $name, string $profile): Gmagick
```

Додає іменований профіль об'єкт Gmagick. Якщо профіль з такою назвою вже існує, він замінюється. Метод відрізняється від методу Gmagick::profileimage() тим, що він не застосовує колірні профілі CMS.

### Список параметрів

`name`

Ім'я профілю для додавання або видалення: ICC, IPTC або загальний профіль.

`profile`

Профіль.

### Значення, що повертаються

Об'єкт Gmagick у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
