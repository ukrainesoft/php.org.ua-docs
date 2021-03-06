- [«chgrp](function.chgrp.md)
- [chown »](function.chown.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Змінює режим доступу до файлу

# chmod

(PHP 4, PHP 5, PHP 7, PHP 8)

chmod — Змінює режим доступу до файлу

### Опис

**chmod**(string `$filename`, int `$permissions`): bool

Здійснює спробу зміни режиму доступу вказаного файлу на режим,
переданий у параметрі `permissions`.

### Список параметрів

`filename`
Шлях до файлу.

`permissions`
Зверніть увагу, що значення параметра `permissions` не перекладається
автоматично у вісімкову систему числення, тому, щоб
переконатися в тому, що режим було встановлено правильно, попереджайте
нулем (0) значення, що передається в параметрі `permissions`. Рядки, такі
як "g+w", не працюватимуть належним чином.

`<?phpchmod("/somedir/somefile", 755); // десяткове, швидше всього, зазначено невірноchmod("/somedir/somefile", "u+rwx,go+rx"); // рядок, невірний способchmod("/somedir/somefile", 0755); // восьмеричне, вірний способ?> `

Значення параметра `permissions` складається з трьох вісімкових чисел,
визначальних рівень доступу для власника файлу, для групи, в яку
входить власник, та інших користувачів, відповідно. Число,
визначальний рівень користувача може бути обчислено шляхом
підсумовування значень, що визначають права: 1 – доступ на виконання, 2 –
доступ на запис, 4 – доступ на читання. Складіть ці числа для вказівки
необхідного права доступу. Докладніше про систему прав у системах Unix ви
Ви можете дізнатися за допомогою команд '**man 1 chmod**' та '**man 2 chmod**'.

` <?php// Доступ на запис і читання для власника, немає доступу для іншихchmod("/somedir/somefile", 0600);// Доступ на запис і прочитання ", 0644);// Повний доступ для власника, доступ на читання і виконання для іншихchmod("/somedir/somefile", 0755);// Повний доступ для володіння somefile", 0750);?> `

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Помилки

У разі виникнення помилки видається помилка рівня **`E_WARNING`**.

### Примітки

> **Примітка**:
>
> Поточним користувачем є користувач, від імені якого
> виконується PHP. Можливо, що це буде не той користувач, під
> ім'ям якого ви отримуєте доступ до командної оболонки або облікової
> запис FTP. На більшості систем режим доступу до файлу може бути
> змінено лише його власником.

> **Примітка**: Ця функція не застосовується для роботи з [віддаленими > файлами](features.remote-files.md), оскільки файл має бути
> доступний через файлову систему сервера.

### Дивіться також

- [chown()](function.chown.md) - Змінює власника файлу
- [chgrp()](function.chgrp.md) - Змінює групу файлу
- [fileperms()](function.fileperms.md) - Повертає інформацію про
правах на файл
- [stat()](function.stat.md) - Повертає інформацію про файл
