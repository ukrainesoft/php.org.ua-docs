---
navigation:
  - win32service.constants.serviceflag.md: Константи прапорів сервісу Win32Service
  - win32service.constants.basepriorities.md: Базові класи пріоритетів Win32
  - index.md: PHP Manual
  - win32service.constants.md: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
> **Зауваження** :
> 
> Ці константи не використовуються з Win32Service 1.0.0.

**Коди помилок Win32**

| Константа | Значение | Опис |
| --- | --- | --- |
| **`WIN32_ERROR_ACCESS_DENIED`** | 0x00000005 | Обробник бази даних SCM не має потрібних прав доступу. |
| **`WIN32_ERROR_CIRCULAR_DEPENDENCY`** | 0x00000423 | Задано взаємну залежність служб. |
| **`WIN32_ERROR_DATABASE_DOES_NOT_EXIST`** | 0x00000429 | Вказана база даних відсутня. |
| **`WIN32_ERROR_DEPENDENT_SERVICES_RUNNING`** | 0x0000041B | Службу не можна зупинити, оскільки від неї залежить інша запущена служба. |
| **`WIN32_ERROR_DUPLICATE_SERVICE_NAME`** | 0x00000436 | Ім'я, що відображається, вже існує в базі даних диспетчера служб або як ім'я служби або як інше відображене ім'я. |
| **`WIN32_ERROR_FAILED_SERVICE_CONTROLLER_CONNECT`** | 0x00000427 | Ця помилка повертається, якщо програма запускається як консольна програма, а не як служба. Якщо програма виконується як консольна програма для налагодження, структуруйте її таким чином, щоб код, специфічний для служб, не викликався. |
| **`WIN32_ERROR_INSUFFICIENT_BUFFER`** | 0x0000007A | Буфер дуже малий для структури стану служби. У структуру нічого не буде записано. |
| **`WIN32_ERROR_INVALID_DATA`** | 0x0000000D | Вказано некоректну структуру стану служби. |
| **`WIN32_ERROR_INVALID_HANDLE`** | 0x00000006 | Обробник для зазначеної бази даних диспетчера керування службами недійсний. |
| **`WIN32_ERROR_INVALID_LEVEL`** | 0x0000007C | Параметр InfoLevel містить непідтримуване значення. |
| **`WIN32_ERROR_INVALID_NAME`** | 0x0000007B | Вказане ім'я служби неправильне. |
| **`WIN32_ERROR_INVALID_PARAMETER`** | 0x00000057 | Зазначений параметр некоректний. |
| **`WIN32_ERROR_INVALID_SERVICE_ACCOUNT`** | 0x00000421 | Ім'я облікового запису користувача, вказане в `user` Відсутнє. Дивіться [win32\_create\_service()](function.win32-create-service.md) |
| **`WIN32_ERROR_INVALID_SERVICE_CONTROL`** | 0x0000041C | Запитаний контрольний код є недійсним або неприйнятним для служби. |
| **`WIN32_ERROR_PATH_NOT_FOUND`** | 0x00000003 | Виконуваний файл служби не знайдено. |
| **`WIN32_ERROR_SERVICE_ALREADY_RUNNING`** | 0x00000420 | Екземпляр служби вже запущено. |
| **`WIN32_ERROR_SERVICE_CANNOT_ACCEPT_CTRL`** | 0x00000425 | Запитаний код керування не може бути надісланий службі, оскільки її статус **`WIN32_SERVICE_STOPPED`** **`WIN32_SERVICE_START_PENDING`**, или\*\*`WIN32_SERVICE_STOP_PENDING`\*\* |
| **`WIN32_ERROR_SERVICE_DATABASE_LOCKED`** | 0x0000041F | Базу даних заблоковано. |
| **`WIN32_ERROR_SERVICE_DEPENDENCY_DELETED`** | 0x00000433 | Служба залежить від служби якої немає або яка відзначена для видалення. |
| **`WIN32_ERROR_SERVICE_DEPENDENCY_FAIL`** | 0x0000042C | Служба залежить від іншої служби, яка не може запуститись. |
| **`WIN32_ERROR_SERVICE_DISABLED`** | 0x00000422 | Службу заборонено. |
| **`WIN32_ERROR_SERVICE_DOES_NOT_EXIST`** | 0x00000424 | Вказану службу не встановлено. |
| **`WIN32_ERROR_SERVICE_EXISTS`** | 0x00000431 | Зазначена служба вже є у базі даних. |
| **`WIN32_ERROR_SERVICE_LOGON_FAILED`** | 0x0000042D | Служба не може запуститися через проблеми авторизації. Така помилка трапляється, якщо служба налаштована на запуск під обліковим записом, яка не має права запускатися як службі (Log on as a service). |
| **`WIN32_ERROR_SERVICE_MARKED_FOR_DELETE`** | 0x00000430 | Вказана служба вже позначена для видалення. |
| **`WIN32_ERROR_SERVICE_NO_THREAD`** | 0x0000041E | Для цієї служби може бути створено потік. |
| **`WIN32_ERROR_SERVICE_NOT_ACTIVE`** | 0x00000426 | Службу не запущено. |
| **`WIN32_ERROR_SERVICE_REQUEST_TIMEOUT`** | 0x0000041D | Процес служби стартований, але він не викликав StartServiceCtrlDispatcher, або потік, що викликав StartServiceCtrlDispatcher, заблокований функцією керуючої обробки. |
| **`WIN32_ERROR_SHUTDOWN_IN_PROGRESS`** | 0x0000045B | Система зупиняється; ця функція може бути викликана. |
| **`WIN32_ERROR_SERVICE_SPECIFIC_ERROR`** | 0x0000042A | Служба повернула свій код помилки. |
| **`WIN32_NO_ERROR`** | 0x00000000 | Нема помилок. |
