Встановлення

-   [« Вимоги](zookeeper.requirements.md)
    
-   [Налаштування під час виконання »](zookeeper.configuration.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](zookeeper.setup.md)
    
-   Встановлення
    

## Встановлення

Цей модуль [» PECL](https://pecl.php.net/) не постачається разом з PHP.

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/zookeeper](https://pecl.php.net/package/zookeeper)

Щоб увімкнути підтримку zookeeper, конфігуруйте PHP з опцією **\-with-libzookeeper-dir=DIR**. DIR - директорія в якій встановлена ​​бібліотека ZooKeeper C Binding, всередині якої має знаходитись include/zookeeper/zookeeper.h

DLL для цього модуля PECL зараз недоступна. Дивіться також розділ [сборка на Windows](install.windows.building.md)