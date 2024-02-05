---
navigation:
  - function.imagegrabscreen.md: « imagegrabscreen
  - function.imageinterlace.md: imageinterlace »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegrabwindow
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagegrabwindow

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

imagegrabwindow — Захоплює зображення вікна

### Опис

```methodsynopsis
imagegrabwindow(int $handle, bool $client_area = false): GdImage|false
```

Робить знімок вікна або його клієнтської частини, використовуючи windows обробник (властивість HWND COM об'єкта)

> **Зауваження** :
> 
> Функція доступна лише у Windows.

### Список параметрів

`handle`

ID вікна HWND.

`client_area`

Включає клієнтську частину вікна програми.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання, \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

E\_NOTICE видається, якщо `handle` є неприпустимим обробником вікна. E\_WARNING видається, якщо Windows API застарів.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |
| 8.0.0 | `client_area` тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int). |

### Приклади

**Пример #1 Пример использования**imagegrabwindow()\*\*\*\*

Захоплення вікна (IE наприклад)

```php
<?php
$browser = new COM("InternetExplorer.Application");
$handle = $browser->HWND;
$browser->Visible = true;
$im = imagegrabwindow($handle);
$browser->Quit();
imagepng($im, "iesnap.png");
imagedestroy($im);
?>
```

Захоплення вікна (IE наприклад) із вмістом

```php
<?php
$browser = new COM("InternetExplorer.Application");
$handle = $browser->HWND;
$browser->Visible = true;
$browser->Navigate("http://www.libgd.org");

/* ещё работает? */
while ($browser->Busy) {
    com_message_pump(4000);
}
$im = imagegrabwindow($handle, 0);
$browser->Quit();
imagepng($im, "iesnap.png");
imagedestroy($im);
?>
```

### Дивіться також

-   [imagegrabscreen()](function.imagegrabscreen.md) \- Захоплює зображення з екрану
