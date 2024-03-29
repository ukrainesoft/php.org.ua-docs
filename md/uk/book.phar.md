---
navigation:
  - function.lzf-optimized-for.md: « lzf\_optimized\_for
  - intro.phar.md: Вступ "
  - index.md: PHP Manual
  - refs.compression.md: Модулі для стиснення та архівації
title: Phar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar

-   [Вступ](intro.phar.md)
-   [Встановлення та налаштування](phar.setup.md)
    -   [Вимоги](phar.requirements.md)
    -   [Установка](phar.installation.md)
    -   [Налаштування під час виконання](phar.configuration.md)
    -   [Типи ресурсів](phar.resources.md)
-   [Обумовлені константи](phar.constants.md)
-   [Використання Phar-архівів](phar.using.md)
    -   [Використання Phar-архівів: Вступ](phar.using.intro.md)
    -   [Використання Phar-архівів: обгортка потоку phar](phar.using.stream.md)
    -   [Використання Phar-архівів: класи Phar та PharData](phar.using.object.md)
-   [Створення Phar-архівів](phar.creating.md)
    -   [Створення Phar-архівів: Вступ](phar.creating.intro.md)
-   [Чим відрізняється phar від tar-або zip-архіву?](phar.fileformat.md)
    -   [Складові всіх Phar-архівів незалежно від формату файлу](phar.fileformat.ingredients.md)
    -   [Заглушка Phar-файлу](phar.fileformat.stub.md)
    -   [Порівняння Phar, Tar та Zip](phar.fileformat.comparison.md)
    -   [Phar-архіви, засновані на tar](phar.fileformat.tar.md)
    -   [Phar-архіви на основі zip](phar.fileformat.zip.md)
    -   [Формат файлу phar](phar.fileformat.phar.md)
    -   [Прапори глобальної бітової карти Phar](phar.fileformat.flags.md)
    -   [Опис запису файлу в маніфесті Phar](phar.fileformat.manifestfile.md)
    -   [Формат підпису Phar](phar.fileformat.signature.md)
