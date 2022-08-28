Захоплює зображення вікна

-   [« imagegrabscreen](function.imagegrabscreen.html)
    
-   [imageinterlace »](function.imageinterlace.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Захоплює зображення вікна
    

# imagegrabwindow

(PHP 5> = 5.2.2, PHP 7, PHP 8)

imagegrabwindow — Захоплює зображення вікна

### Опис

```methodsynopsis
imagegrabwindow(int $handle, bool $client_area = false): GdImage|false
```

Робить знімок вікна або його клієнтської частини, використовуючи windows обробник (властивість HWND COM об'єкта)

> **Зауваження**
> 
> Функція доступна лише у Windows.

### Список параметрів

`handle`

ID вікна HWND.

`client_area`

Включає клієнтську частину вікна програми.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання, **`false`** у разі виникнення помилки.

### Помилки

ЕNOTICE видається, якщо `handle` є неприпустимим обробником вікна. EWARNING видається, якщо Windows API застарів.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс (resource). |
|  | `client_area` тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int). |

### Приклади

**Приклад #1 Приклад використання **imagegrabwindow()****

Захоплення вікна (IE наприклад)

```php
<?php
$browser = new COM("InternetExplorer.Application");
$handle = $browser->HWND;
$browser->Visible = true;
$im = imagegrabwindow($handle);
$browser->Quit();
imagepng($im, "iesnap.png");
imagedestroy($im);
?>
```

Захоплення вікна (IE наприклад) із вмістом

```php
<?php
$browser = new COM("InternetExplorer.Application");
$handle = $browser->HWND;
$browser->Visible = true;
$browser->Navigate("http://www.libgd.org");

/* ещё работает? */
while ($browser->Busy) {
    com_message_pump(4000);
}
$im = imagegrabwindow($handle, 0);
$browser->Quit();
imagepng($im, "iesnap.png");
imagedestroy($im);
?>
```

### Дивіться також

-   [imagegrabscreen()](function.imagegrabscreen.html) - Захоплює зображення з екрану