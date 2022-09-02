---
navigation:
  - reserved.classes.md: « Обумовлені класи
  - reserved.other-reserved-words.md: Список інших зарезервованих слів »
  - index.md: PHP Manual
  - reserved.md: Список зарезервованих слів
title: Обумовлені константи
---
## Обумовлені константи

### Оголошені в ядрі константи

Ці константи оголошуються ядром PHP та охоплюють PHP, Zend engine та SAPI-модулі.

**`PHP_VERSION`** (string)

Поточна версія PHP у вигляді рядка у форматі "major.minor.releaseextra".

**`PHP_MAJOR_VERSION`** (int)

Поточна "основна" (major) версія PHP як цілого числа (наприклад, int(5) для версії "5.2.7-extra").

**`PHP_MINOR_VERSION`** (int)

Поточна "проміжна" (minor) версія PHP як цілого числа (наприклад, int(2) для версії "5.2.7-extra").

**`PHP_RELEASE_VERSION`** (int)

Поточна "реліз"-версія (release) PHP як цілого числа (наприклад, int(7) для версії "5.2.7-extra").

**`PHP_VERSION_ID`** (int)

Поточна версія PHP у вигляді цілого числа її зручно використовувати при порівняннях версій (наприклад, int(50207) для версії "5.2.7-extra").

**`PHP_EXTRA_VERSION`** (string)

Поточна "екстра"-версія PHP у вигляді рядка (наприклад, '-extra' для версії "5.2.7-extra"). Зазвичай використовують у різних дистрибутивах для індикації версій пакетів.

**`PHP_ZTS`** (int)

**`PHP_DEBUG`** (int)

**`PHP_MAXPATHLEN`** (int)

Максимальна довжина файлових імен (включаючи шлях), яку підтримує ця збірка PHP.

**`PHP_OS`** (string)

Операційна система, під яку збирався PHP.

**`PHP_OS_FAMILY`** (string)

Сімейство операційних систем, для яких зібрано PHP. Будь-яка з `'Windows'` `'BSD'` `'Darwin'` `'Solaris'` `'Linux'` або `'unknown'`. Доступно з PHP 7.2.0.

**`PHP_SAPI`** (string)

API сервера (Server API) цієї збірки PHP. Дивіться також [phpsapiname()](function.php-sapi-name.md)

**`PHP_EOL`** (string)

Коректний символ кінця рядка, який використовується на даній платформі.

**`PHP_INT_MAX`** (int)

Максимальне ціле число, яке підтримує ця збірка PHP. Зазвичай це int(2147483647) у 32-бітових системах і int(9223372036854775807) у 64-бітних. Зазвичай, PHPINTMIN === ~PHPINTMAX.

**`PHP_INT_MIN`** (int)

Мінімальне ціле число, яке підтримує ця збірка PHP. Зазвичай це int(-2147483648) у 32-бітових системах та int(-9223372036854775808) у 64-бітних.

**`PHP_INT_SIZE`** (int)

Розмір цілого числа в байтах у поточному збиранні PHP.

**`PHP_FLOAT_DIG`** (int)

Кількість десяткових цифр, які можуть бути округлені в float і назад без втрати точності. Доступно з PHP 7.2.0.

**`PHP_FLOAT_EPSILON`** (float)

Найменше позитивне число x, таке, що `x + 1.0 != 1.0`. Доступно з PHP 7.2.0.

**`PHP_FLOAT_MIN`** (float)

Найменше можливе *позитивне* Число типу float. Якщо вам потрібно найменше можливе *негативне* число типу float, використовуйте `- PHP_FLOAT_MAX`. Доступно з PHP 7.2.0.

**`PHP_FLOAT_MAX`** (float)

Максимальна можлива кількість типу float. Доступно з PHP 7.2.0.

**`DEFAULT_INCLUDE_PATH`** (string)

**`PEAR_INSTALL_DIR`** (string)

**`PEAR_EXTENSION_DIR`** (string)

**`PHP_EXTENSION_DIR`** (string)

Каталог за замовчуванням, в якому слід шукати модулі, що динамічно завантажуються (якщо він не перевизначений в [extensiondir](ini.core.md#ini.extension-dir)). За замовчуванням використовується **`PHP_PREFIX`** (або `PHP_PREFIX . "\\ext"` у Windows).

**`PHP_PREFIX`** (string)

Значення **\-prefix** було встановлено під час налаштування. У Windows це значення **\-with-prefix** було встановлено під час налаштування.

**`PHP_BINDIR`** (string)

Значення **\-bindir** було встановлено під час налаштування. У Windows це значення **\-with-prefix** було встановлено під час налаштування.

**`PHP_BINARY`** (string)

Вказує шлях до файлів PHP, що виконуються під час виконання скрипту.

**`PHP_MANDIR`** (string)

Вказує шлях встановлення сторінок документації man.

**`PHP_LIBDIR`** (string)

**`PHP_DATADIR`** (string)

**`PHP_SYSCONFDIR`** (string)

**`PHP_LOCALSTATEDIR`** (string)

**`PHP_CONFIG_FILE_PATH`** (string)

**`PHP_CONFIG_FILE_SCAN_DIR`** (string)

**`PHP_SHLIB_SUFFIX`** (string)

Суфікс, що використовується для бібліотек, що динамічно лінуються, таких як "so" (для більшості Unix-систем) або "dll" (Windows).

**`PHP_FD_SETSIZE`** (string)

Максимальна кількість файлових дескрипторів для системних викликів. Доступно з PHP 7.1.0.

**`E_ERROR`** (int)

[Константа, яка вказує рівень повідомлень про помилки](errorfunc.constants.md)

**`E_WARNING`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_PARSE`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_NOTICE`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_CORE_ERROR`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_CORE_WARNING`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_COMPILE_ERROR`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_COMPILE_WARNING`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_USER_ERROR`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_USER_WARNING`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_USER_NOTICE`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_RECOVERABLE_ERROR`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_DEPRECATED`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_USER_DEPRECATED`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_ALL`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`E_STRICT`** (int)

[Константа сообщения об ошибке](errorfunc.constants.md)

**`__COMPILER_HALT_OFFSET__`** (int)

**`true`** (bool)

Дивіться розділ [Булев тип](language.types.boolean.md)

**`false`** (bool)

Дивіться розділ [Булев тип](language.types.boolean.md)

**`null`** (null)

Дивіться [Null](language.types.null.md)

**`PHP_WINDOWS_EVENT_CTRL_C`** (int)

Windows `CTRL+C`. Доступно з PHP 7.4.0 (лише для Windows).

**`PHP_WINDOWS_EVENT_CTRL_BREAK`** (int)

Windows `CTRL+BREAK`. Доступно з PHP 7.4.0 (лише для Windows).

Дивіться також: [Магічні константи](language.constants.magic.md)

### Стандартні визначені константи

Усі константи [модулів, що входять до складу ядра](extensions.membership.md#extensions.membership.core), тепер визначено в PHP за промовчанням.
