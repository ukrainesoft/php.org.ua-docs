---
navigation:
  - imagick.clippathimage.md: '« Imagick::clipPathImage'
  - imagick.clutimage.md: 'Imagick::clutImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::clone'
---
# Imagick::clone

(PECL imagick 2, PECL imagick 3)

Imagick::clone — Створює точну копію об'єкту Imagick

### Опис

```methodsynopsis
public Imagick::clone(): Imagick
```

Створює точну копію об'єкту Imagick.

**Увага**

Функція застаріла (*DEPRECATED*) з imagick версії 3.1.0, замість неї використовуйте ключове слово [clone](language.oop5.cloning.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повернеться копія об'єкта Imagick.

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 3.1.0 | Метод застарів на користь ключового слова [clone](language.oop5.cloning.md) |

### Приклади

**Приклад #1 Клонування об'єкта Imagick у різних версіях**

```php
<?php
// Клонирование объекта Imagick в imagick 2.x и 3.0:
$newImage = $image->clone();

// Клонирование объекта Imagick с версии 3.1.0:
$newImage = clone $image;
?>
```
