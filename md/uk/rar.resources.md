Типи ресурсів

-   [« Настройка во время выполнения](rar.configuration.html)
    
-   [Предопределённые константы »](rar.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](rar.setup.html)
    
-   Типи ресурсів
    

## Типи ресурсів

Цей модуль використовує три внутрішні ресурси: дескриптор файлу, що повертається функцією [rar\_open()](rararchive.open.html) [RarArchive](class.rararchive.html), вміст архіву, що повертається функціями [rar\_list()](rararchive.getentries.html) і [rar\_entry\_get()](rararchive.getentry.html) [RarEntry](class.rarentry.html) та тип винятків [RarException](class.rarexception.html)

Цей модуль також реєструє потоковий ресурс, званий "rar", і обгортку URL, яка називається "rar wrapper", і відповідний їй префікс "rar".