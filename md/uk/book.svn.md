Subversion

-   [« SVMModel::save](svmmodel.save.html)
    
-   [Введение »](intro.svn.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   Subversion
    

# Subversion

-   [Введение](intro.svn.html)
-   [Установка и настройка](svn.setup.html)
    -   [Требования](svn.requirements.html)
    -   [Установка](svn.installation.html)
    -   [Настройка во время выполнения](svn.configuration.html)
    -   [Типы ресурсов](svn.resources.html)
-   [Предопределённые константы](svn.constants.html)
-   [Функции SVN](ref.svn.html)
    -   [svn\_add](function.svn-add.html) — Додає елементи до списку запланованих для додавання до робочої копії
    -   [svn\_auth\_get\_parameter](function.svn-auth-get-parameter.html) — Повертає параметр автентифікації
    -   [svn\_auth\_set\_parameter](function.svn-auth-set-parameter.html) — Встановлює параметр автентифікації
    -   [svn\_blame](function.svn-blame.html) — Построчно виводить автора та редакцію для файлу
    -   [svn\_cat](function.svn-cat.html) — Повертає вміст файлу у репозиторії
    -   [svn\_checkout](function.svn-checkout.html) — Отримує робочу копію з репозиторію
    -   [svn\_cleanup](function.svn-cleanup.html) — Рекурсивно очищує робочу копію директорії, завершує незакінчені операції та знімає блокування.
    -   [svn\_client\_version](function.svn-client-version.html) — Повертає версію клієнтських бібліотек SVN
    -   [svn\_commit](function.svn-commit.html) — Відправляє зміни з робочої директорії до репозиторію
    -   [svn\_delete](function.svn-delete.html) — Видаляє елементи з робочої копії чи репозиторію.
    -   [svn\_diff](function.svn-diff.html) — Рекурсивно показує різницю двох файлів
    -   [svn\_export](function.svn-export.html) — Експортує вміст директорії SVN
    -   [svn\_fs\_abort\_txn](function.svn-fs-abort-txn.html) - Скасує транзакцію
    -   [svn\_fs\_apply\_text](function.svn-fs-apply-text.html) — Створює та повертає потік, який буде використаний для заміни
    -   [svn\_fs\_begin\_txn2](function.svn-fs-begin-txn2.html) - Створює нову транзакцію
    -   [svn\_fs\_change\_node\_prop](function.svn-fs-change-node-prop.html) — Повертає true, якщо операція пройшла успішно або false чи інакше
    -   [svn\_fs\_check\_path](function.svn-fs-check-path.html) — Визначає, яка сутність знаходиться у дорозі репозиторію fsroot
    -   [svn\_fs\_contents\_changed](function.svn-fs-contents-changed.html) — Повертає true, якщо вміст відрізняється або false, або
    -   [svn\_fs\_copy](function.svn-fs-copy.html) — Копіює файл чи директорію
    -   [svn\_fs\_delete](function.svn-fs-delete.html) — Видаляє файл або директорію
    -   [svn\_fs\_dir\_entries](function.svn-fs-dir-entries.html) - Перераховує елементи директорії по заданому шляху; повертає хеш імен директорій та типів файлів
    -   [svn\_fs\_file\_contents](function.svn-fs-file-contents.html) — Повертає поток для доступу до вмісту файлу з даної файлової системи
    -   [svn\_fs\_file\_length](function.svn-fs-file-length.html) — Повертає довжину файлу з цієї файлової системи
    -   [svn\_fs\_is\_dir](function.svn-fs-is-dir.html) — Чи визначає директорія цим шляхом
    -   [svn\_fs\_is\_file](function.svn-fs-is-file.html) — Визначає, чи знаходиться файл по даному шляху
    -   [svn\_fs\_make\_dir](function.svn-fs-make-dir.html) - Створює нову порожню директорію
    -   [svn\_fs\_make\_file](function.svn-fs-make-file.html) — Створює новий пустий файл
    -   [svn\_fs\_node\_created\_rev](function.svn-fs-node-created-rev.html) — Повертає номер ревізії, коли було створено шлях у файловій системі
    -   [svn\_fs\_node\_prop](function.svn-fs-node-prop.html) — Повертає значення властивості для вузла
    -   [svn\_fs\_props\_changed](function.svn-fs-props-changed.html) — Повертає true, якщо властивості різні або false у противному випадку
    -   [svn\_fs\_revision\_prop](function.svn-fs-revision-prop.html) — Повертає значення цієї властивості
    -   [svn\_fs\_revision\_root](function.svn-fs-revision-root.html) — Повертає дескриптор певної версії кореневої директорії репозиторію.
    -   [svn\_fs\_txn\_root](function.svn-fs-txn-root.html) — Створює та повертає корінь транзакції
    -   [svn\_fs\_youngest\_rev](function.svn-fs-youngest-rev.html) — Повертає номер ранньої ревізії у файловій системі
    -   [svn\_import](function.svn-import.html) — Імпорт шляху без версії до репозиторії
    -   [svn\_log](function.svn-log.html) — Повертає коментарі до правок у репозиторії
    -   [svn\_ls](function.svn-ls.html) — Повертає список вмісту директорії репозиторію URL, опційно для конкретної ревізії
    -   [svn\_mkdir](function.svn-mkdir.html) — Створює директорію у робочій копії чи репозиторії
    -   [svn\_repos\_create](function.svn-repos-create.html) — Створення нового репозиторію Subversion
    -   [svn\_repos\_fs\_begin\_txn\_for\_commit](function.svn-repos-fs-begin-txn-for-commit.html) - Створення нової транзакції
    -   [svn\_repos\_fs\_commit\_txn](function.svn-repos-fs-commit-txn.html) — Відправлення транзакції та повернення номера ревізії
    -   [svn\_repos\_fs](function.svn-repos-fs.html) — Повертає дескриптор файлової системи для репозиторію
    -   [svn\_repos\_hotcopy](function.svn-repos-hotcopy.html) — Створює свіжу копію репозиторію на адресу repospath і копіює в destpath
    -   [svn\_repos\_open](function.svn-repos-open.html) — Відкриває репозиторій із загальним блокуванням
    -   [svn\_repos\_recover](function.svn-repos-recover.html) — Запускає процедури відновлення репозиторію
    -   [svn\_revert](function.svn-revert.html) — Скасує локальні зміни робочої копії
    -   [svn\_status](function.svn-status.html) — Повертає SVN-статус файлів та директорій робочої копії
    -   [svn\_update](function.svn-update.html) — Оновлює робочу копію