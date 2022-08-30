Клієнтська бібліотека роботи з URL

-   [« Інші служби](refs.remote.other.md)
    
-   [Введение »](intro.curl.md)
    
-   [PHP Manual](index.md)
    
-   [Інші служби](refs.remote.other.md)
    
-   Клієнтська бібліотека роботи з URL
    

# Клієнтська бібліотека роботи з URL

-   [Введение](intro.curl.md)
-   [Встановлення та налаштування](curl.setup.md)
    -   [Вимоги](curl.requirements.md)
    -   [Установка](curl.installation.md)
    -   [Налаштування під час виконання](curl.configuration.md)
    -   [Типи ресурсів](curl.resources.md)
-   [Обумовлені константи](curl.constants.md)
-   [Приклади](curl.examples.md)
    -   [Простий приклад використання curl](curl.examples-basic.html)
-   [Функции cURL](ref.curl.md)
    -   [curlclose](function.curl-close.html) - Завершує сеанс cURL
    -   [curlcopyhandle](function.curl-copy-handle.html) — Копіює дескриптор cURL разом із усіма його налаштуваннями
    -   [curlerrno](function.curl-errno.html) — Повертає код останньої помилки
    -   [curlerror](function.curl-error.html) — Повертає рядок із описом останньої помилки поточного сеансу
    -   [curlescape](function.curl-escape.html) — Кодує рядок як URL
    -   [curlexec](function.curl-exec.html) — Виконує запит cURL
    -   [curlfilecreate](function.curl-file-create.html) — Створює об'єкт CURLFile
    -   [curlgetinfo](function.curl-getinfo.html) — Повертає інформацію про певну операцію
    -   [curlinit](function.curl-init.html) - Ініціалізує сеанс cURL
    -   [curlmultiaddhandle](function.curl-multi-add-handle.html) — Додає звичайний cURL-дескриптор до набору cURL-дескрипторів
    -   [curlmulticlose](function.curl-multi-close.html) — Закриває набір cURL-дескрипторів
    -   [curlmultierrno](function.curl-multi-errno.html) — Повертає код останньої помилки множинного curl
    -   [curlmultiexec](function.curl-multi-exec.html) — Запускає підключення поточного дескриптора cURL
    -   [curlmultigetcontent](function.curl-multi-getcontent.html) — Повертає результат операції, якщо було встановлено опцію CURLOPTRETURNTRANSFER
    -   [curlmultiinforead](function.curl-multi-info-read.html) — Повертає інформацію про поточні операції
    -   [curlmultiinit](function.curl-multi-init.html) — Створює набір cURL-дескрипторів
    -   [curlmultiremovehandle](function.curl-multi-remove-handle.html) — Видаляє cURL дескриптор із набору cURL дескрипторів
    -   [curlmultiselect](function.curl-multi-select.html) — Чекає на активність на будь-якому curlmulti з'єднанні
    -   [curlmultisetopt](function.curl-multi-setopt.html) — Встановити налаштування для множинного дескриптора cURL
    -   [curlmultistrerror](function.curl-multi-strerror.html) — Повертає рядок, що описує помилку
    -   [curlpause](function.curl-pause.html) — Припинити та відновити з'єднання
    -   [curlreset](function.curl-reset.html) — Скинути налаштування обробника сесії libcurl
    -   [curlsetoptarray](function.curl-setopt-array.html) — Встановлює кілька параметрів сеансу cURL
    -   [curlsetopt](function.curl-setopt.html) — Встановлює параметр сеансу CURL
    -   [curlshareclose](function.curl-share-close.html) — Закрити оброблюваний обробник cURL
    -   [curlshareerrno](function.curl-share-errno.html) — Повертає код останньої помилки оброблюваного обробника curl
    -   [curlshareinit](function.curl-share-init.html) — Ініціалізація оброблюваного обробника cURL
    -   [curlsharesetopt](function.curl-share-setopt.html) — Встановити опції роздільного обробника cURL
    -   [curlsharestrerror](function.curl-share-strerror.html) — Повертає опис для заданого коду помилки
    -   [curlstrerror](function.curl-strerror.html) — Отримати текстовий опис для коду помилки
    -   [curlunescape](function.curl-unescape.html) — Декодує закодований URL-рядок
    -   [curlversion](function.curl-version.html) — Повертає версію cURL
-   [CurlHandle](class.curlhandle.md) - Клас CurlHandle
-   [CurlMultiHandle](class.curlmultihandle.md) - Клас CurlMultiHandle
-   [CurlShareHandle](class.curlsharehandle.md) - Клас CurlShareHandle
-   [CURLFile](class.curlfile.md) - Клас CURLFile
    -   [CURLFile::construct](curlfile.construct.md) — Створює об'єкт CURLFile
    -   [CURLFile::getFilename](curlfile.getfilename.md) — Повертає ім'я файлу на сервері
    -   [CURLFile::getMimeType](curlfile.getmimetype.md) - Повертає MIME-тип файлу
    -   [CURLFile::getPostFilename](curlfile.getpostfilename.md) — Повертає ім'я файлу, що надсилається POST-запитом
    -   [CURLFile::setMimeType](curlfile.setmimetype.md) - Встановлює MIME-тип
    -   [CURLFile::setPostFilename](curlfile.setpostfilename.md) — Встановлює ім'я файлу для надсилання методом POST
-   [CURLStringFile](class.curlstringfile.md) - Клас CURLStringFile
    -   [CURLStringFile::construct](curlstringfile.construct.md) — Створює об'єкт CURLStringFile