---
navigation:
  - class.pharexception.md: « PharException
  - intro.rar.md: Вступ "
  - index.md: PHP Manual
  - refs.compression.md: Модулі для стиснення та архівації
title: Архівування Rar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Архівування Rar

-   [Вступ](intro.rar.md)
-   [Встановлення та налаштування](rar.setup.md)
    -   [Вимоги](rar.requirements.md)
    -   [Установка](rar.installation.md)
    -   [Налаштування під час виконання](rar.configuration.md)
    -   [Типи ресурсів](rar.resources.md)
-   [Обумовлені константи](rar.constants.md)
-   [Приклади](rar.examples.md)
-   [Rar](ref.rar.md)
    -   [rar\_wrapper\_cache\_stats](function.rar-wrapper-cache-stats.md)— Кеш доступів та відмов обгортки URL
-   [RarArchive](class.rararchive.md) \- Клас RarArchive
    -   [RarArchive::close](rararchive.close.md)— Закриває RAR архів та звільняє всі ресурси
    -   [RarArchive::getComment](rararchive.getcomment.md)— Отримати текст коментаря з архіву RAR
    -   [RarArchive::getEntries](rararchive.getentries.md)— Повертає повний список елементів із RAR архіву
    -   [RarArchive::getEntry](rararchive.getentry.md)— Повертає об'єкт елемента з архіву RAR
    -   [RarArchive::isBroken](rararchive.isbroken.md)— Перевіряє, чи не зламано архів (не завершено)
    -   [RarArchive::isSolid](rararchive.issolid.md)— Перевірити, чи є архів суцільним
    -   [RarArchive::open](rararchive.open.md)— Відкриває архів RAR
    -   [RarArchive::setAllowBroken](rararchive.setallowbroken.md)— Чи відкривати пошкоджені архіви
    -   [RarArchive::\_\_function toString() { \[native code\] }](rararchive.tostring.md)— Отримати текстову виставу
-   [RarEntry](class.rarentry.md) \- Клас RarEntry
    -   [RarEntry::extract](rarentry.extract.md)— Витягує елемент із архіву
    -   [RarEntry::getAttr](rarentry.getattr.md)— Повертає атрибути елемента архіву
    -   [RarEntry::getCrc](rarentry.getcrc.md)— Повертає CRC елемент архіву
    -   [RarEntry::getFileTime](rarentry.getfiletime.md)— Останнім часом повертає зміни елемента
    -   [RarEntry::getHostOs](rarentry.gethostos.md)— Повертає оригінальну ОС елемента
    -   [RarEntry::getMethod](rarentry.getmethod.md)— Повертає метод компресії елемента
    -   [RarEntry::getName](rarentry.getname.md)— Повертає ім'я елемента
    -   [RarEntry::getPackedSize](rarentry.getpackedsize.md)— Повертає розмір стисненого елемента
    -   [RarEntry::getStream](rarentry.getstream.md)— Отримати обробник для запису
    -   [RarEntry::getUnpackedSize](rarentry.getunpackedsize.md)— Повертає розмір елемента у розпакованому стані
    -   [RarEntry::getVersion](rarentry.getversion.md)— Повертає мінімальну версію програми RAR, необхідну для розпакування елемента
    -   [RarEntry::isDirectory](rarentry.isdirectory.md)— Перевіряє, чи є запис директорією
    -   [RarEntry::isEncrypted](rarentry.isencrypted.md)— Перевіряє, чи зашифрований запис
    -   [RarEntry::\_\_function toString() { \[native code\] }](rarentry.tostring.md)— Отримати текстове подання запису
-   [RarException](class.rarexception.md) \- Клас RarException
    -   [RarException::isUsingExceptions](rarexception.isusingexceptions.md)— Перевірити, чи будуть функції повертати помилки або викидати винятки
    -   [RarException::setUsingExceptions](rarexception.setusingexceptions.md)— Увімкнути чи вимкнути генерацію винятків замість повернення помилок
