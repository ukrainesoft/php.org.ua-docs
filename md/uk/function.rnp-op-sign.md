---
navigation:
  - function.rnp-op-sign-detached.md: « rnp\_op\_sign\_detached
  - function.rnp-op-verify-detached.md: rnp\_op\_verify\_detached »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_op\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_op\_sign

(PECL rnp >= 0.1.1)

rnp\_op\_sign — Виконує операцію підписання бінарних даних, повертає приєднаний підпис (підписи)

### Опис

```methodsynopsis
rnp_op_sign(    RnpFFI $ffi,    string $data,    array $keys_fp,    array $options = ?): string|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`data`

Дані для підпису.

`keys_fp`

Масив із цифровими відбитками ключів. Має бути зазначений хоча б один ключ. Ключі повинні бути присутніми у параметрі `ffi`

`options`

Асоціативний масив із опціями.

| Ключ | Тип данных | Опис |
| --- | --- | --- |
| `"compression_alg"` | string | Алгоритм стиснення. Для увімкнення стиснення даних повинні бути задані як `"compression_alg"`, так и`"compression_level"` |
| `"compression_level"` | integer | Рівень стиснення 0-9. 0 вимикає стиск. |
| `"armor"` | boolean | Включає ASCII-захищений висновок. За замовчуванням вимкнено. |
| `"hash"` | string | Встановлює хеш-алгоритм, який використовується під час обчислення підпису. |
| `"creation_time"` | integer | Встановлює час створення підпису в секундах з 1 січня 1970 року за Грінвічем. За промовчанням використовується поточний час. |
| `"expiration_time"` | integer | Встановлює час закінчення терміну дії підпису за секунди з моменту створення. Значення 0 використовується для позначки підпису як не закінчується (за замовчуванням). |
| `"file_name"` | string | Встановлює внутрішнє ім'я файлу для даних, що шифруються. Спеціальне значення \_CONSOLE може використовуватися для позначення повідомлення як "тільки для очей", тобто. воно не повинно ніде зберігатися, а лише відображатись одержувачу. За промовчанням використовується порожній рядок. |
| `"file_mtime"` | integer | Встановлює дату модифікації вхідного файлу в секундах з 1 січня 1970 по Гринвічу. |

### Значення, що повертаються

Повертає дані з приєднаним підписом (підписами) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.