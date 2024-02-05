---
navigation:
  - gmagick.frameimage.md: '« Gmagick::frameimage'
  - gmagick.getcopyright.md: 'Gmagick::getcopyright »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::gammaimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::gammaimage

(PECL gmagick >= Unknown)

Gmagick::gammaimage — Гамма-корекція зображення

### Опис

```methodsynopsis
public Gmagick::gammaimage(float $gamma): Gmagick
```

Гамма-корекція зображення. Одне й те саме зображення, що переглядається різних пристроях, матиме перцепционные відмінності у способах представлення інтенсивності зображення на екрані. Вкажіть індивідуальні рівні гами для червоного, зеленого та синього каналів або налаштуйте всі три за допомогою параметра гами. Значення зазвичай коливаються від 08 до 23.

### Список параметрів

`gamma`

Кількість гамма-корекції.

### Значення, що повертаються

Гамма-скоригований об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
