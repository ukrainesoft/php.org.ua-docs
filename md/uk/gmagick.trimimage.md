---
navigation:
  - gmagick.thumbnailimage.md: '« Gmagick::thumbnailimage'
  - gmagick.write.md: 'Gmagick::write »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::trimimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::trimimage

(PECL gmagick >= Unknown)

Gmagick::trimimage — Видаляє краї зображення

### Опис

```methodsynopsis
public Gmagick::trimimage(float $fuzz): Gmagick
```

Видаляє краї, які є кольором фону із зображенням.

### Список параметрів

`fuzz`

За замовчуванням ціль повинна точно відповідати певному кольору пікселя. Однак у багатьох випадках два кольори можуть трохи відрізнятися. Розмитий елемент зображення визначає, наскільки можна визначати, щоб два кольори вважалися однаковими. Параметр є зміною квантового діапазону.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
