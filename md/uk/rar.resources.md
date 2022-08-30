Типи ресурсів

-   [« Налаштування під час виконання](rar.configuration.md)
    
-   [Обумовлені константи »](rar.constants.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](rar.setup.md)
    
-   Типи ресурсів
    

## Типи ресурсів

Цей модуль використовує три внутрішні ресурси: дескриптор файлу, що повертається функцією [raropen()](rararchive.open.md) [RarArchive](class.rararchive.md), вміст архіву, що повертається функціями [rarlist()](rararchive.getentries.md) і [rarentryget()](rararchive.getentry.md) [RarEntry](class.rarentry.md) та тип винятків [RarException](class.rarexception.md)

Цей модуль також реєструє потоковий ресурс, званий "rar", і обгортку URL, яка називається "rar wrapper", і відповідний їй префікс "rar".