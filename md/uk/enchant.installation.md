- [« Вимоги](enchant.requirements.md)
- [Налаштування під час виконання »](enchant.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](enchant.setup.md)
- Установка

## Установка

Якщо встановлено [потрібні бібліотеки](enchant.requirements.md), то
модуль можна встановити за допомогою опції **--with-enchant[=dir]** при
компіляції PHP.

Користувачі Windows повинні увімкнути `php_enchant.dll`, щоб
використовувати модуль.

> **Примітка**: **Додаткове налаштування у Windows**
>
> Для роботи цього модуля системної змінної Windows `PATH` мають бути
> Доступні файли DLL. Щоб дізнатися як цього досягти, зверніться до
> розділ FAQ "[Як додати мою директорію з PHP до змінної Windows > PATH](faq.installation.md#faq.installation.addtopath)". Хоча
> копіювання DLL-файлів із директорії PHP до системної папки Windows
> також вирішує проблему (бо системна директорія за замовчуванням
> перебуває у змінній `PATH`), це рекомендується. *Цьому модулю
> потрібні наступні файли в змінній `PATH`: * `libenchant.dll`,
> `glib-2.dll`, `gmodule-2.dll`.
>
> Крім того, необхідно скопіювати хоча б одного постачальника з
> `lib nchant` у `\usr\local\lib nchant-2` (це абсолютний шлях від
> кореня *поточного диска*). До версії PHP 8.0.0, тобто. при використанні
> Enchant v1, постачальники повинні були бути скопійовані в
> `C: nchant_plugins`, де цей шлях може бути налаштований шляхом створення
> значення реєстру
> `HKEY_CURRENT_USER\SOFTWARE\Enchant\Config\Module_Dir`, вказавши в ньому
> бажаний шлях.