-   [Phar](class.phar.md) \- Клас Phar
    -   [Phar::addEmptyDir](phar.addemptydir.md)— Додає в phar-архів порожню директорію
    -   [Phar::addFile](phar.addfile.md)— Додає в phar-архів файл із файлової системи
    -   [Phar::addFromString](phar.addfromstring.md)— Додає в phar-архів файл із рядка
    -   [Phar::apiVersion](phar.apiversion.md)— Повертає версію API
    -   [Phar::buildFromDirectory](phar.buildfromdirectory.md)— Створює phar-архів із файлів, розташованих усередині директорії
    -   [Phar::buildFromIterator](phar.buildfromiterator.md) \- Створює phar-архів з ітератора
    -   [Phar::canCompress](phar.cancompress.md)— Перевіряє, чи модуль phar підтримує стиснення з використанням zlib або bzip2
    -   [Phar::canWrite](phar.canwrite.md)— Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
    -   [Phar::compress](phar.compress.md) \- Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
    -   [Phar::compressFiles](phar.compressfiles.md)— Стискає всі файли у поточному Phar-архіві
    -   [Phar::\_\_construct](phar.construct.md)— Створює об'єкт Phar-архіву
    -   [Phar::convertToData](phar.converttodata.md)— Конвертує phar-архів у tar-або zip-файл, що не виконується.
    -   [Phar::convertToExecutable](phar.converttoexecutable.md)— Конвертує phar-архів в інший формат файлу, що виконується.
    -   [Phar::copy](phar.copy.md)— Копіює один файл усередині phar-архіву в інший новий файл усередині phar-архіву
    -   [Phar::count](phar.count.md)— Повертає кількість записів (файлів) у Phar-архіві
    -   [Phar::createDefaultStub](phar.createdefaultstub.md)— Створити заглушку у форматі phar-архіву
    -   [Phar::decompress](phar.decompress.md) \- Розпаковує весь Phar-архів
    -   [Phar::decompressFiles](phar.decompressfiles.md)— Розпаковує всі файли в поточному Phar-архіві
    -   [Phar::delMetadata](phar.delmetadata.md)— Видалити глобальні метадані в архіві phar
    -   [Phar::delete](phar.delete.md)— Видаляє файл усередині phar-архіву
    -   [Phar::\_\_destruct](phar.destruct.md)— Знищує об'єкт архіву Phar
    -   [Phar::extractTo](phar.extractto.md)— Витягти вміст phar-архіву в директорію
    -   [Phar::getAlias](phar.getalias.md) \- Отримати псевдонім для Phar
    -   [Phar::getMetadata](phar.getmetadata.md)— Витягти метадані phar-архіву
    -   [Phar::getModified](phar.getmodified.md)— Визначити, чи змінювався phar-архів
    -   [Phar::getPath](phar.getpath.md)— Отримати реальний шлях до Phar-архіву на диску
    -   [Phar::getSignature](phar.getsignature.md)— Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву
    -   [Phar::getStub](phar.getstub.md)— Отримати завантажувач PHP або завантажувач заглушки Phar-архіву
    -   [Phar::getSupportedCompression](phar.getsupportedcompression.md)— Повертає масив підтримуваних алгоритмів стиснення.
    -   [Phar::getSupportedSignatures](phar.getsupportedsignatures.md)— Отримати масив підтримуваних алгоритмів підпису архіву
    -   [Phar::getVersion](phar.getversion.md)— Отримати версію Phar-архіву
    -   [Phar::hasMetadata](phar.hasmetadata.md)— Перевірити, чи містить phar-архів глобальні метадані
    -   [Phar::interceptFileFuncs](phar.interceptfilefuncs.md) \- Вказує phar перехоплювати fopen, file\_get\_contents, opendir та всі stat-функції
    -   [Phar::isBuffering](phar.isbuffering.md)— Перевірити, чи будуть операції з Phar-архівом буферизовані чи записані безпосередньо на диск
    -   [Phar::isCompressed](phar.iscompressed.md) \- Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
    -   [Phar::isFileFormat](phar.isfileformat.md)— Перевірити, що phar-архів має заданий формат (tar/phar/zip)
    -   [Phar::isValidPharFilename](phar.isvalidpharfilename.md)— Перевіряє, що ім'я файлу є коректним ім'ям phar-архіву.
    -   [Phar::isWritable](phar.iswritable.md) \- Перевіряє, чи можна модифікувати phar-архів
    -   [Phar::loadPhar](phar.loadphar.md)— Завантажити phar-архів із псевдонімом
    -   [Phar::mapPhar](phar.mapphar.md)— Прочитати поточний запущений phar-архів та зареєструвати його маніфест
    -   [Phar::mount](phar.mount.md)— Монтування зовнішнього шляху або файлу до віртуального шляху в phar-архіві
    -   [Phar::mungServer](phar.mungserver.md) \- Визначити список до чотирьох $\_SERVER-змінних, які мають бути змінені для запуску
    -   [Phar::offsetExists](phar.offsetexists.md)— Визначити, чи є файл у архіві
    -   [Phar::offsetGet](phar.offsetget.md)— Отримати PharFileInfo об'єкт для конкретного файлу
    -   [Phar::offsetSet](phar.offsetset.md)— Зміна вмісту файлу
    -   [Phar::offsetUnset](phar.offsetunset.md)— Видалити файл із phar-архіву
    -   [Phar::running](phar.running.md)— Отримати повний шлях на диску або повний URL запущеного Phar-архіву
    -   [Phar::setAlias](phar.setalias.md)— Встановити псевдонім для Phar-архіву
    -   [Phar::setDefaultStub](phar.setdefaultstub.md)— Встановити завантажувач PHP або початкову заглушку Phar-архіву в завантажувач за замовчуванням
    -   [Phar::setMetadata](phar.setmetadata.md)— Встановити метадані phar-архіву
    -   [Phar::setSignatureAlgorithm](phar.setsignaturealgorithm.md)— Встановити алгоритм підписання phar-архіву та застосування його
    -   [Phar::setStub](phar.setstub.md)— Встановити завантажувач або заглушку в Phar-архів
    -   [Phar::startBuffering](phar.startbuffering.md)— Запуск буферизації операцій запису, відключаючи запис змін Phar-архіву на диск
    -   [Phar::stopBuffering](phar.stopbuffering.md)— Зупиняє буферизацію та записує всі зміни на диск
    -   [Phar::unlinkArchive](phar.unlinkarchive.md)— Повністю видалити архів із пам'яті та з диска
    -   [Phar::webPhar](phar.webphar.md)— Надсилає запит із браузера у внутрішній файл у phar-архіві
