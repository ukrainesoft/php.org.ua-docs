---
navigation:
  - sockets.resources.md: « Типи ресурсів
  - sockets.examples.md: Приклади »
  - index.md: PHP Manual
  - book.sockets.md: Сокети
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`AF_UNIX`**(int)

**`AF_INET`**(int)

**`AF_INET6`**(int)

Константа доступна, лише якщо PHP скомпільовано за допомогою IPv6.

**`AF_DIVERT`**(int)

Константа доступна з PHP 8.3.0 (тільки на FreeBSD)

**`SOCK_STREAM`**(int)

**`SOCK_DGRAM`**(int)

**`SOCK_RAW`**(int)

**`SOCK_SEQPACKET`**(int)

**`SOCK_RDM`**(int)

**`MSG_OOB`**(int)

**`MSG_WAITALL`**(int)

**`MSG_PEEK`**(int)

**`MSG_DONTROUTE`**(int)

**`MSG_EOR`**(int)

Константа недоступна на платформах Windows.

**`MSG_EOF`**(int)

Константа недоступна на платформах Windows.

**`MSG_ZEROCOPY`**(int)

Константа доступна з PHP 8.2.0.

**`SO_DEBUG`**(int)

**`SO_REUSEADDR`**(int)

**`SO_REUSEPORT`**(int)

Ця константа доступна лише на платформах, які підтримують опцію \*\*`SO_REUSEPORT`\*\*сокета: сюда входят Linux, macOS и\*BSD, але Windows не входить.

**`SO_KEEPALIVE`**(int)

**`SO_DONTROUTE`**(int)

**`SO_LINGER`**(int)

**`SO_BROADCAST`**(int)

**`SO_OOBINLINE`**(int)

**`SO_SNDBUF`**(int)

**`SO_RCVBUF`**(int)

**`SO_SNDLOWAT`**(int)

**`SO_RCVLOWAT`**(int)

**`SO_SNDTIMEO`**(int)

**`SO_RCVTIMEO`**(int)

**`SO_TYPE`**(int)

**`SO_ERROR`**(int)

**`SO_ZEROCOPY`**(int)

Константа доступна з PHP 8.2.0.

**`TCP_NODELAY`**(int)

Константа використовується для відключення TCP-алгоритму Нагла.

**`TCP_KEEPCNT`**(int)

Константа доступна з PHP 8.2.0.

**`TCP_KEEPIDLE`**(int)

Константа доступна з PHP 8.2.0.

**`TCP_KEEPINTVL`**(int)

Константа доступна з PHP 8.2.0.

**`TCP_KEEPALIVE`**(int)

Константа доступна з PHP 8.2.0.

**`TCP_NOTSENT_LOWAT`**(int)

Константа доступна з PHP 8.2.0.

**`SO_MARK`**(int)

Константа доступна з PHP 8.1.0

**`SO_USER_COOKIE`**(int)

Константа доступна з PHP 8.1.0

**`SO_RTABLE`**(int)

Константа доступна з PHP 8.2.0.

**`SO_ACCEPTFILTER`**(int)

Константа доступна з PHP 8.1.0

**`SO_DONTTRUNC`**(int)

Константа доступна з PHP 8.1.0

**`SO_WANTMORE`**(int)

Константа доступна з PHP 8.1.0

**`SO_INCOMING_CPU`**(int)

Константа доступна з PHP 8.2.0.

**`SO_MEMINFO`**(int)

Константа доступна з PHP 8.2.0.

**`SO_BPF_EXTENSIONS`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SO_SETFIB`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SO_ATTACH_REUSEPORT_CBPF`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`SO_DETACH_BPF`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`SO_DETACH_FILTER`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`SO_RERROR`**(int)

Константа доступна з PHP 8.3.0 (лише NetBSD)

**`SO_ZEROIZE`**(int)

Константа доступна з PHP 8.3.0 (лише OpenBSD)

**`SO_SPLICE`**(int)

Константа доступна з PHP 8.3.0 (лише OpenBSD)

