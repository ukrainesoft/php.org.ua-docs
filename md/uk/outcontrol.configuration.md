---
navigation:
  - outcontrol.installation.md: « Встановлення
  - outcontrol.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - outcontrol.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції керування висновком**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [output\_buffering](outcontrol.configuration.md#ini.output-buffering) | `«0»` | **`INI_PERDIR`** |  |
| [output\_handler](outcontrol.configuration.md#ini.output-handler) | **`null`** | **`INI_PERDIR`** |  |
| [implicit\_flush](outcontrol.configuration.md#ini.implicit-flush) | `«0»` | **`INI_ALL`** |  |
| [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags) | `«form=»` | **`INI_ALL`** | Починаючи з PHP 7.1.0 ця INI-настройка впливає лише на функцію [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md). . До PHP 7.1.0 ця INI-настройка включала підтримку прозорого ідентифікатора сеансу (див. опис директиви [session.trans\_sid\_tags](session.configuration.md#ini.session.trans-sid-tags)). функцію. |
| [url\_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts) | `$_SERVER['HTTP_HOST']` встановлено за замовчуванням. | **`INI_ALL`** | Доступно з PHP 7.1.0 |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`output_buffering`bool/integer

Щоб увімкнути буферизацію виводу для всіх файлів, директиві встановлюють значення `«On»`. Щоб обмежити розмір буфера, замість `«On»` можна вказати число, яке відповідатиме кількості байтів, що обмежують розмір буфера. Наприклад - `output_buffering=4096`

`output_handler`string

Дозволено перенаправляти виведення скриптів у функцію. Наприклад, якщо встановити функцію [mb\_output\_handler()](function.mb-output-handler.md) як значення директиви `output_handler`, кодування символів буде прозоро перетворюватися на задане кодування. Установка будь-якого обробника виводу автоматично включає буферизацію виводу.

> **Зауваження** :
> 
> Не можна використовувати разом функції [mb\_output\_handler()](function.mb-output-handler.md) і [ob\_iconv\_handler()](function.ob-iconv-handler.md), а функцию[ob\_gzhandler()](function.ob-gzhandler.md) та директиву [zlib.output\_compression](zlib.configuration.md#ini.zlib.output-compression) не можна використовувати з жодним з наступних: з функцією [mb\_output\_handler()](function.mb-output-handler.md), з функцією [ob\_gzhandler()](function.ob-gzhandler.md), з директивою [zlib.output\_compression](zlib.configuration.md#ini.zlib.output-compression), з обробником «URL-Rewriter» (дивіться опис директиви [session.use\_trans\_sid](session.configuration.md#ini.session.use-trans-sid) та функції [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)

> **Зауваження** :
> 
> З директивою можна використовувати лише вбудовані функції. Для функцій користувача викликають функцію [ob\_start()](function.ob-start.md)

`implicit_flush`bool

Значение по умолчанию —\*\*`false`**Изменение значения на**`true`\*\* вказує PHP не зберігати дані у буфер, а після кожного відправленого блоку автоматично надсилати дані у вихідний шар. Це еквівалентно виклику PHP-функції [flush()](function.flush.md) після кожного виклику функції виводу (наприклад, [print](function.print.md) або [echo](function.echo.md)) та кожного `HTML`\-блоку.

При використанні PHP у веб-середовищі включення цієї опції призведе до серйозної втрати продуктивності, тому рекомендується використовувати її лише для налагодження. Це значення за замовчуванням має \*\*`true`\*\*при работе в`CLI SAPI`

Сморите также[ob\_implicit\_flush()](function.ob-implicit-flush.md)

`url_rewriter.tags`string

Директива`url_rewriter.tags` визначає HTML-теги та атрибути, в яких URL-адреси перезаписуються значеннями функції [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)Значение по умолчанию —`«form=»`Добавление значения`«form=»` або будь-якого атрибуту форми (`form`) додати прихований елемент `input`к форме (`form`), з артибутом із зазначеними ім'ям та значенням для кожної пари ім'я-значення, переданої у функцію [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)

**Застереження**

Якщо у директиву `url_rewriter.tags` додати той самий тег більше одного разу, при перезапису URL буде оброблено тільки перше входження.

> **Зауваження**: До PHP 7.1.0 треба було використовувати [url\_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags)для указания[session.trans\_sid\_tags](session.configuration.md#ini.session.trans-sid-tags)

`url_rewriter.hosts`string

Директива`url_rewriter.hosts` вказує, які хости перезаписуються, щоб увімкнути в них значення функції [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)По умолчанию директиве установлено значение`$_SERVER['HTTP_HOST']`. Дозволено вказувати кілька хостів, перерахувавши їх через кому без прогалин. Наприклад, `«php.net,wiki.php.net,bugs.php.net»`
