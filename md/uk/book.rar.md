Архівування Rar

-   [« PharException](class.pharexception.html)
    
-   [Введение »](intro.rar.html)
    
-   [PHP Manual](index.html)
    
-   [Модулі для стиснення та архівації](refs.compression.html)
    
-   Архівування Rar
    

# Архівування Rar

-   [Введение](intro.rar.html)
-   [Встановлення та налаштування](rar.setup.html)
    -   [Вимоги](rar.requirements.html)
    -   [Установка](rar.installation.html)
    -   [Налаштування під час виконання](rar.configuration.html)
    -   [Типи ресурсів](rar.resources.html)
-   [Обумовлені константи](rar.constants.html)
-   [Приклади](rar.examples.html)
-   [Rar](ref.rar.html)
    -   [rarwrappercachestats](function.rar-wrapper-cache-stats.html) — Кеш доступів та відмов обгортки URL
-   [RarArchive](class.rararchive.html) - Клас RarArchive
    -   [RarArchive::close](rararchive.close.html) — Закриває RAR архів та звільняє всі ресурси
    -   [RarArchive::getComment](rararchive.getcomment.html) — Отримати текст коментаря з архіву RAR
    -   [RarArchive::getEntries](rararchive.getentries.html) — Повертає повний список елементів із RAR архіву
    -   [RarArchive::getEntry](rararchive.getentry.html) — Повертає об'єкт елемента з архіву RAR
    -   [RarArchive::isBroken](rararchive.isbroken.html) — Перевіряє, чи не зламано архів (не завершено)
    -   [RarArchive::isSolid](rararchive.issolid.html) — Перевірити, чи є архів суцільним
    -   [RarArchive::open](rararchive.open.html) - Відкриває архів RAR
    -   [RarArchive::setAllowBroken](rararchive.setallowbroken.html) — Чи відкривати пошкоджені архіви
    -   [RarArchive::toString](rararchive.tostring.html) — Отримати текстову виставу
-   [RarEntry](class.rarentry.html) - Клас RarEntry
    -   [RarEntry::extract](rarentry.extract.html) — Витягує елемент із архіву
    -   [RarEntry::getAttr](rarentry.getattr.html) — Повертає атрибути елемента архіву
    -   [RarEntry::getCrc](rarentry.getcrc.html) — Повертає CRC елемент архіву
    -   [RarEntry::getFileTime](rarentry.getfiletime.html) — Останнім часом повертає зміни елемента
    -   [RarEntry::getHostOs](rarentry.gethostos.html) — Повертає оригінальну ОС елемента
    -   [RarEntry::getMethod](rarentry.getmethod.html) — Повертає метод компресії елемента
    -   [RarEntry::getName](rarentry.getname.html) — Повертає ім'я елемента
    -   [RarEntry::getPackedSize](rarentry.getpackedsize.html) — Повертає розмір стисненого елемента
    -   [RarEntry::getStream](rarentry.getstream.html) — Отримати обробник для запису
    -   [RarEntry::getUnpackedSize](rarentry.getunpackedsize.html) — Повертає розмір елемента у розпакованому стані
    -   [RarEntry::getVersion](rarentry.getversion.html) — Повертає мінімальну версію програми RAR, необхідну для розпакування елемента
    -   [RarEntry::isDirectory](rarentry.isdirectory.html) — Перевіряє, чи є запис директорією
    -   [RarEntry::isEncrypted](rarentry.isencrypted.html) — Перевіряє, чи зашифрований запис
    -   [RarEntry::toString](rarentry.tostring.html) — Отримати текстове подання запису
-   [RarException](class.rarexception.html) - Клас RarException
    -   [RarException::isUsingExceptions](rarexception.isusingexceptions.html) — Перевірити, чи будуть функції повертати помилки чи викидати винятки
    -   [RarException::setUsingExceptions](rarexception.setusingexceptions.html) — Включити або вимкнути генерацію винятків замість повернення помилок