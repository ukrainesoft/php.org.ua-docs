- [«mcrypt_get_key_size](function.mcrypt-get-key-size.md)
- [mcrypt_list_modes »](function.mcrypt-list-modes.md)

- [PHP Manual](index.md)
- [Mcrypt](ref.mcrypt.md)
- Отримати список усіх підтримуваних алгоритмів шифрування

# mcrypt_list_algorithms

(PHP 4 \>= 4.0.2, PHP 5, PHP 7 \< 7.2.0, PECL mcrypt \>= 1.0.0)

mcrypt_list_algorithms — Отримати список усіх підтримуваних алгоритмів
шифрування

**Увага**

Ця функція оголошена *УСТАРНІЙ*, починаючи з PHP 7.1.0 і була *Видалена*
у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

**mcrypt_list_algorithms**(string `$lib_dir` =
ini_get("mcrypt.algorithms_dir")): array

Отримати список всіх підтримуваних алгоритмів шифрування в заданій
директорії `lib_dir`.

### Список параметрів

`lib_dir`
Вказує директорію, де розташовані алгоритми. Якщо не поставлено,
то буде використано значення директиви `mcrypt.algorithms_dir` з
`php.ini`.

### Значення, що повертаються

Повертає масив алгоритмів, що підтримуються.

### Приклади

**Приклад #1 Приклад використання **mcrypt_list_algorithms()****

` <?php$algorithms = mcrypt_list_algorithms();print_r($algorithms);?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => cast-128
[1] => gost
[2] => rijndael-128
[3] => twofish
[4] => arcfour
[5] => cast-256
[6] => loki97
[7] => rijndael-192
[8] => saferplus
[9] => wake
[10] => blowfish-compat
[11] => des
[12] => rijndael-256
[13] => serpent
[14] => xtea
[15] => blowfish
[16] => enigma
[17] => rc2
[18] => tripledes
)
