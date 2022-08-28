Обумовлені константи

-   [« Типы ресурсов](yaml.resources.html)
    
-   [Примеры »](yaml.examples.html)
    
-   [PHP Manual](index.html)
    
-   [Yaml](book.yaml.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**Скалярні стилі сутностей, які можна використовувати в callback-методах [yaml\_parse()](function.yaml-parse.html)**

**`YAML_ANY_SCALAR_STYLE`** (int)

**`YAML_PLAIN_SCALAR_STYLE`** (int)

**`YAML_SINGLE_QUOTED_SCALAR_STYLE`** (int)

**`YAML_DOUBLE_QUOTED_SCALAR_STYLE`** (int)

**`YAML_LITERAL_SCALAR_STYLE`** (int)

**`YAML_FOLDED_SCALAR_STYLE`** (int)

**Стандартні теги, які можна використовувати у callback-методах [yaml\_parse()](function.yaml-parse.html)**

**`YAML_NULL_TAG`** (string)

"tag:yaml.org,2002:null"

**`YAML_BOOL_TAG`** (string)

"tag:yaml.org,2002:bool"

**`YAML_STR_TAG`** (string)

"tag:yaml.org,2002:str"

**`YAML_INT_TAG`** (string)

"tag:yaml.org,2002:int"

**`YAML_FLOAT_TAG`** (string)

"tag:yaml.org,2002:float"

**`YAML_TIMESTAMP_TAG`** (string)

"tag:yaml.org,2002:timestamp"

**`YAML_SEQ_TAG`** (string)

"tag:yaml.org,2002:seq"

**`YAML_MAP_TAG`** (string)

"tag:yaml.org,2002:map"

**`YAML_PHP_TAG`** (string)

"!php/object"

**Типи кодувань для [yaml\_emit()](function.yaml-emit.html)**

**`YAML_ANY_ENCODING`** (int)

Дозволити джерелу вибрати кодування.

**`YAML_UTF8_ENCODING`** (int)

UTF8

**`YAML_UTF16LE_ENCODING`** (int)

UTF16LE

**`YAML_UTF16BE_ENCODING`** (int)

UTF16BE

**Типи кінця рядків для [yaml\_emit()](function.yaml-emit.html)**

**`YAML_ANY_BREAK`** (int)

Дозволити джерелу вибрати символ кінця рядка.

**`YAML_CR_BREAK`** (int)

Використати `\r` (Стиль Mac).

**`YAML_LN_BREAK`** (int)

Використати `\n` (Стиль Unix).

**`YAML_CRLN_BREAK`** (int)

Використати `\r\n` (Стиль DOS/Windows).