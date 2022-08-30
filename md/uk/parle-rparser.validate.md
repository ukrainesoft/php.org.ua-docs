Перевіряє вхідні дані

-   [« ParleRParser::trace](parle-rparser.trace.html)
    
-   [ParleStack »](class.parle-stack.html)
    
-   [PHP Manual](index.md)
    
-   [ParleRParser](class.parle-rparser.html)
    
-   Перевіряє вхідні дані
    

# ParleRParser::validate

(PECL parle >= 0.7.0)

ParleRParser::validate — Перевіряє вхідні дані

### Опис

```methodsynopsis
public Parle\RParser::validate(string $data, Parle\RLexer $lexer): bool
```

Перевіряє вхідний рядок. Рядок аналізується внутрішнім механізмом, тому метод корисний швидкої перевірки вхідних даних.

### Список параметрів

`data`

Рядок для перевірки.

`lexer`

Об'єкт лексера містить правила лексування, підготовлені для конкретної граматики.

### Значення, що повертаються

Повертає логічне значення (bool) визначальне, чи вхідні дані відповідають заданим правилам чи ні.