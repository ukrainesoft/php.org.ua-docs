- [« Вимоги](mysql.requirements.md)
- [Налаштування під час виконання »](mysql.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](mysql.setup.md)
- Встановлення

## Установка

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений до PHP 7.0.0.
Використовуйте замість нього [MySQLi](book.mysqli.md) або
[PDO_MySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

Для компіляції просто використовуйте опцію конфігурації
**--with-mysql[=DIR]**, де необов'язковий параметр `[DIR]` вказує
на директорію із встановленим MySQL.

Незважаючи на те, що модуль MySQL сумісний з MySQL 4.1.0 та вище, він не
підтримує додаткову функціональність, що надається цими
версіями. Для отримання такої можливості скористайтесь модулем [MySQLi](book.mysqli.md).

Якщо ви хочете встановити модуль mysql спільно з mysqli, то для
уникнення будь-яких конфліктів необхідно використовувати ту саму
клієнтську бібліотеку.

## Установка на Linux-системи

Примітка: `[DIR]` є шляхом до файлів клієнтської бібліотеки MySQL
(*заголовкам та бібліотекам*), які можна завантажити з
[»MySQL](http://www.mysql.com/).

| PHP Версія          | За замовчуванням | Опції налаштування: [mysqlnd](mysqlnd.overview.md) | Опції налаштування: libmysqlclient  | Список змін                                                                                                   |
| ------------------- | ---------------- | -------------------------------------------------- | ----------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| 4.x.x               | libmysqlclient   | Недоступний                                        | **--without-mysql** для відключення | MySQL включений за замовчуванням, клієнтські бібліотеки MySQL входять до постачання PHP                       |
| 5.0.x, 5.1.x, 5.2.x | libmysqlclient   | Недоступний                                        | **--with-mysql=[DIR]**              | MySQL більше не включений за замовчуванням, і клієнтські бібліотеки MySQL більше не входять до постачання PHP |
| 5.3.x               | libmysqlclient   | **--with-mysql=mysqlnd**                           | **--with-mysql=[DIR]**              | Став доступним mysqlnd                                                                                        |
| 5.4.x               | mysqlnd          | **--with-mysql**                                   | **--with-mysql=[DIR]**              | mysqlnd вибирається за замовчуванням                                                                          |

**Таблиця компіляції ext/mysql за версіями PHP**

## Встановлення на Windows-системи

## PHP 5.0.x, 5.1.x, 5.2.x

Підтримка MySQL більше не включена за замовчуванням, тому для неї
включення необхідно підключити `php_mysql.dll` DLL всередині `php.ini`.
Крім цього, PHP знадобиться доступ до клієнтської бібліотеки MySQL. Файл
`libmysql.dll` поставляється у Windows дистрибутиві PHP, і для
коректного спілкування PHP з MySQL, цей файл повинен бути доступний
системному шляху Windows `PATH`. Про те, як це зробити, дивіться FAQ "[Як
додати мою PHP директорію в системний `PATH` на Windows?](faq.installation.md#faq.installation.addtopath)". Хоча
копіювання `libmysql.dll` у системну папку Windows також спрацює
(оскільки системна папка знаходиться за умовчанням в `PATH`), це не
рекомендується.

Як і при включенні будь-якого іншого модуля PHP (в тому числі і
`php_mysql.dll`), директива
[extension_dir](ini.core.md#ini.extension-dir) має вказувати на
директорію, що містить PHP-модулі. Дивіться також [Інструкції з ручної роботи інсталяції у Windows](install.windows.manual.md) . Приклад значення
extension_dir для PHP 5: `c:\php xt`

> **Примітка**:
>
> Якщо під час старту веб-сервера відбувається подібна помилка:
> ``Unable to load dynamic library './php_mysql.dll''`, ("Неможливо
> підвантажити динамічну бібліотеку './php_mysql.dll'), то це
> трапляється через те, що на вашій системі не може бути знайдено
> `php_mysql.dll` та/або `libmysql.dll`.

## PHP 5.3.0+

[MySQL Native Driver](mysqlnd.overview.md) включений за замовчуванням. В тому
числа `php_mysql.dll`, але без вимоги та використання `libmysql.dll`.

## Зауваження щодо встановлення MySQL

**Увага**

Збої в роботі PHP можуть виникнути при завантаженні цього модуля разом з
модулем recode. За додатковою інформацією звертайтесь до розділу
модуль для [recode](ref.recode.md).

> **Примітка**:
>
> Якщо вам потрібна підтримка кодувань, відмінних від *latin*,
> (за замовчуванням), вам доведеться встановити зовнішню
> бібліотеку libmysqlclient, скомпільовану з їхньою підтримкою.
