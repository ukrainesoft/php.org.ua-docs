Відправляє YAML-подання значення файлу

-   [« Функции Yaml](ref.yaml.html)
    
-   [yamlemit »](function.yaml-emit.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Yaml](ref.yaml.html)
    
-   Відправляє YAML-подання значення файлу
    

# yamlemitfile

(PECL yaml >= 0.5.0)

yamlemitfile — Відправляє YAML-подання значення файлу

### Опис

```methodsynopsis
yaml_emit_file(    string $filename,    mixed $data,    int $encoding = YAML_ANY_ENCODING,    int $linebreak = YAML_ANY_BREAK,    array $callbacks = null): bool
```

Генерує YAML-подання з даних `data` і відправляє в `filename`

### Список параметрів

`filename`

Шлях до файлу.

`data`

Параметр `data` буде кодовано. Допускається будь-який тип даних, крім ресурсу (resource).

`encoding`

Кодування виводу вибирається з **`YAML_ANY_ENCODING`** **`YAML_UTF8_ENCODING`** **`YAML_UTF16LE_ENCODING`** **`YAML_UTF16BE_ENCODING`**

`linebreak`

Символ кінця рядка виведення вибирається з **`YAML_ANY_BREAK`** **`YAML_CR_BREAK`** **`YAML_LN_BREAK`** **`YAML_CRLN_BREAK`**

`callbacks`

Обробники контенту для створення вузлів YAML. Асоціативний масив (array), де як ключі використовуються імена класів, а як значення callback-функції ([callable](language.types.callable.html)), які створюватимуть вузли для цих класів. Більше подробиць можна дізнатись у розділі про [публікуючі callback-функції](yaml.callbacks.emit.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання.

### список змін

| Версия          | Описание                     |
|-----------------|------------------------------|
| PECL yaml 1.1.0 | Доданий аргумент `callbacks` |

### Дивіться також

-   [yamlemit()](function.yaml-emit.html) - Повертає YAML-подання значення
-   [yamlparse()](function.yaml-parse.html) - Розбирає потік YAML