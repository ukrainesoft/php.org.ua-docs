---
navigation:
  - reserved.classes.md: «Зумовлені класи
  - reserved.other-reserved-words.md: Список інших зарезервованих слів »
  - index.md: PHP Manual
  - reserved.md: Список зарезервованих слів
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Обумовлені константи

### Обумовлені константи ядра

Ці константи визначені ядром PHP. Сюди входять PHP, двигун Zend та SAPI-модулі.

**`PHP_VERSION`**(string)

Поточна версія PHP у вигляді рядка у форматі «major.minor.release\[extra\]».

**`PHP_MAJOR_VERSION`**(int)

Поточна "основна" (major) версія PHP у вигляді цілого числа (наприклад, int(5) для версії "5.2.7-extra").

**`PHP_MINOR_VERSION`**(int)

Поточна "проміжна" (minor) версія PHP у вигляді цілого числа (наприклад, int(2) для версії "5.2.7-extra").

**`PHP_RELEASE_VERSION`**(int)

Поточна реліз-версія (release) PHP у вигляді цілого числа (наприклад, int(7) для версії 5.2.7-extra).

**`PHP_VERSION_ID`**(int)

Поточна версія PHP у вигляді цілого числа її зручно використовувати при порівняннях версій (наприклад, int(50207) для версії «5.2.7-extra»).

**`PHP_EXTRA_VERSION`**(string)

Поточна "екстра"-версія PHP у вигляді рядка (наприклад, "-extra" для версії "5.2.7-extra"). Зазвичай використовують у різних дистрибутивах для індикації версій пакетів.

**`ZEND_THREAD_SAFE`**(bool)

Вказує, чи поточна збірка PHP потокобезпечна.

**`ZEND_DEBUG_BUILD`**(bool)

Вказує, чи PHP для налагодження.

**`PHP_ZTS`**(int)

Вказує, чи поточна збірка PHP потокобезпечна.

**`PHP_DEBUG`**(int)

Вказує, чи PHP для налагодження.

**`PHP_MAXPATHLEN`**(int)

Максимальна довжина файлових імен (включаючи шлях), яку підтримує ця збірка PHP.

**`PHP_OS`**(string)

Операційна система, під яку збирався PHP.

**`PHP_OS_FAMILY`**(string)

Сімейство операційних систем, для яких зібрано PHP. Будь-яка з `«Windows»` `«BSD»` `«Darwin»` `«Solaris»` `«Linux»`или`«unknown»`Доступно с PHP 7.2.0.

**`PHP_SAPI`**(string)

API сервера (Server API) данной сборки PHP. Смотрите также[php\_sapi\_name()](function.php-sapi-name.md)

**`PHP_EOL`**(string)

Коректний символ кінця рядка (End Of Line) для платформи.

**`PHP_INT_MAX`**(int)

Максимальне ціле число, що підтримується збиранням PHP. Зазвичай це int(2147483647) у 32-бітових системах і int(9223372036854775807) у 64-бітних.

**`PHP_INT_MIN`**(int)

Мінімальне ціле число, що підтримується збиранням PHP. Зазвичай це int(-2147483648) у 32-бітових системах та int(-9223372036854775808) у 64-бітних. Зазвичай PHP\_INT\_MIN === ~PHP\_INT\_MAX.

**`PHP_INT_SIZE`**(int)

Розмір цілого числа в байтах у збиранні PHP.

**`PHP_FLOAT_DIG`**(int)

Кількість десяткових цифр, які можуть бути заокруглені в числі з плаваючою точкою (float) та назад без втрати точності. Доступно з PHP 7.2.0.

**`PHP_FLOAT_EPSILON`**(float)

Найменше уявне позитивне число x, таке, що `x + 1.0 != 1.0`Доступно с PHP 7.2.0.

**`PHP_FLOAT_MIN`**(float)

Наименьшее представимое*позитивне* число з плаваючою точкою float. Якщо потрібно найменше уявлення *негативне* число з плаваючою точкою float, вказують `- PHP_FLOAT_MAX`Доступно с PHP 7.2.0.

**`PHP_FLOAT_MAX`**(float)

Максимальне уявлене число з плаваючою точкою float. Доступно з PHP 7.2.0.

**`DEFAULT_INCLUDE_PATH`**(string)

**`PEAR_INSTALL_DIR`**(string)

**`PEAR_EXTENSION_DIR`**(string)

**`PHP_EXTENSION_DIR`**(string)

Каталог за замовчуванням, в якому потрібно шукати модулі, що динамічно завантажуються (якщо він не перевизначений директивою [extension\_dir](ini.core.md#ini.extension-dir)). По умолчанию —\*\*`PHP_PREFIX`\*\*(или`PHP_PREFIX . "\\ext"`в Windows).

**`PHP_PREFIX`**(string)

Значение**\--prefix** було встановлено під час налаштування. У Windows це значення **\--with-prefix** було встановлено під час налаштування.

**`PHP_BINDIR`**(string)

Значение**\--bindir** було встановлено під час налаштування. У Windows це значення **\--with-prefix** було встановлено під час налаштування.

**`PHP_BINARY`**(string)

Вказує шлях до файлів PHP, що виконуються під час виконання скрипту.

**`PHP_MANDIR`**(string)

Вказує, куди було встановлено сторінки керівництва (manpages).

**`PHP_LIBDIR`**(string)

**`PHP_DATADIR`**(string)

**`PHP_SYSCONFDIR`**(string)

**`PHP_LOCALSTATEDIR`**(string)

**`PHP_CONFIG_FILE_PATH`**(string)

**`PHP_CONFIG_FILE_SCAN_DIR`**(string)

**`PHP_SHLIB_SUFFIX`**(string)

Суфікс модулів платформи-складання, що розділяються (динамічних), наприклад, «so» (більшість Unix-систем) або «dll» (Windows).

**`PHP_FD_SETSIZE`**(int)

Максимальна кількість файлових дескрипторів для системних викликів. Доступно з PHP 7.1.0.

**`E_ERROR`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_WARNING`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_PARSE`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_NOTICE`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_CORE_ERROR`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_CORE_WARNING`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_COMPILE_ERROR`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_COMPILE_WARNING`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_USER_ERROR`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_USER_WARNING`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_USER_NOTICE`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_RECOVERABLE_ERROR`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_DEPRECATED`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_USER_DEPRECATED`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_ALL`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`E_STRICT`**(int)

[Константа повідомлення про помилку](errorfunc.constants.md)

**`__COMPILER_HALT_OFFSET__`**(int)

**`true`**(bool)

Смотрите раздел[Логічний тип](language.types.boolean.md)

**`false`**(bool)

Смотрите раздел[Логічний тип](language.types.boolean.md)

**`null`**(null)

Смотрите[Null](language.types.null.md)

**`PHP_WINDOWS_EVENT_CTRL_C`**(int)

Windows `CTRL + C`. Доступно з PHP 7.4.0 (лише для Windows).

**`PHP_WINDOWS_EVENT_CTRL_BREAK`**(int)

Windows `CTRL+BREAK`. Доступно з PHP 7.4.0 (лише для Windows).

Дивіться також: "[Магічні константи](language.constants.magic.md)».

### Стандартні визначені константи

Усі константи [модулів, що входять до складу ядра](extensions.membership.md#extensions.membership.core), тепер визначено в PHP за промовчанням.
