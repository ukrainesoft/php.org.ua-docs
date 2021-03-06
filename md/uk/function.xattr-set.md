- [«xattr_remove](function.xattr-remove.md)
- [xattr_supported »](function.xattr-supported.md)

- [PHP Manual](index.md)
- [xattr Функції](ref.xattr.md)
- Встановлення розширених атрибутів файлу

#xattr_set

(PECL xattr \>= 0.9.0)

xattr_set — Встановлення розширених атрибутів файлу

### Опис

**xattr_set**(
string `$filename`,
string `$name`,
string `$value`,
int `$flags` = 0
): bool

Ця функція визначає розширений атрибут файлу.

Розширені атрибути мають два різні простори імен:
користувальницьке та кореневе (root). Користувальницький простір імен
доступно для всіх користувачів, в той час як кореневе - тільки для
користувачів з root-привілеями. За замовчуванням xattr оперує в
користувальницькому просторі імен, але ви можете змінити цю поведінку
за допомогою аргументу `flags`.

### Список параметрів

`filename`
Назва файлу, атрибут якого потрібно встановити.

`name`
Назва розширеного атрибута. За його відсутності атрибут створюється,
в іншому випадку - перезаписується. Ви можете змінити поведінку,
використовуючи прапори (flags).

`value`
Значення атрибуту.

`flags`
|                      |                                                                                 |
|----------------------|---------------------------------------------------------------------------------|
| **XATTR_CREATE**     | Функція поверне помилку, якщо існує атрибут.                                    |
| **XATTR_REPLACE**    | Функція поверне помилку, якщо атрибут не існує.                                 |
| **XATTR_DONTFOLLOW** | Чи не розіменовувати символічні посилання, працювати з самим посиланням.        |
| **XATTR_ROOT**       | Встановити атрибут у кореневому просторі назв. Потрібні права суперкористувача. |

**Підтримувані xattr-прапори**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Встановити розширені атрибути `.wav` файлу**

` <?php$file = 'my_favourite_song.wav';xattr_set($file, 'Artist', 'Someone');xattr_set($file, 'My ranking', 'Good');xattr_set($file, 'Listen ', '34');/* ... other code ... */printf("You've played this song %d times", xattr_get($file, 'Listen count'));?> `

### Дивіться також

- [xattr_get()](function.xattr-get.md) - Отримання розширених
атрибутів файлу
- [xattr_remove()](function.xattr-remove.md) - Видалення розширених
атрибутів файлу
