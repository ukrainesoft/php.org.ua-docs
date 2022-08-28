Поєднує одне або кілька зображень в одне зображення

-   [« Imagick::colorMatrixImage](imagick.colormatriximage.html)
    
-   [Imagick::commentImage »](imagick.commentimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Поєднує одне або кілька зображень в одне зображення
    

# Imagick::combineImages

(PECL imagick 2, PECL imagick 3)

Imagick::combineImages — Об'єднує одне або кілька зображень в одне зображення

### Опис

```methodsynopsis
public Imagick::combineImages(int $channelType): Imagick
```

Поєднує одне або кілька зображень в одне зображення. Значення відтінків сірого пікселів кожного зображення в послідовності надається по порядку зазначених каналів об'єднаного зображення. Типовий порядок: зображення 1 => червоний, 2 => зелений, 3 => синій і т.д.

### Список параметрів

`channelType`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.