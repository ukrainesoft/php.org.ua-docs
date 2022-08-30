Компонує набір зображень

-   [« Imagick::clutImage](imagick.clutimage.md)
    
-   [Imagick::colorFloodfillImage »](imagick.colorfloodfillimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Компонує набір зображень
    

# Imagick::coalesceImages

(PECL imagick 2, PECL imagick 3)

Imagick::coalesceImages — Компонує набір зображень

### Опис

```methodsynopsis
public Imagick::coalesceImages(): Imagick
```

Скомпонований набір зображень із дотриманням будь-яких зсувів сторінок та методів видалення. Анімаційні послідовності GIF, MIFF та MNG зазвичай починаються з фону зображення, і кожне наступне зображення змінюється за розміром та зміщенням. Повертає новий об'єкт Imagick, де кожне зображення у послідовності має той самий розмір, що й перше і скомпоноване з наступним зображенням у послідовності.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий об'єкт Imagick у разі успішного виконання.

### Помилки

Викликає ImagickException у разі виникнення помилки.