-   [PharData](class.phardata.md) \- Клас PharData
    -   [PharData::addEmptyDir](phardata.addemptydir.md)— Додати порожню директорію до tar/zip-архіву
    -   [PharData::addFile](phardata.addfile.md)— Додати існуючі файли до tar/zip-архіву
    -   [PharData::addFromString](phardata.addfromstring.md)— Додає файл із рядка до архіву tar/zip
    -   [PharData::buildFromDirectory](phardata.buildfromdirectory.md)— Створює tar/zip-архів із файлів у директорії
    -   [PharData::buildFromIterator](phardata.buildfromiterator.md)— Створення tar/zip-архіву за допомогою ітератора
    -   [PharData::compress](phardata.compress.md)— Стискає весь архів tar/zip, використовуючи стиск Gzip або Bzip2
    -   [PharData::compressFiles](phardata.compressfiles.md)— Стиснути всі файли у поточному tar/zip-архіві
    -   [PharData::\_\_construct](phardata.construct.md) \- Конструктор об'єкта PharData
    -   [PharData::convertToData](phardata.converttodata.md)— Конвертація phar-архіву в tar/zip-архів, що не запускається.
    -   [PharData::convertToExecutable](phardata.converttoexecutable.md)— Конвертація tar/zip-архіву з даними в phar-архів, що запускається
    -   [PharData::copy](phardata.copy.md)— Скопіювати файл із tar/zip-архіву в новий файл усередині нього ж
    -   [PharData::decompress](phardata.decompress.md) \- Розпакувати весь Phar-архів
    -   [PharData::decompressFiles](phardata.decompressfiles.md)— Розпакувати всі файли у поточному zip-архіві
    -   [PharData::delMetadata](phardata.delmetadata.md)— Видалити глобальні метадані для zip-архіву
    -   [PharData::delete](phardata.delete.md)— Видалити файл із tar/zip-архіву
    -   [PharData::\_\_destruct](phardata.destruct.md)— Знищує об'єкт архіву tar або zip, що не виконується.
    -   [PharData::extractTo](phardata.extractto.md)— Витягти вміст tar/zip-архіву в директорію
    -   [PharData::isWritable](phardata.iswritable.md)— Перевірити, чи можна модифікувати tar/zip-архів
    -   [PharData::offsetSet](phardata.offsetset.md)— Зміна вмісту файлу
    -   [PharData::offsetUnset](phardata.offsetunset.md)— Видалити файл із tar/zip-архіву
    -   [PharData::setAlias](phardata.setalias.md)— Функція заглушка (Phar::setAlias ​​не можна використовувати для PharData)
    -   [PharData::setDefaultStub](phardata.setdefaultstub.md)— Функція заглушка (Phar::setDefaultStub не можна використовувати для PharData)
    -   [PharData::setMetadata](phardata.setmetadata.md)— Встановити метадані phar-архіву
    -   [PharData::setSignatureAlgorithm](phardata.setsignaturealgorithm.md)— Встановити алгоритм підписання phar-архіву та застосування його
    -   [PharData::setStub](phardata.setstub.md)— Функція заглушка (Phar::setStub не можна використовувати для PharData)
-   [PharFileInfo](class.pharfileinfo.md) \- Клас PharFileInfo
    -   [PharFileInfo::chmod](pharfileinfo.chmod.md)— Встановлення прав доступу
    -   [PharFileInfo::compress](pharfileinfo.compress.md)— Стиснути поточний файл за допомогою zlib або bzip2
    -   [PharFileInfo::\_\_construct](pharfileinfo.construct.md) \- Конструктор об'єкта PharFileInfo
    -   [PharFileInfo::decompress](pharfileinfo.decompress.md)— Розтискає поточний файл
    -   [PharFileInfo::delMetadata](pharfileinfo.delmetadata.md)— Видалити метадані файлу
    -   [PharFileInfo::\_\_destruct](pharfileinfo.destruct.md) \- Знищує вхідний об'єкт Phar
    -   [PharFileInfo::getCRC32](pharfileinfo.getcrc32.md)— Отримати контрольну суму CRC32
    -   [PharFileInfo::getCompressedSize](pharfileinfo.getcompressedsize.md)— Отримати реальний розмір, що займає файл, на диску з урахуванням стиснення
    -   [PharFileInfo::getContent](pharfileinfo.getcontent.md)— Отримати повний вміст файлу запису
    -   [PharFileInfo::getMetadata](pharfileinfo.getmetadata.md)— Отримати метадані, пов'язані з файлом
    -   [PharFileInfo::getPharFlags](pharfileinfo.getpharflags.md)— Отримати прапори файлу в phar-архіві
    -   [PharFileInfo::hasMetadata](pharfileinfo.hasmetadata.md)— Перевірити, чи є у файлу метадані
    -   [PharFileInfo::isCRCChecked](pharfileinfo.iscrcchecked.md)— Визначити, чи файл пройшов перевірку CRC
    -   [PharFileInfo::isCompressed](pharfileinfo.iscompressed.md)— Перевірити, чи файл стиснутий.
    -   [PharFileInfo::setMetadata](pharfileinfo.setmetadata.md)— Встановлення метаданих для файлу
-   [PharException](class.pharexception.md) \- Клас PharException
