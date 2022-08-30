Налаштування під час виконання

-   [« Установка](outcontrol.installation.md)
    
-   [Типи ресурсів »](outcontrol.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](outcontrol.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції керування висновком**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [outputbuffering](outcontrol.configuration.html#ini.output-buffering) | "0" | PHPINIPERDIR |  |
| [outputhandler](outcontrol.configuration.html#ini.output-handler) | NULL | PHPINIPERDIR |  |
| [implicitflush](outcontrol.configuration.html#ini.implicit-flush) | "0" | PHPINIALL |  |
| [urlrewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags) | "a=href,area=href,frame=src,form=,fieldset=" | PHPINIALL | До PHP 7.1.0 використовувалася для встановлення перезапису сесії "trans sid". З PHP 7.1.0 використовується тільки [outputaddrewritevar()](function.output-add-rewrite-var.html) |
| [urlrewriter.hosts](outcontrol.configuration.html#ini.url-rewriter.hosts) | `$_SERVER['HTTP_HOST']` використовується за замовчуванням. | PHPINIALL | Доступно з PHP 7.1.0 |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`output_buffering` bool/integer

Ви можете дозволити буферизацію виводу всім файлів, встановивши цю директиву в 'On'. Якщо ви хочете обмежити розмір буфера до певного розміру, ви можете встановити не 'On', а максимальну кількість байт цієї директиви (наприклад, outputbuffering = 4096). Ця директива завжди вимкнена у PHP-CLI.

`output_handler` string

Ви можете перенаправити весь висновок вашого скрипта на функцію. Наприклад, якщо ви встановите outputhandler в [мбoutputhandler()](function.mb-output-handler.html), то кодування символів прозоро перетворюється відповідно до зазначеного кодування. Налаштування будь-якого обробника виводу автоматично включає буферизацію виводу.

> **Зауваження**
> 
> Ви не можете використовувати разом [мбoutputhandler()](function.mb-output-handler.html) з [проiconvhandler()](function.ob-iconv-handler.html), і ви не можете використовувати разом [проgzhandler()](function.ob-gzhandler.html) і [zlib.outputcompression](zlib.configuration.html#ini.zlib.output-compression)

> **Зауваження**
> 
> Тільки вбудовані функції можуть використовуватись із цією директивою. Для функції, визначеної користувачем, використовуйте [проstart()](function.ob-start.html)

`implicit_flush` bool

**`false`** за замовчуванням. Зміна значення на **`true`** вказує PHP не зберігати дані буфер, а після кожного відправленого блоку автоматично відправляти дані у вихідний шар. Це еквівалентно виклику PHP-функції [flush()](function.flush.md) після кожного виклику [print](function.print.md) або [echo](function.echo.md) для кожного `HTML`блоку.

При використанні PHP у веб-середовищі включення цієї опції призведе до серйозної втрати продуктивності, тому рекомендується використовувати її лише для налагодження. Це значення за замовчуванням має **`true`** при роботі в `CLI SAPI`

Зморите також [про implicit flush()](function.ob-implicit-flush.html)

`url_rewriter.tags` string

`url_rewriter.tags` визначає, які HTML-теги будуть перезаписані значеннями [outputaddrewritevar()](function.output-add-rewrite-var.html). За замовчуванням `a=href,area=href,frame=src,input=src,form=` `form` є спеціальним тегом . `<input hidden="session_id" name="session_name">` додається як змінна форми.

> **Зауваження**: До PHP 7.1.0 треба було використовувати [urlrewriter.tags](outcontrol.configuration.html#ini.url-rewriter.tags) для вказівки [session.transsidtags](session.configuration.html#ini.session.trans-sid-tags). Починаючи з PHP 7.1.0, `fieldset` більше не сприймається як спеціальний тег.

`url_rewriter.hosts` string

`url_rewriter.hosts` вказує, які хости перезаписуються для включення значень [outputaddrewritevar()](function.output-add-rewrite-var.html). За замовчуванням використовується `$_SERVER['HTTP_HOST']`. Декілька хостів можна вказати перерахувавши їх через кому, між хостами не повинно бути прогалин. Тобто `php.net,wiki.php.net,bugs.php.net`