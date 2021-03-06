- [«hash_hmac_file](function.hash-hmac-file.md)
- [hash_init »](function.hash-init.md)

- [PHP Manual](index.md)
- [Функції Hash](ref.hash.md)
- Генерація хеш-коду на основі ключа, використовуючи метод HMAC

# hash_hmac

(PHP 5 = 5.1.2, PHP 7, PHP 8, PECL hash = 1.1)

hash_hmac — Генерація хеш-коду на основі ключа, використовуючи метод HMAC

### Опис

**hash_hmac**(
string `$algo`,
string `$data`,
string `$key`,
bool `$binary` = **`false`**
): string

### Список параметрів

`algo`
Ім'я вибраного алгоритму хешування (наприклад, "md5", "sha256",
"haval160,4" і т.д.) Дивіться
[hash_hmac_algos()](function.hash-hmac-algos.md) для отримання списку
алгоритмів, що підтримуються.

`data`
Повідомлення для хешування.

`key`
Загальний секретний ключ, який використовується для генерації HMAC хеш-коду.

`binary`
Коли встановлено в **`true`**, виводить необроблені двійкові дані.
При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому
регістрі.

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому
кодування у нижньому регістрі. Якщо `binary` заданий як **`true`**, то
повертається хеш-код як бінарних даних.

### Список змін

| Версія | Опис                                                                                                                                                                       |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | Функція [hash()](function.hash.md) тепер викидає виняток [ValueError](class.valueerror.md), якщо алгоритм algo невідомий; раніше натомість поверталося значення **false**. |
| 7.2.0  | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat).                                                   |

### Приклади

**Приклад #1 Приклад використання **hash_hmac()****

`<?phpecho hash_hmac('ripemd160', 'Нахабний коричневий лисенок стрибає навколо ледачої собаки.', 'secret');?> `

Результат виконання цього прикладу:

b95d4abec7c27ec87fb54da1621f9942948879e4

### Дивіться також

- [hash()](function.hash.md) - Генерує хеш-код (підпис
повідомлення)
- [hash_hmac_algos()](function.hash-hmac-algos.md) - Повертає
список зареєстрованих алгоритмів хешування, які застосовуються для
hash_hmac
- [hash_init()](function.hash-init.md) - Ініціалізація
інкрементального контексту хешування
- [hash_hmac_file()](function.hash-hmac-file.md) - Генерація
хеш-коду на основі ключа, використовуючи метод HMAC та вміст
отриманого файлу
