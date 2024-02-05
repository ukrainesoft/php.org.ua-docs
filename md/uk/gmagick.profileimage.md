---
navigation:
  - gmagick.previousimage.md: '« Gmagick::previousimage'
  - gmagick.quantizeimage.md: 'Gmagick::quantizeimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::profileimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::profileimage

(PECL gmagick >= Unknown)

Gmagick::profileimage — Додає або видаляє профіль із зображення.

### Опис

```methodsynopsis
public Gmagick::profileimage(string $name, string $profile): Gmagick
```

Додає або видаляє ICC, IPTC або загальний профіль зображення. Якщо значення profile дорівнює **`null`**, профиль удаляется из изображения, в противном случае добавляется. Используйте значение`*`для параметра name и\*\*`null`\*\* для параметра profile, щоб видалити всі профілі із зображення.

### Список параметрів

`name`

Ім'я профілю, який потрібно додати або видалити: ICC, IPTC або загальний профіль.

`profile`

Профіль.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
