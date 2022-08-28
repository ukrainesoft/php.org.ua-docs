Повертає CRC елемент архіву

-   [« RarEntry::getAttr](rarentry.getattr.html)
    
-   [RarEntry::getFileTime »](rarentry.getfiletime.html)
    
-   [PHP Manual](index.html)
    
-   [RarEntry](class.rarentry.html)
    
-   Повертає CRC елемент архіву
    

# RarEntry::getCrc

(PECL rar >= 0.1)

RarEntry::getCrc — Повертає CRC елемент архіву

### Опис

```methodsynopsis
public RarEntry::getCrc(): string
```

Повертає шістнадцяткове рядкове представлення CRC елемента архіву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає CRC елемента архіву або **`false`** у разі виникнення помилки.

### список змін

| Версия         | Описание                                                         |
|----------------|------------------------------------------------------------------|
| PECL rar 2.0.0 | Тепер цей метод повертає коректні значення багатотомних архівів. |