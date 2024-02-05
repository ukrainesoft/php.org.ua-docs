---
navigation:
  - class.volatile.md: « Volatile
  - intro.sem.md: Вступ "
  - index.md: PHP Manual
  - refs.fileprocess.process.md: Модулі для керування процесами програм
title: 'Семафори, пам''ять, що розділяється, і IPC'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Семафори, пам'ять, що розділяється, і IPC

-   [Вступ](intro.sem.md)
-   [Встановлення та налаштування](sem.setup.md)
    -   [Вимоги](sem.requirements.md)
    -   [Установка](sem.installation.md)
    -   [Налаштування під час виконання](sem.configuration.md)
    -   [Типи ресурсів](sem.resources.md)
-   [Обумовлені константи](sem.constants.md)
-   [Функції семафорів](ref.sem.md)
    -   [ftok](function.ftok.md)— Перетворює шлях та ідентифікатор проекту на ключ System V IPC
    -   [msg\_get\_queue](function.msg-get-queue.md)— Створення або підключення до черги повідомлень
    -   [msg\_queue\_exists](function.msg-queue-exists.md)— Перевірка існування черги повідомлень
    -   [msg\_receive](function.msg-receive.md)— Отримання повідомлення з черги повідомлень
    -   [msg\_remove\_queue](function.msg-remove-queue.md)— Видалення черги повідомлень
    -   [msg\_send](function.msg-send.md)— Надсилання повідомлення до черги повідомлень
    -   [msg\_set\_queue](function.msg-set-queue.md)— Встановлення інформації у структурі даних черги повідомлень
    -   [msg\_stat\_queue](function.msg-stat-queue.md)— Отримання інформації із структури даних черги повідомлень
    -   [sem\_acquire](function.sem-acquire.md) \- Захоплення семафору
    -   [sem\_get](function.sem-get.md) \- Отримання ідентифікатора семафору
    -   [sem\_release](function.sem-release.md) \- Звільнення семафору
    -   [sem\_remove](function.sem-remove.md) \- Видалення семафору
    -   [shm\_attach](function.shm-attach.md)— Створює або відкриває сегмент пам'яті, що розділяється.
    -   [shm\_detach](function.shm-detach.md)— Відключається від сегмента пам'яті, що розділяється
    -   [shm\_get\_var](function.shm-get-var.md)— Повертає змінну з пам'яті, що розділяється.
    -   [shm\_has\_var](function.shm-has-var.md)— Перевіряє, чи існує конкретний запис
    -   [shm\_put\_var](function.shm-put-var.md)— Вставляє або оновлює змінну в пам'яті, що розділяється.
    -   [shm\_remove\_var](function.shm-remove-var.md)— Видаляє змінну з пам'яті, що розділяється.
    -   [shm\_remove](function.shm-remove.md)— Видаляє пам'ять із систем Unix, що розділяється.
-   [SysvMessageQueue](class.sysvmessagequeue.md) \- Клас SysvMessageQueue
-   [SysvSemaphore](class.sysvsemaphore.md) \- Клас SysvSemaphore
-   [SysvSharedMemory](class.sysvsharedmemory.md) \- Клас SysvSharedMemory
