Функції PCNTL

-   [« Базовое применение](pcntl.example.html)
    
-   [pcntl\_alarm »](function.pcntl-alarm.html)
    
-   [PHP Manual](index.html)
    
-   [PCNTL](book.pcntl.html)
    
-   Функції PCNTL
    

# Функції PCNTL

# Дивіться також

Огляд розділу про [функциях POSIX](ref.posix.html) може бути корисним.

## Зміст

-   [pcntl\_alarm](function.pcntl-alarm.html) - Задати таймер доставки сигналу SIGALRM
-   [pcntl\_async\_signals](function.pcntl-async-signals.html) — Увімкнути/вимкнути асинхронну обробку сигналів або отримати поточний статус
-   [pcntl\_errno](function.pcntl-errno.html) - Псевдонім pcntlgetlasterror
-   [pcntl\_exec](function.pcntl-exec.html) — Запустити вказану програму в галузі поточного процесу
-   [pcntl\_fork](function.pcntl-fork.html) - Розгалужити (fork) поточний запущений процес
-   [pcntl\_get\_last\_error](function.pcntl-get-last-error.html) — Отримати код останньої помилки, що виникла у pcntl-функції
-   [pcntl\_getpriority](function.pcntl-getpriority.html) — Отримати значення пріоритету процесу
-   [pcntl\_rfork](function.pcntl-rfork.html) — Взаємодіє із ресурсами процесу
-   [pcntl\_setpriority](function.pcntl-setpriority.html) — Змінити пріоритет процесу
-   [pcntl\_signal\_dispatch](function.pcntl-signal-dispatch.html) — Викликає обробники для сигналів, що очікують.
-   [pcntl\_signal\_get\_handler](function.pcntl-signal-get-handler.html) — Отримати поточний обробник вказаного сигналу
-   [pcntl\_signal](function.pcntl-signal.html) - Встановлення оброблювача сигналу
-   [pcntl\_sigprocmask](function.pcntl-sigprocmask.html) — Задає та витягує список сигналів, що блокуються.
-   [pcntl\_sigtimedwait](function.pcntl-sigtimedwait.html) — Очікує сигнали протягом заданого часу
-   [pcntl\_sigwaitinfo](function.pcntl-sigwaitinfo.html) — Очікування сигналів
-   [pcntl\_strerror](function.pcntl-strerror.html) — Отримати текст помилки за її кодом
-   [pcntl\_unshare](function.pcntl-unshare.html) — Поділяє частини контексту виконання процесу
-   [pcntl\_wait](function.pcntl-wait.html) — Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_waitpid](function.pcntl-waitpid.html) — Очікує чи повертає статус породженого дочірнього процесу
-   [pcntl\_wexitstatus](function.pcntl-wexitstatus.html) — Отримати код повернення завершеного дочірнього процесу
-   [pcntl\_wifexited](function.pcntl-wifexited.html) — Перевіряє, чи код завершення процесу відповідає нормальному завершенню.
-   [pcntl\_wifsignaled](function.pcntl-wifsignaled.html) — Перевірити, чи код завершення процесу завершення по сигналу
-   [pcntl\_wifstopped](function.pcntl-wifstopped.html) — Перевірити, чи зупинено дочірній процес
-   [pcntl\_wstopsig](function.pcntl-wstopsig.html) — Отримати сигнал, через який було зупинено дочірній процес
-   [pcntl\_wtermsig](function.pcntl-wtermsig.html) — Отримати сигнал, через який було примусово завершено дочірній процес