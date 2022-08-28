Функції LDAP

-   [« LDAP Controls](ldap.examples-controls.html)
    
-   [ldap\_8859\_to\_t61 »](function.ldap-8859-to-t61.html)
    
-   [PHP Manual](index.html)
    
-   [LDAP](book.ldap.html)
    
-   Функції LDAP
    

# Функції LDAP

## Зміст

-   [ldap\_8859\_to\_t61](function.ldap-8859-to-t61.html) — Перекладає символи з кодування ISO-8859 у t61
-   [ldap\_add\_ext](function.ldap-add-ext.html) — Додати записи до каталогу LDAP
-   [ldap\_add](function.ldap-add.html) — Додати запис до LDAP директорії
-   [ldap\_bind\_ext](function.ldap-bind-ext.html) — Прив'язати до директорії LDAP
-   [ldap\_bind](function.ldap-bind.html) — Прив'язати до LDAP директорії
-   [ldap\_close](function.ldap-close.html) - Псевдонім ldapunbind
-   [ldap\_compare](function.ldap-compare.html) — Порівняти значення атрибута, знайденого у записі певної DN
-   [ldap\_connect](function.ldap-connect.html) — Підключитись до сервера LDAP
-   [ldap\_control\_paged\_result\_response](function.ldap-control-paged-result-response.html) — Отримати вказівник на поточну сторінку LDAP
-   [ldap\_control\_paged\_result](function.ldap-control-paged-result.html) — Надіслати серверу LDAP дані для використання посторінкового отримання результату
-   [ldap\_count\_entries](function.ldap-count-entries.html) — Порахувати кількість записів у результатах пошуку
-   [ldap\_count\_references](function.ldap-count-references.html) — Підраховує кількість посилань у результатах пошуку
-   [ldap\_delete\_ext](function.ldap-delete-ext.html) — Видалити запис із директорії
-   [ldap\_delete](function.ldap-delete.html) — Видаляє запис із директорії LDAP
-   [ldap\_dn2ufn](function.ldap-dn2ufn.html) — Перетворити DN на зручний для користувача формат іменування
-   [ldap\_err2str](function.ldap-err2str.html) — Перетворити код помилки LDAP на рядкове повідомлення про помилку
-   [ldap\_errno](function.ldap-errno.html) — Повернути номер помилки LDAP останньої команди
-   [ldap\_error](function.ldap-error.html) — Повернути повідомлення про помилку LDAP останньої команди
-   [ldap\_escape](function.ldap-escape.html) — Екранування рядка для використання у фільтрі LDAP або DN
-   [ldap\_exop\_passwd](function.ldap-exop-passwd.html) — Обгортка для розширеної операції PASSWD
-   [ldap\_exop\_refresh](function.ldap-exop-refresh.html) — Обгортка для розширеної операції Refresh
-   [ldap\_exop\_whoami](function.ldap-exop-whoami.html) — Обгортка для розширеної операції WHOAMI
-   [ldap\_exop](function.ldap-exop.html) — Виконує розширену операцію
-   [ldap\_explode\_dn](function.ldap-explode-dn.html) — Розділити DN на його складові
-   [ldap\_first\_attribute](function.ldap-first-attribute.html) - Повернути перший атрибут
-   [ldap\_first\_entry](function.ldap-first-entry.html) - Повернути перший ідентифікатор результату
-   [ldap\_first\_reference](function.ldap-first-reference.html) - Повертає першу довідку
-   [ldap\_free\_result](function.ldap-free-result.html) - Звільнити пам'ять результату
-   [ldap\_get\_attributes](function.ldap-get-attributes.html) — Отримує атрибути із запису у результатах пошуку
-   [ldap\_get\_dn](function.ldap-get-dn.html) — Отримати DN результуючого запису
-   [ldap\_get\_entries](function.ldap-get-entries.html) — Отримує всі записи результату
-   [ldap\_get\_option](function.ldap-get-option.html) — Отримати поточне значення цієї опції
-   [ldap\_get\_values\_len](function.ldap-get-values-len.html) — Отримати всі бінарні значення із запису результату
-   [ldap\_get\_values](function.ldap-get-values.html) — Отримує всі значення із запису результату
-   [ldap\_list](function.ldap-list.html) - Однорівневий пошук
-   [ldap\_mod\_add\_ext](function.ldap-mod_add-ext.html) — Додати значення атрибуту до поточних атрибутів
-   [ldap\_mod\_add](function.ldap-mod-add.html) — Додати значення атрибуту до поточних атрибутів
-   [ldap\_mod\_del\_ext](function.ldap-mod_del-ext.html) — Видалити значення атрибутів із поточних атрибутів
-   [ldap\_mod\_del](function.ldap-mod-del.html) — Видалити атрибути з поточних атрибутів.
-   [ldap\_mod\_replace\_ext](function.ldap-mod_replace-ext.html) — Замінити значення атрибута на нові
-   [ldap\_mod\_replace](function.ldap-mod-replace.html) — Замінити значення атрибутів на нові
-   [ldap\_modify\_batch](function.ldap-modify-batch.html) — Формування та запуск пакетної зміни запису LDAP
-   [ldap\_modify](function.ldap-modify.html) - Псевдонім ldapmodreplace
-   [ldap\_next\_attribute](function.ldap-next-attribute.html) — Отримати наступний атрибут із результату
-   [ldap\_next\_entry](function.ldap-next-entry.html) — Отримати наступний запис результату
-   [ldap\_next\_reference](function.ldap-next-reference.html) - Повертає наступну довідку
-   [ldap\_parse\_exop](function.ldap-parse-exop.html) — Розбір результуючого об'єкта виконання розширеної операції LDAP
-   [ldap\_parse\_reference](function.ldap-parse-reference.html) — Витягує інформацію з довідника
-   [ldap\_parse\_result](function.ldap-parse-result.html) — Витягти інформацію з результату
-   [ldap\_read](function.ldap-read.html) - Читає запис
-   [ldap\_rename\_ext](function.ldap-rename-ext.html) — Модифікувати назву запису
-   [ldap\_rename](function.ldap-rename.html) - Змінити ім'я запису
-   [ldap\_sasl\_bind](function.ldap-sasl-bind.html) — Прив'язати до LDAP директорії за допомогою SASL
-   [ldap\_search](function.ldap-search.html) — Пошук по LDAP дереву
-   [ldap\_set\_option](function.ldap-set-option.html) — Встановити значення цієї опції
-   [ldap\_set\_rebind\_proc](function.ldap-set-rebind-proc.html) — Встановити функцію зворотного дзвінка для повторного зв'язування під час посилального пошуку
-   [ldap\_sort](function.ldap-sort.html) — Сортує записи LDAP
-   [ldap\_start\_tls](function.ldap-start-tls.html) - Запускає TLS
-   [ldap\_t61\_to\_8859](function.ldap-t61-to-8859.html) — Перекладає символи з кодування t61 ISO-8859
-   [ldap\_unbind](function.ldap-unbind.html) — Розірвати прив'язку до директорії LDAP