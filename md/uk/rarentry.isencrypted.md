Перевіряє, чи зашифрований запис

-   [« RarEntry::isDirectory](rarentry.isdirectory.html)
    
-   [RarEntry::toString »](rarentry.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [RarEntry](class.rarentry.html)
    
-   Перевіряє, чи зашифрований запис
    

# RarEntry::isEncrypted

(PECL rar >= 2.0.0)

RarEntry::isEncrypted — Перевіряє, чи зашифрований запис

### Опис

```methodsynopsis
public RarEntry::isEncrypted(): bool
```

Перевіряє, чи зашифровано поточний запис.

> **Зауваження**
> 
> В тому самому архіві для різних файлів можуть використовуватися різні паролі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`** Залежно від результату.