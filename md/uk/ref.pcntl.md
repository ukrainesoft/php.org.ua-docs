Функції PCNTL

-   [« Базовое применение](pcntl.example.html)
    
-   [pcntlalarm »](function.pcntl-alarm.html)
    
-   [PHP Manual](index.html)
    
-   [PCNTL](book.pcntl.html)
    
-   Функції PCNTL
    

# Функції PCNTL

# Дивіться також

Огляд розділу про [функциях POSIX](ref.posix.html) може бути корисним.

## Зміст

-   [pcntlalarm](function.pcntl-alarm.html) - Задати таймер доставки сигналу SIGALRM
-   [pcntlasyncsignals](function.pcntl-async-signals.html) — Увімкнути/вимкнути асинхронну обробку сигналів або отримати поточний статус
-   [pcntlerrno](function.pcntl-errno.html) - Псевдонім pcntlgetlasterror
-   [pcntlexec](function.pcntl-exec.html) — Запустити вказану програму в галузі поточного процесу
-   [pcntlfork](function.pcntl-fork.html) - Розгалужити (fork) поточний запущений процес
-   [pcntlgetlasterror](function.pcntl-get-last-error.html) — Отримати код останньої помилки, що виникла у pcntl-функції
-   [pcntlgetpriority](function.pcntl-getpriority.html) — Отримати значення пріоритету процесу
-   [pcntlrfork](function.pcntl-rfork.html) — Взаємодіє із ресурсами процесу
-   [pcntlsetpriority](function.pcntl-setpriority.html) — Змінити пріоритет процесу
-   [pcntlsignaldispatch](function.pcntl-signal-dispatch.html) — Викликає обробники для сигналів, що очікують.
-   [pcntlsignalgethandler](function.pcntl-signal-get-handler.html) — Отримати поточний обробник вказаного сигналу
-   [pcntlsignal](function.pcntl-signal.html) - Встановлення оброблювача сигналу
-   [pcntlsigprocmask](function.pcntl-sigprocmask.html) — Задає та витягує список сигналів, що блокуються.
-   [pcntlsigtimedwait](function.pcntl-sigtimedwait.html) — Очікує сигнали протягом заданого часу
-   [pcntlsigwaitinfo](function.pcntl-sigwaitinfo.html) — Очікування сигналів
-   [pcntlstrerror](function.pcntl-strerror.html) — Отримати текст помилки за її кодом
-   [pcntlunshare](function.pcntl-unshare.html) — Поділяє частини контексту виконання процесу
-   [pcntlwait](function.pcntl-wait.html) — Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlwaitpid](function.pcntl-waitpid.html) — Очікує чи повертає статус породженого дочірнього процесу
-   [pcntlwexitstatus](function.pcntl-wexitstatus.html) — Отримати код повернення завершеного дочірнього процесу
-   [pcntlwifexited](function.pcntl-wifexited.html) — Перевіряє, чи код завершення процесу відповідає нормальному завершенню.
-   [pcntlwifsignaled](function.pcntl-wifsignaled.html) — Перевірити, чи код завершення процесу завершення по сигналу
-   [pcntlwifstopped](function.pcntl-wifstopped.html) — Перевірити, чи зупинено дочірній процес
-   [pcntlwstopsig](function.pcntl-wstopsig.html) — Отримати сигнал, через який було зупинено дочірній процес
-   [pcntlwtermsig](function.pcntl-wtermsig.html) — Отримати сигнал, через який було примусово завершено дочірній процес