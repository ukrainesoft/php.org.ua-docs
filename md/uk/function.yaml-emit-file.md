---
navigation:
  - ref.yaml.md: « Функції Yaml
  - function.yaml-emit.md: yaml\_emit »
  - index.md: PHP Manual
  - ref.yaml.md: Функції Yaml
title: yaml\_emit\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaml\_emit\_file

(PECL yaml >= 0.5.0)

yaml\_emit\_file — Відправляє YAML-подання значення файлу

### Опис

```methodsynopsis
yaml_emit_file(    string $filename,    mixed $data,    int $encoding = YAML_ANY_ENCODING,    int $linebreak = YAML_ANY_BREAK,    array $callbacks = null): bool
```

Генерує YAML-подання з даних `data` і відправляє в `filename`

### Список параметрів

`filename`

Шлях до файлу.

`data`

Параметр`data` буде кодовано. Допускається будь-який тип даних, крім ресурсу (resource).

`encoding`

Кодування виводу вибирається з **`YAML_ANY_ENCODING`** **`YAML_UTF8_ENCODING`** **`YAML_UTF16LE_ENCODING`** **`YAML_UTF16BE_ENCODING`**

`linebreak`

Символ кінця рядка виведення вибирається з **`YAML_ANY_BREAK`** **`YAML_CR_BREAK`** **`YAML_LN_BREAK`** **`YAML_CRLN_BREAK`**

`callbacks`

Обробники контенту для створення вузлів YAML. Асоціативний масив (array), де як ключі використовуються імена класів, а як значення callback-функції ([callable](language.types.callable.md)), які створюватимуть вузли для цих класів. Більше подробиць можна дізнатись у розділі про [публікуючі callback-функції](yaml.callbacks.emit.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання.

### список змін

| Версия | Опис |
| --- | --- |
| PECL yaml 1.1.0 | Доданий аргумент `callbacks` |

### Дивіться також

-   [yaml\_emit()](function.yaml-emit.md) \- Повертає YAML-подання значення
-   [yaml\_parse()](function.yaml-parse.md) \- Розбирає потік YAML
