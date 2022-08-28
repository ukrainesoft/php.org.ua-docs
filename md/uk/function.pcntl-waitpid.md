Очікує чи повертає статус породженого дочірнього процесу

-   [« pcntl\_wait](function.pcntl-wait.html)
    
-   [pcntl\_wexitstatus »](function.pcntl-wexitstatus.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Очікує чи повертає статус породженого дочірнього процесу
    

# pcntlwaitpid

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

pcntlwaitpid — Очікує чи повертає статус породженого дочірнього процесу

### Опис

```methodsynopsis
pcntl_waitpid(    int $process_id,    int &$status,    int $flags = 0,    array &$resource_usage = []): int
```

Функція очікування призупиняє виконання поточного процесу доти, доки дочірній процес, зазначений у аргументі `process_id`, не завершиться або доки не буде отримано сигнал, який завершує поточний процес або викликає функцію обробки сигналу.

Якщо дочірній процес, зазначений у аргументі `process_id`, вже завершився до часу виклику (так звані "зомбі" процеси), функція негайно поверне управління. Будь-які системні ресурси, що використовуються дочірнім процесом, будуть звільнені. Зверніться до вашого системного посібника waitpid(2) для уточнення специфіки роботи waitpid у вашій системі.

### Список параметрів

`process_id`

Аргумент `process_id` може приймати одне з наступних значень:

<table class="doctable table"><caption><strong>можливі значення аргументу <code class="parameter">process_id</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">&lt; -1</code></td><td>очікувати будь-який дочірній процес, у якого значення ідентифікатора групи процесів (group ID) дорівнює модулю значення аргументу |<code class=" parameter">process_id</code>|.</td></tr><tr><td><code class="literal">-1</code></td><td>очікувати будь-який дочірній процес; це така ж поведінка, що й у функції wait. ідентифікатор групи процесів (group ID) якого дорівнює ідентифікатору поточного процесу.</td><td>очікувати процес ID якого дорівнює <code class="parameter">process_id</code>.</td></tr></tbody></table>

> **Зауваження**
> 
> Вказівка `-1` в якості `process_id` - це аналог функції [pcntl\_wait()](function.pcntl-wait.html) (мінус `flags`

`status`

**pcntlwaitpid()** розмістить інформацію про статус за посиланням у аргументі `status`, який може бути переданий у такі функції: [pcntl\_wifexited()](function.pcntl-wifexited.html) [pcntl\_wifstopped()](function.pcntl-wifstopped.html) [pcntl\_wifsignaled()](function.pcntl-wifsignaled.html) [pcntl\_wexitstatus()](function.pcntl-wexitstatus.html) [pcntl\_wtermsig()](function.pcntl-wtermsig.html) і [pcntl\_wstopsig()](function.pcntl-wstopsig.html)

`flags`

Значення аргументу `flags` - це бітова маска, яка може набувати значення нуль або більше шляхом логічного об'єднання наступних констант:

<table class="doctable table"><caption><strong>Можливі значення для <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">WNOHANG</code></td><td>Негайно повернути управління, якщо жоден з дочірніх процесів не завершено</td></tr><tr><td>&lt; code class="literal"&gt;WUNTRACED</td><td>Повернути управління для зупинених дочірніх процесів, про статус яких ще не повідомлено</td></tr></tbody></table>

### Значення, що повертаються

[pcntl\_wait()](function.pcntl-wait.html) повертає ID завершеного дочірнього процесу, -1 у разі виникнення помилки або нуль, якщо **`WNOHANG`** було передано в аргумент `flags` і не було доступних дочірніх процесів.

### Дивіться також

-   [pcntl\_fork()](function.pcntl-fork.html) - Розгалужити (fork) поточний запущений процес
-   [pcntl\_signal()](function.pcntl-signal.html) - Встановлення оброблювача сигналу
-   [pcntl\_wifexited()](function.pcntl-wifexited.html) - Перевіряє, чи код завершення процесу відповідає нормальному завершенню
-   [pcntl\_wifstopped()](function.pcntl-wifstopped.html) - Перевірити, чи зупинено дочірній процес
-   [pcntl\_wifsignaled()](function.pcntl-wifsignaled.html) - Перевірити, чи код завершення процесу завершення по сигналу
-   [pcntl\_wexitstatus()](function.pcntl-wexitstatus.html) - Отримати код повернення завершеного дочірнього процесу
-   [pcntl\_wtermsig()](function.pcntl-wtermsig.html) - Отримати сигнал, через який було примусово завершено дочірній процес
-   [pcntl\_wstopsig()](function.pcntl-wstopsig.html) - Отримати сигнал, через який було зупинено дочірній процес