**`SO_REUSEPORT_LB`**(int)

Константа доступна з PHP 8.3.0 (тільки на FreeBSD)

**`SOL_FILTER`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SOL_UDPLITE`**(int)

Константа доступна з PHP 8.3.0

**`UDPLITE_RECV_CSCOV`**(int)

Константа доступна з PHP 8.3.0

**`UDPLITE_SEND_CSCOV`**(int)

Константа доступна з PHP 8.3.0

**`TCP_DEFER_ACCEPT`**(int)

Константа доступна з PHP 8.1.0

**`TCP_CONGESTION`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`TCP_QUICKACK`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`TCP_REPAIR`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_DONTFRAG`**(int)

Константа доступна з PHP 8.3.0 (тільки на FreeBSD)

**`IP_MTU_DISCOVER`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_PMTUDISC_DO`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_PMTUDISC_DONT`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_PMTUDISC_WANT`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_PMTUDISC_PROBE`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_PMTUDISC_INTERFACE`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_PMTUDISC_OMIT`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`IP_BIND_ADDRESS_NO_PORT`**(int)

Константа доступна з PHP 8.3.0 (лише Linux)

**`SOL_SOCKET`**(int)

**`PHP_NORMAL_READ`**(int)

**`PHP_BINARY_READ`**(int)

**`SOL_TCP`**(int)

**`SOL_UDP`**(int)

Наступні константи визначені лише у Windows та Unix-подібних системах. Кожна константа визначена лише, якщо її еквівалент доступний у системі.

**`SOCKET_EINTR`**(int)

Перерваний системний виклик.

**`SOCKET_EBADF`**(int)

Неправильний номер файлу дескриптора.

**`SOCKET_EACCES`**(int)

Доступ заборонено.

**`SOCKET_EFAULT`**(int)

Неправильна адреса.

**`SOCKET_EINVAL`**(int)

Неправильний аргумент.

**`SOCKET_EMFILE`**(int)

Занадто багато відкритих файлів.

**`SOCKET_ENAMETOOLONG`**(int)

Занадто довге ім'я файлу.

**`SOCKET_ENOTEMPTY`**(int)

Каталог не порожній.

**`SOCKET_ELOOP`**(int)

Виявлено дуже багато символічних посилань.

**`SOCKET_EWOULDBLOCK`**(int)

Операцію буде блоковано.

**`SOCKET_EREMOTE`**(int)

Об'єкт є віддаленим.

**`SOCKET_EUSERS`**(int)

Занадто багато користувачів.

**`SOCKET_ENOTSOCK`**(int)

Socket operation on non-socket.

**`SOCKET_EDESTADDRREQ`**(int)

Destination address required.

**`SOCKET_EMSGSIZE`**(int)

Повідомлення надто довге.

**`SOCKET_EPROTOTYPE`**(int)

Protocol wrong type for socket.

**`SOCKET_EPROTONOSUPPORT`**(int)

Протокол не підтримується.

**`SOCKET_ESOCKTNOSUPPORT`**(int)

Тип сокету не підтримується.

**`SOCKET_EOPNOTSUPP`**(int)

Операція не підтримується кінцевою точкою транспорту.

**`SOCKET_EPFNOSUPPORT`**(int)

Сімейство протоколів не підтримується.

**`SOCKET_EAFNOSUPPORT`**(int)

Сімейство адрес не підтримується протоколом.

**`SOCKET_EADDRNOTAVAIL`**(int)

Неможливо призначити потрібну адресу.

**`SOCKET_ENETDOWN`**(int)

Мережа не працює.

**`SOCKET_ENETUNREACH`**(int)

Мережа недоступна.

**`SOCKET_ENETRESET`**(int)

Мережа скинула з'єднання через переустановку з'єднання.

**`SOCKET_ECONNABORTED`**(int)

Програма викликала розрив з'єднання.

**`SOCKET_ECONNRESET`**(int)

З'єднання скинуто вузлом.

**`SOCKET_ENOBUFS`**(int)

Немає буферного простору.

**`SOCKET_EISCONN`**(int)

