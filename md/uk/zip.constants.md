---
navigation:
  - zip.resources.md: « Типи ресурсів
  - zip.examples.md: Приклади »
  - index.md: PHP Manual
  - book.zip.md: Zip
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

Класс[ZipArchive](class.ziparchive.md) використовує константи класу. Існують константи різних типів, основні з них: Глобальні прапори (префікс) `AFL_`), флаги (префикс`FL_`), ошибки (префикс`ER_`) та константи режиму роботи (без префікса).

**Режими відкриття архіву**

**`ZipArchive::CREATE`**(int)

Створювати архів, якщо він не існує.

**`ZipArchive::OVERWRITE`**(int)

Якщо архів існує, ігнорувати його поточний вміст. Говорячи інакше, обробити його так само, як і порожній архів.

**`ZipArchive::EXCL`**(int)

Виводити помилку, якщо існує архів.

**`ZipArchive::RDONLY`**(int)

Відкрийте архів у режимі лише для читання. Доступно з PHP 7.4.3 та PECL zip 1.17.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.0.0.

**`ZipArchive::CHECKCONS`**(int)

Виконувати додаткові перевірки узгодженості архіву та видавати помилку при невдачі.

**Глобальні прапори архіву**

**`ZipArchive::AFL_RDONLY`**(int)

Архів доступний лише читання, очистити його не можна. Доступно з PHP 8.3.0 та PECL zip 1.22.0, відповідно, якщо зібрано з модулем libzip ≥ 1.10.0.

**`ZipArchive::AFL_IS_TORRENTZIP`**(int)

Поточний архів записаний у форматі torrentzip. Доступно з PHP 8.3.0 та PECL zip 1.22.0 відповідно, якщо зібраний з модулем libzip ≥ 1.10.0.

**`ZipArchive::AFL_WANT_TORRENTZIP`**(int)

Запис архіву у форматі torrentzip. Доступно з PHP 8.3.0 та PECL zip 1.22.0 відповідно, якщо зібраний з модулем libzip ≥ 1.10.0.

**`ZipArchive::AFL_CREATE_OR_KEEP_FILE_FOR_EMPTY_ARCHIVE`**(int)

Не видаляйте файл, якщо архів порожній. Доступно з PHP 8.3.0 та PECL zip 1.22.0 відповідно, якщо зібраний з модулем libzip ≥ 1.10.0.

**Прапори архіву**

**`ZipArchive::FL_NOCASE`**(int)

Ігнорувати регістр символів в іменах елементів архіву.

**`ZipArchive::FL_NODIR`**(int)

Не зважати на шляхи директорій в архіві.

**`ZipArchive::FL_COMPRESSED`**(int)

Читати стислі дані.

**`ZipArchive::FL_UNCHANGED`**(int)

Використовуйте вихідні дані, ігноруючи зміни.

**`ZipArchive::FL_RECOMPRESS`**(int)

Примусово повторювати стиск даних. Доступно з PHP 8.0.0 та PECL zip 1.18.0. Оголошено застарілим з PHP 8.3.0 та PECL zip 1.22.1, буде видалено у майбутній версії модуля libzip.

**`ZipArchive::FL_ENCRYPTED`**(int)

Читати зашифровані дані (мається на увазі FL\_COMPRESSED). Доступно з PHP 8.0.0 та PECL zip 1.18.0.

**`ZipArchive::FL_OVERWRITE`**(int)

Якщо файл з ім'ям існує, перезаписати його. Доступно з PHP 8.0.0 та PECL zip 1.18.0.

**`ZipArchive::FL_LOCAL`**(int)

У локальному заголовку. Доступно з PHP 8.0.0 та PECL zip 1.18.0.

**`ZipArchive::FL_CENTRAL`**(int)

У центральному каталозі. Доступно з PHP 8.0.0 та PECL zip 1.18.0.

**`ZipArchive::FL_ENC_GUESS`**(int)

Вгадати кодування рядка (за замовчуванням). Доступно з PHP 7.0.8.

**`ZipArchive::FL_ENC_RAW`**(int)

Взяти немодифікований рядок. Доступно з PHP 7.0.8.

**`ZipArchive::FL_ENC_STRICT`**(int)

Строго слідувати специфікації. Доступно з PHP 7.0.8.

**`ZipArchive::FL_ENC_UTF_8`**(int)

Рядок у кодуванні UTF-8. Доступно з PHP 7.0.8.

**`ZipArchive::FL_ENC_CP437`**(int)

Рядок у кодуванні CP437. Доступно з PHP 7.0.8.

**`ZipArchive::FL_OPEN_FILE_NOW`**(int)

Відкривати файл при додаванні замість чекати закриття архіву. Пам'ятайте про використання файлових дескрипторів. Доступно з PHP 8.3.0 та PECL zip 1.22.1.

**Режими стиснення**

**`ZipArchive::CM_DEFAULT`**(int)

