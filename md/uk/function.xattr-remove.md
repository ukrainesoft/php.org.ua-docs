- [«xattr_list](function.xattr-list.md)
- [xattr_set »](function.xattr-set.md)

- [PHP Manual](index.md)
- [xattr Функції](ref.xattr.md)
- Видалення розширених атрибутів файлу

#xattr_remove

(PECL xattr \>= 0.9.0)

xattr_remove — Видалення розширених атрибутів файлу

### Опис

**xattr_remove**(string `$filename`, string `$name`, int `$flags` = 0):
bool

Ця функція видаляє розширений атрибут файлу.

Розширені атрибути мають два різні простори імен:
користувальницьке та кореневе (root). Користувальницький простір імен
доступно для всіх користувачів, в той час як кореневе - тільки для
користувачів з root-привілеями. За замовчуванням xattr оперує в
користувальницькому просторі імен, але ви можете змінити цю поведінку
за допомогою аргументу `flags`.

### Список параметрів

`filename`
Файл, атрибут якого потрібно видалити.

`name`
Ім'я атрибута, що видаляється.

`flags`
|                      |                                                                                 |
|----------------------|---------------------------------------------------------------------------------|
| **XATTR_DONTFOLLOW** | Чи не розіменовувати символічні посилання, працювати з самим посиланням.        |
| **XATTR_ROOT**       | Встановити атрибут у кореневому просторі назв. Потрібні права суперкористувача. |

**Підтримувані xattr-прапори**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Видалити всі розширені атрибути файлу**

` <?php$file = 'some_file';$attributes = xattr_list($file);foreach ($attributes as $attr_name) {    xattr_remove($file, $attr_name);}?> `

### Дивіться також

- [xattr_list()](function.xattr-list.md) - Перегляд списку
розширених атрибутів файлу
- [xattr_set()](function.xattr-set.md) - Установка розширених
атрибутів файлу
- [xattr_get()](function.xattr-get.md) - Отримання розширених
атрибутів файлу
