---
navigation:
  - refs.basic.php.md: « Зміна поведінки PHP
  - intro.apcu.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.php.md: Зміна поведінки PHP
title: Кеш користувача APC
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Кеш користувача APC

-   [Вступ](intro.apcu.md)
-   [Встановлення та налаштування](apcu.setup.md)
    -   [Вимоги](apcu.requirements.md)
    -   [Установка](apcu.installation.md)
    -   [Налаштування під час виконання](apcu.configuration.md)
    -   [Типи ресурсів](apcu.resources.md)
-   [Обумовлені константи](apcu.constants.md)
-   [Функції APCu](ref.apcu.md)
    -   [apcu\_add](function.apcu-add.md) \- Додати змінну в кеш
    -   [apcu\_cache\_info](function.apcu-cache-info.md)— Витягує закешовану інформацію зі сховища APCu
    -   [apcu\_cas](function.apcu-cas.md)— Замінює старе значення на нове
    -   [apcu\_clear\_cache](function.apcu-clear-cache.md)— Очистити кеш APCu
    -   [apcu\_dec](function.apcu-dec.md)— Зменшити збережене число
    -   [apcu\_delete](function.apcu-delete.md)— Видаляє збережене значення з кешу
    -   [apcu\_enabled](function.apcu-enabled.md)— Чи можливо використовувати APCu у поточному оточенні
    -   [apcu\_entry](function.apcu-entry.md)— Автоматичне вилучення або створення запису в кеші
    -   [apcu\_exists](function.apcu-exists.md)— Перевіряє, чи є записи
    -   [apcu\_fetch](function.apcu-fetch.md) \- Витягує з кеша збережену змінну
    -   [apcu\_inc](function.apcu-inc.md)— Збільшити збережене число
    -   [apcu\_key\_info](function.apcu-key-info.md)— Отримати детальну інформацію про ключ у кеші
    -   [apcu\_sma\_info](function.apcu-sma-info.md)— Витягує інформацію про виділення пам'яті APCu, що розділяється.
    -   [apcu\_store](function.apcu-store.md) \- Кешує змінну
-   [APCUIterator](class.apcuiterator.md) \- Клас APCUIterator
    -   [APCUIterator::\_\_construct](apcuiterator.construct.md)— Створює об'єкт ітератора класу APCUIterator
    -   [APCUIterator::current](apcuiterator.current.md)— Отримати поточний елемент
    -   [APCUIterator::getTotalCount](apcuiterator.gettotalcount.md)— Отримати загальну кількість записів
    -   [APCUIterator::getTotalHits](apcuiterator.gettotalhits.md)— Отримати загальну кількість влучень у кеш
    -   [APCUIterator::getTotalSize](apcuiterator.gettotalsize.md) \- Загальний розмір кешу
    -   [APCUIterator::key](apcuiterator.key.md) \- Отримати ключ ітератора
    -   [APCUIterator::next](apcuiterator.next.md)— Переміщує курсор на наступний елемент
    -   [APCUIterator::rewind](apcuiterator.rewind.md) \- Перемотування ітератора
    -   [APCUIterator::valid](apcuiterator.valid.md)— Перевіряє, чи поточна позиція ітератора коректна.