Вибрати найкращий метод стиснення "deflate" або "stored" (без стиснення).

**`ZipArchive::CM_STORE`**(int)

Застосовувати метод стиснення "stored" (без стиснення).

**`ZipArchive::CM_SHRINK`**(int)

Застосовувати метод стиснення "shrunk".

**`ZipArchive::CM_REDUCE_1`**(int)

Застосовувати метод стиснення "reduced" з коефіцієнтом 1.

**`ZipArchive::CM_REDUCE_2`**(int)

Застосовувати метод стиснення "reduced" з коефіцієнтом 2.

**`ZipArchive::CM_REDUCE_3`**(int)

Застосовувати метод стиснення "reduced" з коефіцієнтом 3.

**`ZipArchive::CM_REDUCE_4`**(int)

Застосовувати метод стиснення "reduced" з коефіцієнтом 4.

**`ZipArchive::CM_IMPLODE`**(int)

Застосовувати метод стиснення "imploded".

**`ZipArchive::CM_DEFLATE`**(int)

Застосовувати метод стиснення "deflated".

**`ZipArchive::CM_DEFLATE64`**(int)

Застосовувати метод стиснення "deflate64".

**`ZipArchive::CM_PKWARE_IMPLODE`**(int)

Застосовувати метод стиснення "PKWARE imploding".

**`ZipArchive::CM_BZIP2`**(int)

Застосовувати метод стиснення алгоритмом BZIP2.

**`ZipArchive::CM_LZMA`**(int)

Застосовувати метод стиснення алгоритмом LZMA.

**`ZipArchive::CM_LZMA2`**(int)

Застосовувати метод стиснення алгоритмом LZMA2. Доступно з PHP 7.4.3 та PECL zip 1.16.0, відповідно, якщо скомпільовано з модулем libzip ≥ 1.6.0.

**`ZipArchive::CM_ZSTD`**(int)

Застосовувати метод стиснення алгоритмом Zstandard. Доступно з PHP 8.0.0 та PECL zip 1.19.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.8.0.

**`ZipArchive::CM_XZ`**(int)

Застосовувати метод стиснення алгоритмом XZ. Доступно з PHP 7.4.3 та PECL zip 1.16.0, відповідно, якщо скомпільовано з модулем libzip ≥ 1.6.0.

**`ZipArchive::CM_TERSE`**(int)

**`ZipArchive::CM_LZ77`**(int)

**`ZipArchive::CM_WAVPACK`**(int)

**`ZipArchive::CM_PPMD`**(int)

**Помилки**

**`ZipArchive::ER_OK`**(int)

Нема помилок.

**`ZipArchive::ER_MULTIDISK`**(int)

Багатотомний ZIP-архів не підтримується.

**`ZipArchive::ER_RENAME`**(int)

Перейменування тимчасового файлу не вдалося.

**`ZipArchive::ER_CLOSE`**(int)

Закриття ZIP-архіву не вдалося.

**`ZipArchive::ER_SEEK`**(int)

Помилка пошуку.

**`ZipArchive::ER_READ`**(int)

Помилка читання.

**`ZipArchive::ER_WRITE`**(int)

Помилка запису.

**`ZipArchive::ER_CRC`**(int)

Помилка контрольної суми.

**`ZipArchive::ER_ZIPCLOSED`**(int)

Відкритий ZIP-архів було закрито.

**`ZipArchive::ER_NOENT`**(int)

Нема такого файлу.

**`ZipArchive::ER_EXISTS`**(int)

Файл існує.

**`ZipArchive::ER_OPEN`**(int)

Неможливо відкрити файл.

**`ZipArchive::ER_TMPOPEN`**(int)

Не вдалося створити тимчасовий файл.

**`ZipArchive::ER_ZLIB`**(int)

Ошибка Zlib.

**`ZipArchive::ER_MEMORY`**(int)

Помилка виділення пам'яті.

**`ZipArchive::ER_CHANGED`**(int) (string)

Запис було змінено.

**`ZipArchive::ER_COMPNOTSUPP`**(int)

Метод стиснення не підтримується.

**`ZipArchive::ER_EOF`**(int)

Передчасний кінець файлу.

**`ZipArchive::ER_INVAL`**(int)

Неприпустимий аргумент.

**`ZipArchive::ER_NOZIP`**(int)

Чи не ZIP-архів.

**`ZipArchive::ER_INTERNAL`**(int)

Внутрішня помилка

**`ZipArchive::ER_INCONS`**(int)

ZIP-архів несумісний.

**`ZipArchive::ER_REMOVE`**(int)

Неможливо видалити файл.

**`ZipArchive::ER_DELETED`**(int)

Запис було видалено.

**`ZipArchive::ER_ENCRNOTSUPP`**(int)

Метод шифрування не підтримується. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно.

**`ZipArchive::ER_RDONLY`**(int)

Архів лише для читання. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно.

**`ZipArchive::ER_NOPASSWD`**(int)

