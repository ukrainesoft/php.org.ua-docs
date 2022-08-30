Клієнтська бібліотека роботи з URL

-   [« Другие службы](refs.remote.other.html)
    
-   [Введение »](intro.curl.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   Клієнтська бібліотека роботи з URL
    

# Клієнтська бібліотека роботи з URL

-   [Введение](intro.curl.html)
-   [Установка и настройка](curl.setup.html)
    -   [Требования](curl.requirements.html)
    -   [Установка](curl.installation.html)
    -   [Настройка во время выполнения](curl.configuration.html)
    -   [Типы ресурсов](curl.resources.html)
-   [Предопределённые константы](curl.constants.html)
-   [Примеры](curl.examples.html)
    -   [Простий приклад використання curl](curl.examples-basic.html)
-   [Функции cURL](ref.curl.html)
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
-   [CurlHandle](class.curlhandle.html) - Клас CurlHandle
-   [CurlMultiHandle](class.curlmultihandle.html) - Клас CurlMultiHandle
-   [CurlShareHandle](class.curlsharehandle.html) - Клас CurlShareHandle
-   [CURLFile](class.curlfile.html) - Клас CURLFile
    -   [CURLFile::construct](curlfile.construct.html) — Створює об'єкт CURLFile
    -   [CURLFile::getFilename](curlfile.getfilename.html) — Повертає ім'я файлу на сервері
    -   [CURLFile::getMimeType](curlfile.getmimetype.html) - Повертає MIME-тип файлу
    -   [CURLFile::getPostFilename](curlfile.getpostfilename.html) — Повертає ім'я файлу, що надсилається POST-запитом
    -   [CURLFile::setMimeType](curlfile.setmimetype.html) - Встановлює MIME-тип
    -   [CURLFile::setPostFilename](curlfile.setpostfilename.html) — Встановлює ім'я файлу для надсилання методом POST
-   [CURLStringFile](class.curlstringfile.html) - Клас CURLStringFile
    -   [CURLStringFile::construct](curlstringfile.construct.html) — Створює об'єкт CURLStringFile