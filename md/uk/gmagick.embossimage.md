Повертає зображення у градаціях сірого з тривимірним ефектом

-   [« Gmagick::edgeimage](gmagick.edgeimage.html)
    
-   [Gmagick::enhanceimage »](gmagick.enhanceimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Повертає зображення у градаціях сірого з тривимірним ефектом
    

# Gmagick::embossimage

(PECL gmagick >= Unknown)

Gmagick::embossimage — Повертає зображення у градаціях сірого з тривимірним ефектом

### Опис

```methodsynopsis
public Gmagick::embossimage(float $radius, float $sigma): Gmagick
```

Повертає зображення у градаціях сірого із тривимірним ефектом. Ми згортаємо зображення за допомогою гаусівського оператора, заданого радіусу та стандартного відхилення (сигма). Для отримання розумних результатів радіус має бути більшим за сигму. При використанні радіуса 0, радіус вибереться автоматично.

### Список параметрів

`radius`

Радіус ефекту.

`sigma`

Сигма ефект.

### Значення, що повертаються

Рельєфний об'єкт [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.