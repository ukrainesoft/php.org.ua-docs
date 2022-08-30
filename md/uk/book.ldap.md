Полегшений протокол доступу до каталогів (LDAP)

-   [« GearmanException](class.gearmanexception.md)
    
-   [Введение »](intro.ldap.md)
    
-   [PHP Manual](index.md)
    
-   [Інші служби](refs.remote.other.md)
    
-   Полегшений протокол доступу до каталогів (LDAP)
    

# Полегшений протокол доступу до каталогів (LDAP)

-   [Введение](intro.ldap.md)
-   [Встановлення та налаштування](ldap.setup.md)
    -   [Вимоги](ldap.requirements.md)
    -   [Установка](ldap.installation.md)
    -   [Налаштування під час виконання](ldap.configuration.md)
    -   [Типи ресурсів](ldap.resources.md)
-   [Обумовлені константи](ldap.constants.md)
-   [Використання дзвінків PHP LDAP](ldap.using.md)
-   [Керуючі об'єкти LDAP](ldap.controls.md)
-   [Приклади](ldap.examples.md)
    -   [Базовое использование](ldap.examples-basic.html)
    -   [LDAP Controls](ldap.examples-controls.html)
-   [Функції LDAP](ref.ldap.md)
    -   [ldapтоt61](function.ldap-8859-to-t61.html) — Перекладає символи з кодування ISO-8859 у t61
    -   [ldapaddext](function.ldap-add-ext.html) — Додати записи до каталогу LDAP
    -   [ldapadd](function.ldap-add.html) — Додати запис до LDAP директорії
    -   [ldapbindext](function.ldap-bind-ext.html) — Прив'язати до директорії LDAP
    -   [ldapbind](function.ldap-bind.html) — Прив'язати до LDAP директорії
    -   [ldapclose](function.ldap-close.html) - Псевдонім ldapunbind
    -   [ldapcompare](function.ldap-compare.html) — Порівняти значення атрибута, знайденого у записі певної DN
    -   [ldapconnect](function.ldap-connect.html) — Підключитись до сервера LDAP
    -   [ldapcontrolpagedresultresponse](function.ldap-control-paged-result-response.html) — Отримати вказівник на поточну сторінку LDAP
    -   [ldapcontrolpagedresult](function.ldap-control-paged-result.html) — Надіслати серверу LDAP дані для використання посторінкового отримання результату
    -   [ldapcountentries](function.ldap-count-entries.html) — Порахувати кількість записів у результатах пошуку
    -   [ldapcountreferences](function.ldap-count-references.html) — Підраховує кількість посилань у результатах пошуку
    -   [ldapdeleteext](function.ldap-delete-ext.html) — Видалити запис із директорії
    -   [ldapdelete](function.ldap-delete.html) — Видаляє запис із директорії LDAP
    -   [ldapdn2ufn](function.ldap-dn2ufn.html) — Перетворити DN на зручний для користувача формат іменування
    -   [ldaperr2str](function.ldap-err2str.html) — Перетворити код помилки LDAP на рядкове повідомлення про помилку
    -   [ldaperrno](function.ldap-errno.html) — Повернути номер помилки LDAP останньої команди
    -   [ldaperror](function.ldap-error.html) — Повернути повідомлення про помилку LDAP останньої команди
    -   [ldapescape](function.ldap-escape.html) — Екранування рядка для використання у фільтрі LDAP або DN
    -   [ldapexoppasswd](function.ldap-exop-passwd.html) — Обгортка для розширеної операції PASSWD
    -   [ldapexoprefresh](function.ldap-exop-refresh.html) — Обгортка для розширеної операції Refresh
    -   [ldapexopwhoami](function.ldap-exop-whoami.html) — Обгортка для розширеної операції WHOAMI
    -   [ldapexop](function.ldap-exop.html) — Виконує розширену операцію
    -   [ldapexplodeдн](function.ldap-explode-dn.html) — Розділити DN на його складові
    -   [ldapfirstattribute](function.ldap-first-attribute.html) - Повернути перший атрибут
    -   [ldapfirstentry](function.ldap-first-entry.html) - Повернути перший ідентифікатор результату
    -   [ldapfirstreference](function.ldap-first-reference.html) - Повертає першу довідку
    -   [ldapfreeresult](function.ldap-free-result.html) - Звільнити пам'ять результату
    -   [ldapgetattributes](function.ldap-get-attributes.html) — Отримує атрибути із запису у результатах пошуку
    -   [ldapgetдн](function.ldap-get-dn.html) — Отримати DN результуючого запису
    -   [ldapgetentries](function.ldap-get-entries.html) — Отримує всі записи результату
    -   [ldapgetoption](function.ldap-get-option.html) — Отримати поточне значення цієї опції
    -   [ldapgetvalueslen](function.ldap-get-values-len.html) — Отримати всі бінарні значення із запису результату
    -   [ldapgetvalues](function.ldap-get-values.html) — Отримує всі значення із запису результату
    -   [ldaplist](function.ldap-list.html) - Однорівневий пошук
    -   [ldapmodaddext](function.ldap-mod_add-ext.html) — Додати значення атрибуту до поточних атрибутів
    -   [ldapmodadd](function.ldap-mod-add.html) — Додати значення атрибуту до поточних атрибутів
    -   [ldapmoddelext](function.ldap-mod_del-ext.html) — Видалити значення атрибутів із поточних атрибутів
    -   [ldapmoddel](function.ldap-mod-del.html) — Видалити атрибути з поточних атрибутів.
    -   [ldapmodreplaceext](function.ldap-mod_replace-ext.html) — Замінити значення атрибута на нові
    -   [ldapmodreplace](function.ldap-mod-replace.html) — Замінити значення атрибутів на нові
    -   [ldapmodifybatch](function.ldap-modify-batch.html) — Формування та запуск пакетної зміни запису LDAP
    -   [ldapmodify](function.ldap-modify.html) - Псевдонім ldapmodreplace
    -   [ldapnextattribute](function.ldap-next-attribute.html) — Отримати наступний атрибут із результату
    -   [ldapnextentry](function.ldap-next-entry.html) — Отримати наступний запис результату
    -   [ldapnextreference](function.ldap-next-reference.html) - Повертає наступну довідку
    -   [ldapparseexop](function.ldap-parse-exop.html) — Розбір результуючого об'єкта виконання розширеної операції LDAP
    -   [ldapparsereference](function.ldap-parse-reference.html) — Витягує інформацію з довідника
    -   [ldapparseresult](function.ldap-parse-result.html) — Витягти інформацію з результату
    -   [ldapread](function.ldap-read.html) - Читає запис
    -   [ldaprenameext](function.ldap-rename-ext.html) — Модифікувати назву запису
    -   [ldaprename](function.ldap-rename.html) - Змінити ім'я запису
    -   [ldapsaslbind](function.ldap-sasl-bind.html) — Прив'язати до LDAP директорії за допомогою SASL
    -   [ldapsearch](function.ldap-search.html) — Пошук по LDAP дереву
    -   [ldapsetoption](function.ldap-set-option.html) — Встановити значення цієї опції
    -   [ldapsetrebindproc](function.ldap-set-rebind-proc.html) — Встановити функцію зворотного дзвінка для повторного зв'язування під час посилального пошуку
    -   [ldapsort](function.ldap-sort.html) — Сортує записи LDAP
    -   [ldapstarttls](function.ldap-start-tls.html) - Запускає TLS
    -   [ldapt61то](function.ldap-t61-to-8859.html) — Переводить символи з кодування t61 ISO-8859
    -   [ldapunbind](function.ldap-unbind.html) — Розірвати прив'язку до директорії LDAP
-   [LDAPConnection](class.ldap-connection.html) - Клас LDAPConnection
-   [LDAPResult](class.ldap-result.html) - Клас LDAPResult
-   [LDAPResultEntry](class.ldap-result-entry.html) - Клас LDAPResultEntry