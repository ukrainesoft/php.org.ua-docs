Встановлює схему для значень, що повертаються

-   [« yazscan](function.yaz-scan.html)
    
-   [yazsearch »](function.yaz-search.html)
    
-   [PHP Manual](index.md)
    
-   [Функции YAZ](ref.yaz.md)
    
-   Встановлює схему для значень, що повертаються
    

# yazschema

(PHP 4> = 4.2.0, PECL yaz> = 0.9.0)

yazschema — Встановлює схему для значень, що повертаються.

### Опис

```methodsynopsis
yaz_schema(resource $id, string $schema): void
```

**yazschema()** встановлює схему для значень, що повертаються.

Функція має бути викликана до [yazsearch()](function.yaz-search.html) або [yazpresent()](function.yaz-present.html)

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

`schema`

Схема має бути визначена як OID (Object Identifier) ​​у вихідному поданні з роздільниками у вигляді точок (наприклад `1.2.840.10003.13.4`) або як одна з відомих форм імені схеми: `GILS-schema` `Holdings` `Zthes`

### Значення, що повертаються

Функція не повертає значення після виконання.