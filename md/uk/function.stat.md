- [«set_file_buffer](function.set-file-buffer.md)
- [symlink »](function.symlink.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Повертає інформацію про файл

# stat

(PHP 4, PHP 5, PHP 7, PHP 8)

stat — Повертає інформацію про файл

### Опис

**stat**(string `$filename`): array\|false

Збирає статистичну інформацію про файл `filename`. Якщо `filename`
є символічним посиланням, інформація збирається про сам файл, а
не посилання. До PHP 7.4.0 у Windows NTS у цьому випадку будував статистику
`size`, `atime`, `mtime` та `ctime` із символьного посилання.

Функція [lstat()](function.lstat.md) ідентична функції **stat()** за
виключенням того, що в цьому випадку вона поверне інформацію про саму
символічне посилання.

### Список параметрів

`filename`
Шлях до файлу.

### Значення, що повертаються

| Числовий | Асоціативний | Опис                                                  |
|----------|--------------|-------------------------------------------------------|
| 0        | dev          | номер пристрою \*\*\*                                 |
| 1        | ino          | номер inode \*\*\*\*                                  |
| 2        | mode         | режим захисту inode \*\*\*\*\*                        |
| 3        | nlink        | кількість посилань                                    |
| 4        | uid          | userid власника \*                                    |
| 5        | gid          | groupid власника \*                                   |
| 6        | rdev         | тип пристрою, якщо пристрій inode                     |
| 7        | size         | розмір у байтах                                       |
| 8        | atime        | час останнього доступу (тимчасова мітка Unix)         |
| 9        | mtime        | час останньої модифікації (тимчасова мітка Unix)      |
| 10       | ctime        | час останньої зміни inode (тимчасова мітка Unix)      |
| 11       | blksize      | розмір блоку введення-виведення файлової системи \*\* |
| 12       | blocks       | кількість використовуваних 512-байтних блоків \*\*    |

**Формат результату роботи функцій **stat()** та
[fstat()](function.fstat.md)**

\* У Windows це завжди буде `0`.

\*\* Доступний тільки для систем, що підтримують тип st_blksize - інші
системи (наприклад, Windows) повернуть `-1`.

\*\*\* У Windows, починаючи з PHP 7.4.0, це серійний номер тома,
містить файл, який являє собою 64-розрядне ціле число
*без знака*, тому може переповнитися у 32-розрядних системах. Раніше
це було числове представлення літери диска (наприклад, `2` для `C:`) для
**stat()** і `0` для [lstat()](function.lstat.md).

\*\*\*\* У Windows, починаючи з PHP 7.4.0, ідентифікатор, пов'язаний з
файлом, який є 64-розрядним цілим числом *без знака*,
може переповнитися у 32-розрядних системах. Раніше він завжди був '0'.

\*\*\*\*\* У Windows біт дозволу на запис встановлюється в
відповідно до атрибуту файлу тільки для читання, одне й те саме значення
повідомляється для всіх користувачів, групи та власника. ACL не
враховується, на відміну [is_writable()](function.is-writable.md).

Значення `mode` містить інформацію, яку читають кілька функцій. При
записи у вісімковому вигляді, починаючи праворуч, перші три цифри
повертаються функцією [chmod()](function.chmod.md). Наступна цифра
ігнорується PHP. Наступні дві цифри вказують тип файлу:

| mode у вісімковому вигляді | Значення             |
|----------------------------|----------------------|
| **0140000**                | сокет                |
| **0120000**                | символічне посилання |
| **0100000**                | Традиційний файл     |
| **0060000**                | блоковий пристрій    |
| **0040000**                | директорія           |
| **0020000**                | символьний пристрій  |
| **0010000**                | FIFO                 |

**`mode` типів файлів**

Так, наприклад, звичайний файл може бути **`0100644`**, а директорія може бути
бути **`0040755`**.

У разі виникнення помилки **stat()** повертає **`false`**.

> **Примітка**: Так як тип integer в PHP є цілим числом
> знаком, і багато платформ використовують 32-х бітні цілі числа, то
> деякі функції файлових систем можуть повертати несподівані
> результати файлів розміром більше 2 Гб.

### Помилки

У разі виникнення помилки буде згенеровано помилку рівня
**`E_WARNING`**.

### Список змін

| Версія | Опис                                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.4.0  | У Windows номер пристрою тепер є серійним номером тома, що містить файл та номер inode - це ідентифікатор, пов'язаний із файлом.                                  |
| 7.4.0  | Статистика символьних посилань size, atime, mtime та ctime завжди відповідає статистиці цільового об'єкта. Це було раніше не притаманно NTS-складання на Windows. |

### Приклади

**Приклад #1 Приклад використання **stat()****

` <?php/* Отримуємо статистику файлу */$stat = stat('C:\php\php.exe');/* * Виводимо останнє час доступу к файлу, це і         */echo 'Остання час доступу: ' . $stat['atime'];/* * Виводимо час зміни файла, це то ж саме, і * виклик filemtime() */echo 'Час зміни: ' . $stat['mtime'];/*Виводимо номер пристрою */echo 'Номер пристрою: ' . $stat['dev'];?> `

**Приклад #2 Використання інформації з **stat()** разом з
[touch()](function.touch.md)**

` <?php/* Отримуємо статистику файлу */$stat = stat('C:\php\php.exe');/* Вдалося отримати цю статистику? */if (!$stat) {   echo 'виклик stat() не удався...';} else {     /*    * Ми хотімо збільшити востаннє         */   $atime==$stat['atime'] + 604800; /* Торкаємося файла */    if (!touch('some_file.txt', time(), $atime)) {       echo 'Не удалося торкнутися файла'; } else {        echo 'touch() виконався успішно...'; }}?> `

### Примітки

> **Примітка**:
>
> Врахуйте, що обробка часу може відрізнятися в різних файлових
> системах.

> **Примітка**: Результати цієї функції кешуються. Детальніше
> інформацію дивіться у розділі
> [clearstatcache()](function.clearstatcache.md).

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з
* Деякими * обгортками url. Список обгорток, що підтримуються сімейством
функцій **stat()**, дивіться розділ [Підтримувані протоколи та обертки](wrappers.md).

### Дивіться також

- [lstat()](function.lstat.md) - Повертає інформацію про файл або
символічне посилання
- [fstat()](function.fstat.md) - Отримує інформацію про файл,
використовуючи відкритий файловий покажчик
- [filemtime()](function.filemtime.md) - Повертає час останнього
зміни файлу
- [filegroup()](function.filegroup.md) - Отримує ідентифікатор
групи файлу
- [SplFileInfo](class.splfileinfo.md)
