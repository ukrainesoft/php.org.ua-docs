---
navigation:
  - function.expect-popen.md: « expect\_popen
  - intro.pcntl.md: Вступ "
  - index.md: PHP Manual
  - refs.fileprocess.process.md: Модулі для керування процесами програм
title: Управління процесами
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Управління процесами

-   [Вступ](intro.pcntl.md)
-   [Встановлення та налаштування](pcntl.setup.md)
    -   [Вимоги](pcntl.requirements.md)
    -   [Установка](pcntl.installation.md)
    -   [Налаштування під час виконання](pcntl.configuration.md)
    -   [Типи ресурсів](pcntl.resources.md)
-   [Обумовлені константи](pcntl.constants.md)
-   [Приклади](pcntl.examples.md)
    -   [Базове застосування](pcntl.example.md)
-   [Функції PCNTL](ref.pcntl.md)
    -   [pcntl\_alarm](function.pcntl-alarm.md) \- Задати таймер доставки сигналу SIGALRM
    -   [pcntl\_async\_signals](function.pcntl-async-signals.md)— Увімкнути/вимкнути асинхронну обробку сигналів або отримати поточний статус
    -   [pcntl\_errno](function.pcntl-errno.md) \- Псевдонім pcntl\_get\_last\_error
    -   [pcntl\_exec](function.pcntl-exec.md)— Запустити вказану програму в галузі поточного процесу
    -   [pcntl\_fork](function.pcntl-fork.md) \- Розгалужити (fork) поточний запущений процес
    -   [pcntl\_get\_last\_error](function.pcntl-get-last-error.md)— Отримати код останньої помилки, що виникла у pcntl-функції
    -   [pcntl\_getpriority](function.pcntl-getpriority.md)— Отримати значення пріоритету процесу
    -   [pcntl\_rfork](function.pcntl-rfork.md)— Взаємодіє із ресурсами процесу
    -   [pcntl\_setpriority](function.pcntl-setpriority.md)— Змінити пріоритет процесу
    -   [pcntl\_signal\_dispatch](function.pcntl-signal-dispatch.md)— Викликає обробники для сигналів, що очікують.
    -   [pcntl\_signal\_get\_handler](function.pcntl-signal-get-handler.md)— Отримати поточний обробник вказаного сигналу
    -   [pcntl\_signal](function.pcntl-signal.md) \- Встановлення обробника сигналу
    -   [pcntl\_sigprocmask](function.pcntl-sigprocmask.md)— Задає та витягує список сигналів, що блокуються.
    -   [pcntl\_sigtimedwait](function.pcntl-sigtimedwait.md)— Очікує сигнали протягом заданого часу
    -   [pcntl\_sigwaitinfo](function.pcntl-sigwaitinfo.md)— Очікування сигналів
    -   [pcntl\_strerror](function.pcntl-strerror.md)— Отримати текст помилки за її кодом
    -   [pcntl\_unshare](function.pcntl-unshare.md)— Поділяє частини контексту виконання процесу
    -   [pcntl\_wait](function.pcntl-wait.md)— Очікує чи повертає статус породженого дочірнього процесу
    -   [pcntl\_waitpid](function.pcntl-waitpid.md)— Очікує чи повертає статус породженого дочірнього процесу
    -   [pcntl\_wexitstatus](function.pcntl-wexitstatus.md)— Отримати код повернення завершеного дочірнього процесу
    -   [pcntl\_wifexited](function.pcntl-wifexited.md)— Перевіряє, чи код завершення процесу відповідає нормальному завершенню.
    -   [pcntl\_wifsignaled](function.pcntl-wifsignaled.md)— Перевірити, чи код завершення процесу завершення за сигналом відповідає
    -   [pcntl\_wifstopped](function.pcntl-wifstopped.md)— Перевірити, чи зупинено дочірній процес
    -   [pcntl\_wstopsig](function.pcntl-wstopsig.md)— Отримати сигнал, через який було зупинено дочірній процес
    -   [pcntl\_wtermsig](function.pcntl-wtermsig.md)— Отримати сигнал, через який було примусово завершено дочірній процес
