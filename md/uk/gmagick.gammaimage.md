Гамма-корекція зображення

-   [« Gmagick::frameimage](gmagick.frameimage.md)
    
-   [Gmagick::getcopyright »](gmagick.getcopyright.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
-   Гамма-корекція зображення
    

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

Викликає **GmagickException** у разі виникнення помилки.