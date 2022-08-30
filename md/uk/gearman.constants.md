Обумовлені константи

-   [« Типи ресурсів](gearman.resources.html)
    
-   [Приклади »](gearman.examples.html)
    
-   [PHP Manual](index.html)
    
-   [Gearman](book.gearman.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

Значення, що повертаються. Завжди перевіряйте значення [GearmanClient::error()](gearmanclient.error.html) або **GearmanWorker()**, що містить рядок з описом помилки, так як у цьому рядку може бути більш детальна інформація про останню операцію:

**`GEARMAN_SUCCESS`** (int)

Операцію було завершено успішно.

**`GEARMAN_IO_WAIT`** (int)

У режимі без блокування подія очікує встановлення блокування.

**`GEARMAN_ERRNO`** (int)

Системна помилка. Щоб отримати код помилки, скористайтеся функцією **GearmanClient::errno()** або **GearmanWorker::errno()**

**`GEARMAN_NO_ACTIVE_FDS`** (int)

На момент виклику [GearmanClient::wait()](gearmanclient.wait.html) або **GearmanWorker()** не було активних підключень.

**`GEARMAN_UNEXPECTED_PACKET`** (int)

Значить, щось пішло зовсім не так, як мало. Застосовується тільки до [GearmanWorker](class.gearmanworker.html)

**`GEARMAN_GETADDRINFO`** (int)

Невдала операція дозволу імен DNS (невірний порт, хост тощо).

**`GEARMAN_NO_SERVERS`** (int)

Перед відправкою завдання чи завдання не було викликано метод [GearmanClient::addServer()](gearmanclient.addserver.html)

**`GEARMAN_LOST_CONNECTION`** (int)

Під час обробки запиту припинилося з'єднання.

**`GEARMAN_MEMORY_ALLOCATION_FAILURE`** (int)

Не вдалося виділити пам'ять (недостатньо пам'яті).

**`GEARMAN_SERVER_ERROR`** (int)

На сервері Gearman стався збій і сервер не зміг обробити запит.

**`GEARMAN_WORK_DATA`** (int)

Код повернення повідомлення, який можна отримати методом [GearmanClient::returnCode()](gearmanclient.returncode.html) під час роботи [GearmanClient::do()](gearmanclient.do.html). Обробник (worker), що виконує завдання, посилає цей код, коли йому потрібно оновити дані на клієнті, передати частину результатів роботи або скинути дані під час виконання довгих завдань.

**`GEARMAN_WORK_WARNING`** (int)

Код повернення повідомлення, який можна отримати методом [GearmanClient::returnCode()](gearmanclient.returncode.html) під час роботи [GearmanClient::do()](gearmanclient.do.html). Оновлює клієнт із відправкою попередженням. Поведінка ті ж, що і у випадку \*\*`GEARMAN_WORK_DATA`\*\*Однак цей код слід інтерпретувати як попередження замість звичайних даних відповіді.

**`GEARMAN_WORK_STATUS`** (int)

Код повернення повідомлення, який можна отримати методом [GearmanClient::returnCode()](gearmanclient.returncode.html) під час роботи [GearmanClient::do()](gearmanclient.do.html). Оброблювач завдання посилає цей код, щоб оновити статус завдання, що довго виконується. Використовуйте [GearmanClient::doStatus()](gearmanclient.dostatus.html) для одержання відсотка завершення роботи.

**`GEARMAN_WORK_EXCEPTION`** (int)

Код повернення повідомлення, який можна отримати методом [GearmanClient::returnCode()](gearmanclient.returncode.html) під час роботи [GearmanClient::do()](gearmanclient.do.html). Вказує, що виконання завдання завершилося невдачею із заданим винятком.

**`GEARMAN_WORK_FAIL`** (int)

Код повернення повідомлення, який можна отримати методом [GearmanClient::returnCode()](gearmanclient.returncode.html) під час роботи [GearmanClient::do()](gearmanclient.do.html). Вказує, що завдання виконати не вдалося.

**`GEARMAN_COULD_NOT_CONNECT`** (int)

Не вдалося підключитися до сервера.

**`GEARMAN_INVALID_FUNCTION_NAME`** (int)

