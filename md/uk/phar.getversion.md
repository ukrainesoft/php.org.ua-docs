Отримати версію Phar-архіву

-   [« Phar::getSupportedSignatures](phar.getsupportedsignatures.html)
    
-   [Phar::hasMetadata »](phar.hasmetadata.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Отримати версію Phar-архіву
    

# Phar::getVersion

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::getVersion — Отримати версію Phar-архіву

### Опис

```methodsynopsis
public Phar::getVersion(): string
```

Повертає версію API відкритого Phar-архіву.

### Список параметрів

### Значення, що повертаються

Версія API відкритого архіву. Не переплутайте версію API завантаженого модуля phar. Кожен Phar-архів має жорстко прописану версію API, за допомогою якого його створювали у маніфесті. Детальну документацію можна прочитати на сторінці [Формат файла Phar](phar.fileformat.html)

### Дивіться також

-   [Phar::apiVersion()](phar.apiversion.html) - Повертає версію API