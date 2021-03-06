- [«gnupg_import](function.gnupg-import.md)
- [gnupg_keyinfo »](function.gnupg-keyinfo.md)

- [PHP Manual](index.md)
- [GnuPG Функції](ref.gnupg.md)
- Ініціалізувати GnuPG

#gnupg_init

(PECL gnupg \>= 0.4)

gnupg_init - Ініціалізувати GnuPG

### Опис

**gnupg_init**(?array `$options` = **`null`**): resource

### Список параметрів

`options`
Параметр приймає асоціативний масив. Він використовується для зміни
зміни криптографічного механізму за промовчанням.

| Ключ      | Тип    | Опис                                                                                                                 |
| --------- | ------ | -------------------------------------------------------------------------------------------------------------------- |
| file_name | string | Ім'я файлу програми, що реалізує протокол, який зазвичай є шляхом до виконуваного файлу gpg.                         |
| home_dir  | string | Ім'я каталогу конфігурації. Воно також перевизначає змінну оточення GNUPGHOME, яка використовується для тієї ж мети. |

**Перевизначення конфігурації**

### Значення, що повертаються

Повертає ресурс (resource) GnuPG, який використовується іншими
функціями GnuPG.

### Список змін

| Версія | Опис                      |
| ------ | ------------------------- |
| 1.5.0  | Доданий параметр options. |

### Приклади

**Приклад #1 Приклад використання **gnupg_init()** у процедурному стилі з
налаштуваннями за замовчуванням**

` <?php$res = gnupg_init();?> `

**Приклад #2 Приклад використання **gnupg_init()** у процедурному стилі з
перевизначеним ім'ям файлу та домашнім каталогом**

` <?php$res = gnupg_init(["file_name" => "/usr/bin/gpg2", "home_dir" => "/var/www/.gnupg"]);?> `

**Приклад #3 Приклад використання ініціалізатора gnupg в
об'єктно-орієнтованому стилі з параметрами за замовчуванням**

` <?php$gpg = new gnupg();?> `

**Приклад #4 Приклад використання в об'єктно-орієнтованому стилі з
перевизначеним ім'ям файлу та домашнім каталогом**

` <?php$gpg = new gnupg(["file_name" => "/usr/bin/gpg2", "home_dir" => "/var/www/.gnupg"]);?> `
