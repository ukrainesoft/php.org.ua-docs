---
navigation:
  - imagick.getimageprofile.md: '« Imagick::getImageProfile'
  - imagick.getimageproperties.md: 'Imagick::getImageProperties »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageProfiles'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageProfiles

(PECL imagick 2, PECL imagick 3)

Imagick::getImageProfiles — Повертає профілі зображень

### Опис

```methodsynopsis
public Imagick::getImageProfiles(string $pattern = "*", bool $include_values = true): array
```

Повертає всі пов'язані профілі, які відповідають шаблону. Якщо в якості другого параметра передається **`false`**, повертаються лише імена профілів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`pattern`

Шаблон для назв профілів.

`include_values`

Визначає, чи потрібно повертати лише імена профілів. Якщо передано значення **`false`** то будуть повернуті лише імена профілів.

### Значення, що повертаються

Повертає масив, який містить профілі зображень або імена профілів.
