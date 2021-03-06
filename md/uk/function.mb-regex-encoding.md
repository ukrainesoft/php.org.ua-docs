- [«mb_preferred_mime_name](function.mb-preferred-mime-name.md)
- [mb_regex_set_options »](function.mb-regex-set-options.md)

- [PHP Manual](index.md)
- [Функції для роботи з багатобайтовими рядками](ref.mbstring.md)
- Встановлює/отримує поточне кодування для багатобайтового
регулярного вираження

#mb_regex_encoding

(PHP 4 \>= 4.2.0, PHP 5, PHP 7, PHP 8)

mb_regex_encoding — Встановлює/отримує поточне кодування для
багатобайтового регулярного вираження

### Опис

**mb_regex_encoding**(?string `$encoding` = **`null`**): string\|bool

Встановлює/отримує поточне кодування для багатобайтового регулярного
вирази.

### Список параметрів

`encoding`
Параметр 'encoding' є символьним кодуванням. Якщо він
опущений або дорівнює **`null`**, замість нього буде використано значення
внутрішнього кодування.

### Значення, що повертаються

Якщо заданий параметр `encoding`, то Повертає **`true`** у разі
успішного виконання або **`false`** у разі виникнення помилки. В
цьому випадку не змінюється внутрішнє багатобайтове кодування. Якщо
параметр `encoding` не вказано, то повертається поточне ім'я кодування
символів для багатобайтових регулярних виразів.

### Список змін

| Версія | Опис                                                     |
|--------|----------------------------------------------------------|
| 8.0.0  | Тепер параметр encoding може набувати значення **null**. |

### Дивіться також

- [mb_internal_encoding()](function.mb-internal-encoding.md) -
Встановлення/отримання внутрішнього кодування скрипту
- [mb_ereg()](function.mb-ereg.md) - Збіг з регулярним
виразом з підтримкою багатобайтових кодувань
