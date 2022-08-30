Знайти простір імен для префікса

-   [« XMLReader::isValid](xmlreader.isvalid.md)
    
-   [XMLReader::moveToAttribute »](xmlreader.movetoattribute.md)
    
-   [PHP Manual](index.md)
    
-   [XMLReader](class.xmlreader.md)
    
-   Знайти простір імен для префікса
    

# XMLReader::lookupNamespace

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::lookupNamespace — Знайти простір імен для префікса

### Опис

```methodsynopsis
public XMLReader::lookupNamespace(string $prefix): ?string
```

Пошук у контексті простору імен для цього префікса.

### Список параметрів

`prefix`

Рядок, що містить префікс.

### Значення, що повертаються

Значення простору імен або \*\*`null`\*\*якщо простору імен не існує.

### список змін

| Версия | Описание                                     |
|--------|----------------------------------------------|
|        | Функція більше не може повертати **`false`** |