Повертає значення параметра

-   [« XSLTProcessor::\_\_construct](xsltprocessor.construct.html)
    
-   [XSLTProcessor::getSecurityPrefs »](xsltprocessor.getsecurityprefs.html)
    
-   [PHP Manual](index.html)
    
-   [XSLTProcessor](class.xsltprocessor.html)
    
-   Повертає значення параметра
    

# XSLTProcessor::getParameter

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::getParameter — Повертає значення параметра

### Опис

```methodsynopsis
public XSLTProcessor::getParameter(string $namespace, string $name): string|false
```

Повертає параметр, якщо його раніше встановлено за допомогою [XSLTProcessor::setParameter()](xsltprocessor.setparameter.html)

### Список параметрів

`namespace`

Простір імен URI для параметра XSLT.

`name`

Місцеве ім'я параметра XSLT.

### Значення, що повертаються

Значення параметра (у вигляді рядка), або **`false`**якщо воно не встановлено.

### Дивіться також

-   [XSLTProcessor::setParameter()](xsltprocessor.setparameter.html) - Встановлює значення параметра
-   [XSLTProcessor::removeParameter()](xsltprocessor.removeparameter.html) - Видаляє параметр