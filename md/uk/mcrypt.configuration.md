Налаштування під час виконання

-   [« Установка](mcrypt.installation.html)
    
-   [Типы ресурсов »](mcrypt.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mcrypt.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Mcrypt**

| Имя                                                                         | По умолчанию | Место изменения | Список изменений |
|-----------------------------------------------------------------------------|--------------|-----------------|------------------|
| [mcrypt.algorithmsdir](mcrypt.configuration.html#ini.mcrypt.algorithms-dir) | **`null`**   | PHPINIALL       |                  |
| [mcrypt.modesdir](mcrypt.configuration.html#ini.mcrypt.modes-dir)           | **`null`**   | PHPINIALL       |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`mcrypt.algorithms_dir` string

Директорія, яка містить алгоритми. За замовчуванням відповідає директоріям, скомпільованим разом з libmcrypt, зазвичай */usr/local/lib/libmcrypt*. Дивіться [mcryptlistalgorithms()](function.mcrypt-list-algorithms.html) для додаткової інформації.

`mcrypt.modes_dir` string

Директорія з режимами. За замовчуванням відповідає директоріям, скомпільованим разом з libmcrypt, зазвичай */usr/local/lib/libmcrypt*. Дивіться [mcryptlistmodes()](function.mcrypt-list-modes.html) для додаткової інформації.