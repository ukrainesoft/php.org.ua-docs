Функції SVN

-   [« Обумовлені константи](svn.constants.html)
    
-   [svnadd »](function.svn-add.html)
    
-   [PHP Manual](index.html)
    
-   [SVN](book.svn.html)
    
-   Функції SVN
    

# Функції SVN

## Зміст

-   [svnadd](function.svn-add.html) — Додає елементи до списку запланованих для додавання до робочої копії
-   [svnauthgetparameter](function.svn-auth-get-parameter.html) — Повертає параметр автентифікації
-   [svnauthsetparameter](function.svn-auth-set-parameter.html) — Встановлює параметр автентифікації
-   [svnblame](function.svn-blame.html) — Построчно виводить автора та редакцію для файлу
-   [svncat](function.svn-cat.html) — Повертає вміст файлу у репозиторії
-   [svncheckout](function.svn-checkout.html) — Отримує робочу копію з репозиторію
-   [svncleanup](function.svn-cleanup.html) — Рекурсивно очищує робочу копію директорії, завершує незакінчені операції та знімає блокування.
-   [svnclientversion](function.svn-client-version.html) — Повертає версію клієнтських бібліотек SVN
-   [svncommit](function.svn-commit.html) — Відправляє зміни з робочої директорії до репозиторію
-   [svndelete](function.svn-delete.html) — Видаляє елементи з робочої копії або репозиторію
-   [svndiff](function.svn-diff.html) — Рекурсивно показує різницю двох файлів
-   [svnexport](function.svn-export.html) — Експортує вміст директорії SVN
-   [svnфсaborttxn](function.svn-fs-abort-txn.html) - Скасує транзакцію
-   [svnфсapplytext](function.svn-fs-apply-text.html) — Створює та повертає потік, який буде використаний для заміни
-   [svnфсbegintxn2](function.svn-fs-begin-txn2.html) - Створює нову транзакцію
-   [svnфсchangenodeprop](function.svn-fs-change-node-prop.html) — Повертає true, якщо операція пройшла успішно або false чи інакше
-   [svnфсcheckpath](function.svn-fs-check-path.html) — Визначає, яка сутність знаходиться у дорозі репозиторію fsroot
-   [svnфсcontentschanged](function.svn-fs-contents-changed.html) — Повертає true, якщо вміст відрізняється або false, або
-   [svnфсcopy](function.svn-fs-copy.html) — Копіює файл чи директорію
-   [svnфсdelete](function.svn-fs-delete.html) — Видаляє файл або директорію
-   [svnфсdirentries](function.svn-fs-dir-entries.html) - Перераховує елементи директорії по заданому шляху; повертає хеш імен директорій та типів файлів
-   [svnфсfilecontents](function.svn-fs-file-contents.html) — Повертає поток для доступу до вмісту файлу з даної файлової системи
-   [svnфсfilelength](function.svn-fs-file-length.html) — Повертає довжину файлу з цієї файлової системи
-   [svnфсісdir](function.svn-fs-is-dir.html) — Чи визначає директорія цим шляхом
-   [svnфсісfile](function.svn-fs-is-file.html) — Визначає, чи знаходиться файл по даному шляху
-   [svnфсmakedir](function.svn-fs-make-dir.html) - Створює нову порожню директорію
-   [svnфсmakefile](function.svn-fs-make-file.html) — Створює новий пустий файл
-   [svnфсnodecreatedrev](function.svn-fs-node-created-rev.html) — Повертає номер ревізії, коли було створено шлях у файловій системі
-   [svnфсnodeprop](function.svn-fs-node-prop.html) — Повертає значення властивості для вузла
-   [svnфсpropschanged](function.svn-fs-props-changed.html) — Повертає true, якщо властивості різні або false у противному випадку
-   [svnфсrevisionprop](function.svn-fs-revision-prop.html) — Повертає значення цієї властивості
-   [svnфсrevisionroot](function.svn-fs-revision-root.html) — Повертає дескриптор певної версії кореневої директорії репозиторію.
-   [svnфсtxnroot](function.svn-fs-txn-root.html) — Створює та повертає корінь транзакції
-   [svnфсyoungestrev](function.svn-fs-youngest-rev.html) — Повертає номер ранньої ревізії у файловій системі
-   [svnimport](function.svn-import.html) — Імпорт шляху без версії до репозиторії
-   [svnlog](function.svn-log.html) — Повертає коментарі до правок у репозиторії
-   [svnлс](function.svn-ls.html) — Повертає список вмісту директорії репозиторію URL, опційно для конкретної ревізії
-   [svnmkdir](function.svn-mkdir.html) — Створює директорію у робочій копії чи репозиторії
-   [svnreposcreate](function.svn-repos-create.html) — Створення нового репозиторію Subversion
-   [svnreposфсbegintxnforcommit](function.svn-repos-fs-begin-txn-for-commit.html) - Створення нової транзакції
-   [svnreposфсcommittxn](function.svn-repos-fs-commit-txn.html) — Відправлення транзакції та повернення номера ревізії
-   [svnreposфс](function.svn-repos-fs.html) — Повертає дескриптор файлової системи для репозиторію
-   [svnreposhotcopy](function.svn-repos-hotcopy.html) — Створює свіжу копію репозиторію на адресу repospath і копіює в destpath
-   [svnreposopen](function.svn-repos-open.html) — Відкриває репозиторій із загальним блокуванням
-   [svnreposrecover](function.svn-repos-recover.html) — Запускає процедури відновлення репозиторію
-   [svnrevert](function.svn-revert.html) — Скасує локальні зміни робочої копії
-   [svnstatus](function.svn-status.html) — Повертає SVN-статус файлів та директорій робочої копії
-   [svnupdate](function.svn-update.html) — Оновлює робочу копію