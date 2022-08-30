Типи ресурсів

-   [« Настройка во время выполнения](rar.configuration.html)
    
-   [Предопределённые константы »](rar.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](rar.setup.html)
    
-   Типи ресурсів
    

## Типи ресурсів

Цей модуль використовує три внутрішні ресурси: дескриптор файлу, що повертається функцією [raropen()](rararchive.open.html) [RarArchive](class.rararchive.html), вміст архіву, що повертається функціями [rarlist()](rararchive.getentries.html) і [rarentryget()](rararchive.getentry.html) [RarEntry](class.rarentry.html) та тип винятків [RarException](class.rarexception.html)

Цей модуль також реєструє потоковий ресурс, званий "rar", і обгортку URL, яка називається "rar wrapper", і відповідний їй префікс "rar".