Кінцева точка транспорту вже приєднана.

**`SOCKET_ENOTCONN`**(int)

Кінцева точка транспорту не приєднана.

**`SOCKET_ESHUTDOWN`**(int)

Неможливо надіслати дані через відключення кінцевої точки транспорту.

**`SOCKET_ETIMEDOUT`**(int)

Сплив час з'єднання.

**`SOCKET_ECONNREFUSED`**(int)

Відмова у з'єднанні.

**`SOCKET_EHOSTDOWN`**(int)

Хост вимкнено.

**`SOCKET_EHOSTUNREACH`**(int)

Нема маршруту до хоста.

**`SOCKET_EALREADY`**(int)

Операція вже у прогресі.

**`SOCKET_EINPROGRESS`**(int)

Операція зараз у прогресі.

Наступні константи визначено лише у Windows.

**`SOCKET_ENOPROTOOPT`**(int)

**`SOCKET_EADDRINUSE`**(int)

**`SOCKET_ETOOMYREFS`**(int)

**`SOCKET_EPROCLIM`**(int)

**`SOCKET_EDUOT`**(int)

**`SOCKET_ESTALE`**(int)

**`SOCKET_EDISCON`**(int)

**`SOCKET_SYSNOTREADY`**(int)

**`SOCKET_VERNOTSUPPORTED`**(int)

**`SOCKET_NOTINITIALISED`**(int)

**`SOCKET_HOST_NOT_FOUND`**(int)

**`SOCKET_TRY_AGAIN`**(int)

**`SOCKET_NO_RECOVERY`**(int)

**`SOCKET_NO_DATA`**(int)

**`SOCKET_NO_ADDRESS`**(int)

Наступні константи доступні лише на UNIX-платформах. Кожна константа визначена лише якщо її еквівалент доступний на платформі.

**`SOCKET_EPERM`**(int)

Операція заборонена.

**`SOCKET_ENOENT`**(int)

Немає такого файлу чи каталогу.

**`SOCKET_EIO`**(int)

Помилка введення-виведення.

**`SOCKET_ENXIO`**(int)

Немає такого пристрою чи адреси.

**`SOCKET_E2BIG`**(int)

Список аргументів надто довгий.

**`SOCKET_EAGAIN`**(int)

Спробуйте ще раз.

**`SOCKET_ENOMEM`**(int)

Переповнення доступної пам'яті.

**`SOCKET_ENOTBLK`**(int)

Потрібен блоковий пристрій.

**`SOCKET_EBUSY`**(int)

Пристрій чи ресурс зайнятий.

**`SOCKET_EEXIST`**(int)

Файл існує.

**`SOCKET_EXDEV`**(int)

Посилання на крос-пристрій.

**`SOCKET_ENODEV`**(int)

Нема такого пристрою.

**`SOCKET_ENOTDIR`**(int)

Це не каталог.

**`SOCKET_EISDIR`**(int)

Це каталог.

**`SOCKET_ENFILE`**(int)

Переповнення файлової таблиці.

**`SOCKET_ENOTTY`**(int)

Пристрій, що не друкує.

**`SOCKET_ENOSPC`**(int)

Не залишилося місця на пристрої.

**`SOCKET_ESPIPE`**(int)

Неприпустимий запит.

**`SOCKET_EROFS`**(int)

Файлова система доступна лише для читання.

**`SOCKET_EMLINK`**(int)

Занадто багато посилань.

**`SOCKET_EPIPE`**(int)

Обірваний канал.

**`SOCKET_ENOLCK`**(int)

Неможливо блокувати запис.

**`SOCKET_ENOSYS`**(int)

Функцію не реалізовано.

**`SOCKET_ENOMSG`**(int)

Немає повідомлення бажаного типу.

**`SOCKET_EIDRM`**(int)

Ідентифікатор видалено.

**`SOCKET_ECHRNG`**(int)

Тип каналу виходить за межі діапазону.

**`SOCKET_EL2NSYNC`**(int)

Рівень 2 не синхронізовано.

