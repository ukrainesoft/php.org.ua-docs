- [«runkit7_superglobals](function.runkit7-superglobals.md)
- [uopz »](book.uopz.md)

- [PHP Manual](index.md)
- [Функції runkit7](ref.runkit7.md)
- Повертає інформацію про передане значення з типами даних,
кількістю посилань і так далі

# runkit7_zval_inspect

(PECL runkit7 \>= Unknown)

runkit7_zval_inspect — Повертає інформацію про передане значення з
типами даних, кількістю посилань і так далі

### Опис

**runkit7_zval_inspect**(string `$value`): array

### Список параметрів

`value`
Значення, щоб повернути уявлення.

### Значення, що повертаються

Масив, що повертається цією функцією, містить такі елементи:

- `address`
- `refcount` (необов'язковий)
- `is_ref` (необов'язковий)
- `type`

### Приклади

**Приклад #1 Приклад використання **runkit7_zval_inspect()****

` <?php$var = new DateTime();var_dump(runkit7_zval_inspect($var));$var = 1;var_dump(runkit7_zval_inspect($var));?> `

Результат виконання цього прикладу:

array(4) {
["address"]=>
string(14) "0x7f45ab21b1e0"
["refcount"]=>
int(2)
["is_ref"]=>
bool(false)
["type"]=>
int(8)
}

array(2) {
["address"]=>
string(14) "0x7f45ab21b1e0"
["type"]=>
int(4)
}

### Дивіться також

- [Пояснення посилань](language.references.md)
- [» Пояснення посилань (Дерік)
Ретанс)](http://derickrethans.nl/php_references_article.php)