Пароль не вказано. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно.

**`ZipArchive::ER_WRONGPASSWD`**(int)

Наданий неправильний пароль. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно.

**`ZipArchive::ER_OPNOTSUPP`**(int)

Операція не підтримується. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.0.0.

**`ZipArchive::ER_INUSE`**(int)

Ресурс все ще використовується. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.0.0.

**`ZipArchive::ER_TELL`**(int)

Вказано помилку. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.0.0.

**`ZipArchive::ER_COMPRESSED_DATA`**(int)

Стиснуті дані неправильні. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.0.0.

**`ZipArchive::ER_CANCELLED`**(int)

Операцію скасовано. Доступно з PHP 7.4.3 та PECL zip 1.16.1, відповідно, якщо скомпільовано з модулем libzip ≥ 1.0.0.

**`ZipArchive::ER_DATA_LENGTH`**(int)

Несподівана довжина даних. Доступно з PHP 8.3.0 та PECL zip 1.22.0 відповідно, якщо зібраний з модулем libzip ≥ 1.10.0.

**`ZipArchive::ER_NOT_ALLOWED`**(int)

Не допускається в torrentzip. Доступно з PHP 8.3.0 та PECL zip 1.22.0 відповідно, якщо зібраний з модулем libzip ≥ 1.10.0.

**Режими шифрування**

**`ZipArchive::EM_NONE`**(int)

Без шифрування. Доступно з PHP 7.2.0 та PECL zip 1.14.0, відповідно, якщо скомпільовано з модулем libzip ≥ 1.2.0.

**`ZipArchive::EM_TRAD_PKWARE`**(int)

Традиційне шифрування PKWARE. Доступно з PHP 8.0.0 та PECL zip 1.19.0.

**`ZipArchive::EM_AES_128`**(int)

Шифрування AES 128. Доступно з PHP 7.2.0 та PECL zip 1.14.0, відповідно, якщо скомпільовано з модулем libzip ≥ 1.2.0.

**`ZipArchive::EM_AES_192`**(int)

Шифрування AES 192. Доступно з PHP 7.2.0 та PECL zip 1.14.0, відповідно, якщо скомпільовано з модулем libzip ≥ 1.2.0.

**`ZipArchive::EM_AES_256`**(int)

Шифрування AES 256. Доступно з PHP 7.2.0 та PECL zip 1.14.0, відповідно, якщо скомпільовано з модулем libzip ≥ 1.2.0.

**`ZipArchive::EM_UNKNOWN`**(int)

Без шифрування. Доступно з PHP 8.0.0 та PECL zip 1.19.0.

**Константи параметрів довжини**

**`ZipArchive::LENGTH_TO_END`**(int)

Використовувати розмір файлу, якщо файл збільшується, додаткові дані будуть проігноровані, якщо файл зменшується, виникне помилка (**`ZipArchive::ER_DATA_LENGTH`**). Доступно з PHP 8.3.0 та PECL zip 1.22.2.

**`ZipArchive::LENGTH_UNCHECKED`**(int)

Використовуйте всі доступні дані. Доступно з PHP 8.3.0 та PECL zip 1.22.2, якщо зібрано з модулем libzip ≥ 1.10.1.

**Інші константи**

**`ZipArchive::LIBZIP_VERSION`**(int) (string)

Версія бібліотеки Zip. Доступно з PHP 7.4.3 та PECL zip 1.16.0.

**Константи операційної системи для зовнішніх атрибутів**

**`ZipArchive::OPSYS_DOS`**(int)

**`ZipArchive::OPSYS_AMIGA`**(int)

**`ZipArchive::OPSYS_OPENVMS`**(int)

**`ZipArchive::OPSYS_UNIX`**(int)

**`ZipArchive::OPSYS_VM_CMS`**(int)

**`ZipArchive::OPSYS_ATARI_ST`**(int)

**`ZipArchive::OPSYS_OS_2`**(int)

**`ZipArchive::OPSYS_MACINTOSH`**(int)

**`ZipArchive::OPSYS_Z_SYSTEM`**(int)

**`ZipArchive::OPSYS_CPM`**(int)

**`ZipArchive::OPSYS_WINDOWS_NTFS`**(int)

**`ZipArchive::OPSYS_MVS`**(int)

**`ZipArchive::OPSYS_VSE`**(int)

**`ZipArchive::OPSYS_ACORN_RISC`**(int)

**`ZipArchive::OPSYS_VFAT`**(int)

**`ZipArchive::OPSYS_ALTERNATE_MVS`**(int)

**`ZipArchive::OPSYS_BEOS`**(int)

**`ZipArchive::OPSYS_TANDEM`**(int)

**`ZipArchive::OPSYS_OS_400`**(int)

**`ZipArchive::OPSYS_OS_X`**(int)

**`ZipArchive::OPSYS_DEFAULT`**(int)

Починаючи з PECL zip 1.12.4
