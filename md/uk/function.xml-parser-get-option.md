Отримання значення налаштування XML-аналізатора

-   [« xml\_parser\_free](function.xml-parser-free.html)
    
-   [xml\_parser\_set\_option »](function.xml-parser-set-option.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Отримання значення налаштування XML-аналізатора
    

# xmlparsergetoption

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparsergetoption — Отримання значення налаштування XML-аналізатора

### Опис

```methodsynopsis
xml_parser_get_option(XMLParser $parser, int $option): string|int
```

Отримує значення налаштування XML-аналізатора.

### Список параметрів

`parser`

Посилання на XML-аналізатор, налаштування якого потрібно отримати.

`option`

Яке налаштування отримати. Доступні такі параметри **`XML_OPTION_CASE_FOLDING`** **`XML_OPTION_SKIP_TAGSTART`** **`XML_OPTION_SKIP_WHITE`** і **`XML_OPTION_TARGET_ENCODING`**. Їх опис дивіться у документації до функції [xml\_parser\_set\_option()](function.xml-parser-set-option.html)

### Значення, що повертаються

Ця функція повертає **`false`**, якщо `parser` посилається на неприпустимий аналізатор або якщо `option` має неприпустиме значення (у цьому випадку викидається попередження **`E_WARNING`**). В інших випадках повертається значення налаштування.

### список змін

| Версия | Описание                                                                                                    |
|--------|-------------------------------------------------------------------------------------------------------------|
|        | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікували ресурс (resource). |
|        | Тепер параметр `options` підтримує **`XML_OPTION_SKIP_TAGSTART`** і **`XML_OPTION_SKIP_WHITE`**             |