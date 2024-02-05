---
navigation:
  - zookeeper.requirements.md: « Вимоги
  - zookeeper.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - zookeeper.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Цей модуль [» PECL](https://pecl.php.net/)не поставляется вместе с PHP.

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Встановлення PECL модулів](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/zookeeper](https://pecl.php.net/package/zookeeper)

Щоб увімкнути підтримку zookeeper, конфігуруйте PHP з опцією **\--with-libzookeeper-dir=DIR**DIR - директория в которой установлена библиотека ZooKeeper C Binding, внутри которой должен находиться include/zookeeper/zookeeper.h

DLL для цього модуля PECL поки що недоступна. Дивіться також розділ [збирання на Windows](install.windows.building.md)
