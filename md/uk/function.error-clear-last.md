- [«debug_print_backtrace](function.debug-print-backtrace.md)
- [error_get_last »](function.error-get-last.md)

- [PHP Manual](index.md)
- [Функції обробки помилок](ref.errorfunc.md)
- Очистити останню помилку

#error_clear_last

(PHP 7, PHP 8)

error_clear_last — Очистити останню помилку

### Опис

**error_clear_last**(): void

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Очищає останню помилку, унеможливлюючи отримання її за допомогою
[error_get_last()](function.error-get-last.md).

### Приклади

**Приклад #1 Приклад **error_clear_last()****

` <?phpvar_dump(error_get_last());error_clear_last();var_dump(error_get_last());@$a = $b;var_dump(error_get_last());error_clear_last();var_dump(error_get_last());?>

Результатом виконання цього прикладу буде щось подібне:

NULL
NULL
array(4) {
["type"]=>
int(8)
["message"]=>
string(21) "Undefined variable: b"
["file"]=>
string(9) "%s"
["line"]=>
int(6)
}
NULL

### Дивіться також

- [Константи помилок](errorfunc.constants.md)
