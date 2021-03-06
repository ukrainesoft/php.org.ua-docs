- [« Функції для роботи з каталогами](ref.dir.md)
- [chroot »](function.chroot.md)

- [PHP Manual](index.md)
- [Функції для роботи з каталогами](ref.dir.md)
- Змінює каталог

#chdir

(PHP 4, PHP 5, PHP 7, PHP 8)

chdir — Змінює каталог

### Опис

**chdir**(string `$directory`): bool

Змінює поточний каталог PHP на вказаний як параметр
`directory`.

### Список параметрів

`directory`
Новий поточний каталог

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Помилки

У разі невдалого виконання видає помилку рівня **`E_WARNING`**.

### Приклади

**Приклад #1 Приклад використання **chdir()****

`<?php// поточний каталогecho getcwd() . "
";chdir('public_html');// поточний каталогecho getcwd() . "
";?> `

Результатом виконання цього прикладу буде щось подібне:

/home/vincent
/home/vincent/public_html

### Примітки

**Застереження**

Якщо PHP-інтерпретатор зібраний за допомогою ZTS (Zend Thread Safety),
будь-які зміни в поточному каталозі, зроблені за допомогою **chdir()**, не
будуть виявлені операційною системою. Усі вбудовані функції PHP будуть
як і раніше враховувати зміни у поточному каталозі; це не відноситься до
викликаним функціям зовнішніх бібліотек, підключених через
[FFI](book.ffi.md). Використовуйте **php -i** або вбудовану константу
**`PHP_ZTS`**, щоб дізнатися, чи зібрано PHP з ZTS.

### Дивіться також

- [getcwd()](function.getcwd.md) - Отримує ім'я поточного робітника
каталогу
