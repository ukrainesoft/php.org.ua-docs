Створює нове зображення з файлу чи URL

-   [« imagecreatefromstring](function.imagecreatefromstring.html)
    
-   [imagecreatefromwbmp »](function.imagecreatefromwbmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Створює нове зображення з файлу чи URL
    

# imagecreatefromtga

(PHP 7> = 7.4.0, PHP 8)

imagecreatefromtga — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromtga(string $filename): GdImage|false
```

**imagecreatefromtga()** повертає об'єкт зображення, що представляє зображення, одержане з цього імені файлу.

### Список параметрів

`filename`

Шлях до зображення Truevision TGA.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                      |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс ([resource](language.types.resource.html) |