Це значення повертається при спробі зареєструвати NULL як ім'я функції або під час використання callback-інтерфейсу без вказівки callback-функцій.

**`GEARMAN_INVALID_WORKER_FUNCTION`** (int)

Спроба зареєструвати в обробнику функцію, передаючи NULL як callback-функцію.

**`GEARMAN_NO_REGISTERED_FUNCTIONS`** (int)

Коли обробник отримав завдання для функції, яка не зареєстрована.

**`GEARMAN_NO_JOBS`** (int)

Для неблокуючого оброблювача, коли [GearmanWorker::work()](gearmanworker.work.html) немає активних завдань.

**`GEARMAN_ECHO_DATA_CORRUPTION`** (int)

Вказує, що після виклику [GearmanClient::echo()](gearmanclient.echo.html) або [GearmanWorker::echo()](gearmanworker.echo.html) повернені дані не відповідають переданим.

**`GEARMAN_NEED_WORKLOAD_FN`** (int)

Коли клієнт вибрав потоковий режим передачі для обробки, але не задав callback-функцію для обробки даних з цього потоку.

**`GEARMAN_PAUSE`** (int)

При роботі в неблокуючому режимі це значення може повернути callback-функція, щоб призупинити обробку завдання і вийти з методу [GearmanClient::runTasks()](gearmanclient.runtasks.html). Щоб продовжити роботу, слід ще раз викликати метод [GearmanClient::runTasks()](gearmanclient.runtasks.html)

**`GEARMAN_UNKNOWN_STATE`** (int)

Внутрішня помилка клієнта/обробника.

**`GEARMAN_SEND_BUFFER_TOO_SMALL`** (int)

Внутрішня помилка: спроба передати більше даних, ніж в один чанк. Розміри буфера жорстко задані та не підлягають зміні.

**`GEARMAN_TIMEOUT`** (int)

Перевищено час очікування, заданий клієнтом/обробником.

Налаштування [GearmanClient](class.gearmanclient.html)

**`GEARMAN_CLIENT_GENERATE_UNIQUE`** (int)

Створювати унікальний ідентифікатор (UUID) для кожного завдання.

**`GEARMAN_CLIENT_NON_BLOCKING`** (int)

Запускати клієнта у неблокуючому режимі.

**`GEARMAN_CLIENT_UNBUFFERED_RESULT`** (int)

Дозволяти клієнту читати дані та надсилати їх назад у чанках замість буферизації даних цілком засобами бібліотеки.

**`GEARMAN_CLIENT_FREE_TASKS`** (int)

Автоматично знищувати об'єкти завдань після виконання. Ця установка використовується за замовчуванням, щоб запобігти витоку пам'яті.

Налаштування [GearmanWorker](class.gearmanworker.html)

**`GEARMAN_WORKER_NON_BLOCKING`** (int)

Запускати обробник завдань у неблокувальному режимі.

**`GEARMAN_WORKER_GRAB_UNIQ`** (int)

Повертати клієнту унікальний ідентифікатор на додаток до дескриптора завдання.

Базова конфігурація Gearman:

**`GEARMAN_DEFAULT_TCP_HOST`** (string)

**`GEARMAN_DEFAULT_TCP_PORT`** (int)

**`GEARMAN_DEFAULT_SOCKET_TIMEOUT`** (int)

**`GEARMAN_DEFAULT_SOCKET_SEND_SIZE`** (int)

**`GEARMAN_DEFAULT_SOCKET_RECV_SIZE`** (int)

**`GEARMAN_MAX_ERROR_SIZE`** (int)

**`GEARMAN_PACKET_HEADER_SIZE`** (int)

**`GEARMAN_JOB_HANDLE_SIZE`** (int)

**`GEARMAN_OPTION_SIZE`** (int)

**`GEARMAN_UNIQUE_SIZE`** (int)

**`GEARMAN_MAX_COMMAND_ARGS`** (int)

**`GEARMAN_ARGS_BUFFER_SIZE`** (int)

**`GEARMAN_SEND_BUFFER_SIZE`** (int)

**`GEARMAN_RECV_BUFFER_SIZE`** (int)

**`GEARMAN_WORKER_WAIT_TIMEOUT`** (int)