---
navigation:
  - class.volatile.md: « Volatile
  - intro.sem.md: Введение »
  - index.md: PHP Manual
  - refs.fileprocess.process.md: Модули для управления процессами программ
title: 'Семафори, пам''ять, що розділяється, і IPC'
---
# Семафори, пам'ять, що розділяється, і IPC

-   [Введение](intro.sem.md)
-   [Встановлення та налаштування](sem.setup.md)
    -   [Вимоги](sem.requirements.md)
    -   [Установка](sem.installation.md)
    -   [Налаштування під час виконання](sem.configuration.md)
    -   [Типи ресурсів](sem.resources.md)
-   [Обумовлені константи](sem.constants.md)
-   [Функції семафорів](ref.sem.md)
    -   [ftok](function.ftok.md) — Перетворення шляху та ідентифікатора проекту на ключ System V IPC
    -   [msggetqueue](function.msg-get-queue.md) — Створення або підключення до черги повідомлень
    -   [msgqueueexists](function.msg-queue-exists.md) — Перевірка існування черги повідомлень
    -   [msgreceive](function.msg-receive.md) — Отримання повідомлення з черги повідомлень
    -   [msgremovequeue](function.msg-remove-queue.md) — Видалення черги повідомлень
    -   [msgsend](function.msg-send.md) — Надсилання повідомлення до черги повідомлень
    -   [msgsetqueue](function.msg-set-queue.md) — Встановлення інформації у структурі даних черги повідомлень
    -   [msgstatqueue](function.msg-stat-queue.md) — Отримання інформації із структури даних черги повідомлень
    -   [semacquire](function.sem-acquire.md) - Захоплення семафору
    -   [semget](function.sem-get.md) - Отримання ідентифікатора семафору
    -   [semrelease](function.sem-release.md) - Звільнення семафору
    -   [semremove](function.sem-remove.md) - Видалення семафору
    -   [shmattach](function.shm-attach.md) — Створює або відкриває сегмент пам'яті, що розділяється.
    -   [shmdetach](function.shm-detach.md) — Відключається від сегмента пам'яті, що розділяється.
    -   [shmgetvar](function.shm-get-var.md) — Повертає змінну з пам'яті, що розділяється.
    -   [shmhasvar](function.shm-has-var.md) — Перевіряє, чи існує конкретний запис
    -   [shmputvar](function.shm-put-var.md) — Вставляє або оновлює змінну в пам'яті, що розділяється.
    -   [shmremovevar](function.shm-remove-var.md) — Видаляє змінну з пам'яті, що розділяється.
    -   [shmremove](function.shm-remove.md) — Видаляє пам'ять із систем Unix, що розділяється.
-   [SysvMessageQueue](class.sysvmessagequeue.md) - Клас SysvMessageQueue
-   [SysvSemaphore](class.sysvsemaphore.md) - Клас SysvSemaphore
-   [SysvSharedMemory](class.sysvsharedmemory.md) - Клас SysvSharedMemory
