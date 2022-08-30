Встановлює файл для профілювання

-   [« XSLTProcessor::setParameter](xsltprocessor.setparameter.md)
    
-   [XSLTProcessor::setSecurityPrefs »](xsltprocessor.setsecurityprefs.md)
    
-   [PHP Manual](index.md)
    
-   [XSLTProcessor](class.xsltprocessor.md)
    
-   Встановлює файл для профілювання
    

# XSLTProcessor::setProfiling

(PHP >= 5.3.0, PHP 7, PHP 8)

XSLTProcessor::setProfiling — Встановлює файл для профілювання

### Опис

```methodsynopsis
public XSLTProcessor::setProfiling(?string $filename): bool
```

Встановлює файл для запису профілюючої інформації під час обробки таблиць стилів.

### Список параметрів

`filename`

Шлях до файлу, який записується профілююча інформація.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад виведення профілюючої інформації**

```php
<?php
// Загрузка исходного XML
$xml = new DOMDocument;
$xml->load('collection.xml');

$xsl = new DOMDocument;
$xsl->load('collection.xsl');

// Настройка преобразования
$proc = new XSLTProcessor;
$proc->setProfiling('profiling.txt');
$proc->importStyleSheet($xsl); // добавление стилей xsl

echo trim($proc->transformToDoc($xml)->firstChild->wholeText);
?>
```

Вищенаведений код записує наступну інформацію у файл профілювання:

```
number               match                name      mode  Calls Tot 100us Avg

    0                   cd                                    2      3      1
    1           collection                                    1      1      1

                         Total                                3      4
```