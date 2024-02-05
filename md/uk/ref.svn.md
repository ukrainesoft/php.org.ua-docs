---
navigation:
  - svn.constants.md: « Зумовлені константи
  - function.svn-add.md: svn\_add »
  - index.md: PHP Manual
  - book.svn.md: SVN
title: Функції SVN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції SVN

## Зміст

-   [svn\_add](function.svn-add.md)— Додає елементи до списку запланованих для додавання до робочої копії
-   [svn\_auth\_get\_parameter](function.svn-auth-get-parameter.md)— Повертає параметр автентифікації
-   [svn\_auth\_set\_parameter](function.svn-auth-set-parameter.md)— Встановлює параметр автентифікації
-   [svn\_blame](function.svn-blame.md)— Построчно виводить автора та редакцію для файлу
-   [svn\_cat](function.svn-cat.md)— Повертає вміст файлу у репозиторії
-   [svn\_checkout](function.svn-checkout.md)— Отримує робочу копію з репозиторію
-   [svn\_cleanup](function.svn-cleanup.md)— Рекурсивно очищує робочу копію директорії, завершує незакінчені операції та знімає блокування.
-   [svn\_client\_version](function.svn-client-version.md)— Повертає версію клієнтських бібліотек SVN
-   [svn\_commit](function.svn-commit.md)— Відправляє зміни з робочої директорії до репозиторію
-   [svn\_delete](function.svn-delete.md)— Видаляє елементи з робочої копії або репозиторію
-   [svn\_diff](function.svn-diff.md)— Рекурсивно показує різницю двох файлів
-   [svn\_export](function.svn-export.md)— Експортує вміст директорії SVN
-   [svn\_fs\_abort\_txn](function.svn-fs-abort-txn.md) \- Скасує транзакцію
-   [svn\_fs\_apply\_text](function.svn-fs-apply-text.md)— Створює та повертає потік, який буде використаний для заміни
-   [svn\_fs\_begin\_txn2](function.svn-fs-begin-txn2.md) \- Створює нову транзакцію
-   [svn\_fs\_change\_node\_prop](function.svn-fs-change-node-prop.md)— Повертає true, якщо операція пройшла успішно або false чи інакше
-   [svn\_fs\_check\_path](function.svn-fs-check-path.md)— Визначає, яка сутність знаходиться у дорозі репозиторію fsroot
-   [svn\_fs\_contents\_changed](function.svn-fs-contents-changed.md)— Повертає true, якщо вміст відрізняється або false, або
-   [svn\_fs\_copy](function.svn-fs-copy.md)— Копіює файл чи директорію
-   [svn\_fs\_delete](function.svn-fs-delete.md)— Видаляє файл або директорію
-   [svn\_fs\_dir\_entries](function.svn-fs-dir-entries.md) \- Перераховує елементи директорії по заданому шляху; повертає хеш імен директорій та типів файлів
-   [svn\_fs\_file\_contents](function.svn-fs-file-contents.md)— Повертає поток для доступу до вмісту файлу з даної файлової системи
-   [svn\_fs\_file\_length](function.svn-fs-file-length.md)— Повертає довжину файлу з цієї файлової системи
-   [svn\_fs\_is\_dir](function.svn-fs-is-dir.md)— Чи визначає директорія цим шляхом
-   [svn\_fs\_is\_file](function.svn-fs-is-file.md)— Визначає, чи знаходиться файл по даному шляху
-   [svn\_fs\_make\_dir](function.svn-fs-make-dir.md) \- Створює нову порожню директорію
-   [svn\_fs\_make\_file](function.svn-fs-make-file.md)— Створює новий пустий файл
-   [svn\_fs\_node\_created\_rev](function.svn-fs-node-created-rev.md)— Повертає номер ревізії, коли було створено шлях у файловій системі
-   [svn\_fs\_node\_prop](function.svn-fs-node-prop.md)— Повертає значення властивості для вузла
-   [svn\_fs\_props\_changed](function.svn-fs-props-changed.md)— Повертає true, якщо властивості різні або false у противному випадку
-   [svn\_fs\_revision\_prop](function.svn-fs-revision-prop.md)— Повертає значення цієї властивості
-   [svn\_fs\_revision\_root](function.svn-fs-revision-root.md)— Повертає дескриптор певної версії кореневої директорії репозиторію.
-   [svn\_fs\_txn\_root](function.svn-fs-txn-root.md)— Створює та повертає корінь транзакції
-   [svn\_fs\_youngest\_rev](function.svn-fs-youngest-rev.md)— Повертає номер найранішої ревізії у файловій системі
-   [svn\_import](function.svn-import.md)— Імпорт шляху без версії до репозиторії
-   [svn\_log](function.svn-log.md)— Повертає коментарі до правок у репозиторії
-   [svn\_ls](function.svn-ls.md)— Повертає список вмісту директорії репозиторію URL, опційно для конкретної ревізії
-   [svn\_mkdir](function.svn-mkdir.md)— Створює директорію у робочій копії чи репозиторії
-   [svn\_repos\_create](function.svn-repos-create.md)— Створення нового репозиторію Subversion
-   [svn\_repos\_fs\_begin\_txn\_for\_commit](function.svn-repos-fs-begin-txn-for-commit.md) \- Створення нової транзакції
-   [svn\_repos\_fs\_commit\_txn](function.svn-repos-fs-commit-txn.md)— Відправлення транзакції та повернення номера ревізії
-   [svn\_repos\_fs](function.svn-repos-fs.md)— Повертає дескриптор файлової системи для репозиторію
-   [svn\_repos\_hotcopy](function.svn-repos-hotcopy.md)— Створює свіжу копію репозиторію на адресу repospath і копіює в destpath
-   [svn\_repos\_open](function.svn-repos-open.md)— Відкриває репозиторій із загальним блокуванням
-   [svn\_repos\_recover](function.svn-repos-recover.md)— Запускає процедури відновлення репозиторію
-   [svn\_revert](function.svn-revert.md)— Скасує локальні зміни робочої копії
-   [svn\_status](function.svn-status.md)— Повертає SVN-статус файлів та директорій робочої копії
-   [svn\_update](function.svn-update.md)— Оновлює робочу копію
