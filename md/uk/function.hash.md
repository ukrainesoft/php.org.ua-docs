- [«hash_update](function.hash-update.md)
- [Mcrypt »](book.mcrypt.md)

- [PHP Manual](index.md)
- [Функції Hash](ref.hash.md)
- Генерує хеш-код (підпис повідомлення)

# hash

(PHP 5 = 5.1.2, PHP 7, PHP 8, PECL hash = 1.1)

hash — Генерує хеш-код (підпис повідомлення)

### Опис

**hash**(
string `$algo`,
string `$data`,
bool `$binary` = **`false`**,
array `$options` = []
): string

### Список параметрів

`algo`
Ім'я вибраного алгоритму хешування (наприклад, "md5", "sha256",
"haval160,4" і т.д.). Список підтримуваних алгоритмів дивіться
[hash_algos()](function.hash-algos.md).

`data`
Повідомлення для хешування.

`binary`
Коли встановлено в **`true`**, виводить необроблені двійкові дані.
При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому
регістрі.

`options`
Багато опцій для різних алгоритмів хешування. В даний час
у варіантах MurmurHash підтримується лише параметр "seed".

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому
кодування у нижньому регістрі. Якщо `binary` заданий як **`true`**, то
повертається хеш-код як бінарних даних.

### Список змін

| Версія | Опис                                                                                                                                                       |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.1.0  | Доданий параметр options.                                                                                                                                  |
| 8.0.0  | Функція **hash()** тепер викидає виняток [ValueError](class.valueerror.md), якщо алгоритм algo невідомий; раніше натомість поверталося значення **false**. |

### Приклади

**Приклад #1 Приклад використання **hash()****

`<?phpecho hash('ripemd160', 'Нахабний коричневий лисенок стрибає навколо ледачої собаки.');?> `

Результат виконання цього прикладу:

8817ca339f7f902ad3fb456150a1bb9b4cb5dde9

### Дивіться також

- [hash_file()](function.hash-file.md) - Генерація хеш-значення,
використовуючи вміст заданого файлу
- [hash_hmac()](function.hash-hmac.md) - Генерація хеш-коду на
основі ключа, використовуючи метод HMAC
- [hash_init()](function.hash-init.md) - Ініціалізація
інкрементального контексту хешування
- [md5()](function.md5.md) - Повертає MD5-хеш рядки
- [sha1()](function.sha1.md) - Повертає SHA1-хеш рядки
