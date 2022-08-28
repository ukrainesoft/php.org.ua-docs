Встановлює ліміт для конкретного ресурсу

-   [« Imagick::setResolution](imagick.setresolution.html)
    
-   [Imagick::setSamplingFactors »](imagick.setsamplingfactors.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює ліміт для конкретного ресурсу
    

# Imagick::setResourceLimit

(PECL imagick 2, PECL imagick 3)

Imagick::setResourceLimit — Встановлює ліміт для конкретного ресурсу

### Опис

```methodsynopsis
public static Imagick::setResourceLimit(int $type, int $limit): bool
```

Цей метод використовується для зміни ліміту ресурсів вихідної бібліотеки ImageMagick.

### Список параметрів

`type`

Зверніться до списку [констант RESOURCETYPE](imagick.constants.html#imagick.constants.resourcetypes)

`limit`

Одна з [констант RESOURCETYPE](imagick.constants.html#imagick.constants.resourcetypes). Одиниця виміру залежить від типу ресурсу, що обмежується.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::getResourceLimit()](imagick.getresourcelimit.html) - Повертає заданий ліміт ресурсів