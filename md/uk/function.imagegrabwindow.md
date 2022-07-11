- [«imagegrabscreen](function.imagegrabscreen.md)
- [imageinterlace »](function.imageinterlace.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Захоплює зображення вікна

#imagegrabwindow

(PHP 5 \>= 5.2.2, PHP 7, PHP 8)

imagegrabwindow — Захоплює зображення вікна

### Опис

**imagegrabwindow**(int `$handle`, bool `$client_area` = **`false`**):
[GdImage](class.gdimage.md)\|false

Знімок вікна або його клієнтської частини, використовуючи windows
обробник (властивість HWND COM об'єкта)

> **Примітка**:
>
> Функція доступна лише у Windows.

### Список параметрів

`handle`
ID вікна HWND.

`client_area`
Включає клієнтську частину вікна програми.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання, **`false`**
у разі виникнення помилки.

### Помилки

E_NOTICE видається, якщо `handle` є неприпустимим обробником
вікна. E_WARNING видається, якщо Windows API застаріла.

### Список змін

| Версія | Опис                                                                                                                           |
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0  | У разі успішного виконання, функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |
| 8.0.0  | client_area тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int).                                      |

### Приклади

**Приклад #1 Приклад використання **imagegrabwindow()****

Захоплення вікна (IE наприклад)

` <?php$browser = new COM("InternetExplorer.Application");$handle = $browser->HWND;$browser->Visible = true;$im = imagegrabwindow($handle);$browser->Quit() ;imagepng($im, "iesnap.png");imagedestroy($im);?> `

Захоплення вікна (IE наприклад) із вмістом

` <?php$browser = new COM("InternetExplorer.Application");$handle = $browser->HWND;$browser->Visible = true;$browser->Navigate("http://www.libgd.org ");/* ще працює? */while($browser->Busy) {    com_message_pump(4000);}$im = imagegrabwindow($handle, 0);$browser->Quit();imagepng($im, "iesnap.png");imagedes $im);?> `

### Дивіться також

- [imagegrabscreen()](function.imagegrabscreen.md) - Захоплює
зображення з екрану