**`SOCKET_EL3HLT`**(int)

Рівень 3 зупинено.

**`SOCKET_EL3RST`**(int)

Рівень 3 скинутий.

**`SOCKET_ELNRNG`**(int)

Номер посилання виходить за межі діапазону.

**`SOCKET_EUNATCH`**(int)

Драйвер протоколу не підключено.

**`SOCKET_ENOCSI`**(int)

CSI-структура недоступна.

**`SOCKET_EL2HLT`**(int)

Рівень 2 зупинено.

**`SOCKET_EBADE`**(int)

Неприпустимий комутатор.

**`SOCKET_EBADR`**(int)

Неприпустимий дескриптор запиту.

**`SOCKET_EXFULL`**(int)

Комутатор заповнено.

**`SOCKET_ENOANO`**(int)

Чи не anode.

**`SOCKET_EBADRQC`**(int)

Неприпустимий код запиту.

**`SOCKET_EBADSLT`**(int)

Неприпустимий слот.

**`SOCKET_ENOSTR`**(int)

Пристрій не є потоковим.

**`SOCKET_ENODATA`**(int)

Немає доступних даних.

**`SOCKET_ETIME`**(int)

Таймер закінчився.

**`SOCKET_ENOSR`**(int)

Закінчилися потокові ресурси.

**`SOCKET_ENONET`**(int)

Машину не підключено до мережі.

**`SOCKET_ENOLINK`**(int)

Посилання було розірвано.

**`SOCKET_EADV`**(int)

Помилка оголошення (advertise).

**`SOCKET_ESRMNT`**(int)

Помилка Srmount.

**`SOCKET_ECOMM`**(int)

Помилка зв'язку під час відправлення.

**`SOCKET_EPROTO`**(int)

Помилка протоколу.

**`SOCKET_EMULTIHOP`**(int)

Спроба перейти на недоступний ресурс (multihop).

**`SOCKET_EBADMSG`**(int)

Не є повідомлення з даними.

**`SOCKET_ENOTUNIQ`**(int)

Ім'я не унікальне у мережі.

**`SOCKET_EBADFD`**(int)

Файловий покажчик у неправильному стані.

**`SOCKET_EREMCHG`**(int)

Віддалена адреса змінилася.

**`SOCKET_ERESTART`**(int)

Перерваний системний виклик повинен бути перезапущений.

**`SOCKET_ESTRPIPE`**(int)

Помилка потоку каналу.

**`SOCKET_EPROTOOPT`**(int)

Протокол недоступний.

**`SOCKET_ADDRINUSE`**(int)

Адреса вже у використанні.

**`SOCKET_ETOOMANYREFS`**(int)

Забагато посилань: не можу з'єднати.

**`SOCKET_EISNAM`**(int)

Іменований тип файлу.

**`SOCKET_EREMOTEIO`**(int)

Помилка віддаленого введення-виводу.

**`SOCKET_EDQUOT`**(int)

Квота перевищена.

**`SOCKET_ENOMEDIUM`**(int)

Носій не знайдено.

**`SOCKET_EMEDIUMTYPE`**(int)

Неправильний тип носія.

**`SCM_RIGHTS`**(int)

Надіслати чи отримати набір дескрипторів відкритих файлів з іншого процесу.

**`SCM_CREDENTIALS`**(int)

**`SCM_CREDS`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SCM_CREDS2`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`LOCAL_CREDS`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`LOCAL_CREDS_PERSISTENT`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_OFF`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_PROTOCOL`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_PKTTYPE`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_IFINDEX`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_NLATTR`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_NLATTR_NEST`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_MARK`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_QUEUE`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_HATYPE`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_RXHASH`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_CPU`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_ALU_XOR_X`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_VLAN_TAG`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_VLAN_TAG_PRESENT`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_PAY_OFFSET`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_RANDOM`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_VLAN_TPID`**(int)

Константа доступна починаючи з PHP 8.2.0.

**`SKF_AD_MAX`**(int)

Константа доступна починаючи з PHP 8.2.0.
