IMAP, POP3 та NNTP

-   [« Модули для работы с почтой](refs.remote.mail.html)
    
-   [Введение »](intro.imap.html)
    
-   [PHP Manual](index.html)
    
-   [Модули для работы с почтой](refs.remote.mail.html)
    
-   IMAP, POP3 та NNTP
    

# IMAP, POP3 та NNTP

-   [Введение](intro.imap.html)
-   [Установка и настройка](imap.setup.html)
    -   [Требования](imap.requirements.html)
    -   [Установка](imap.installation.html)
    -   [Настройка во время выполнения](imap.configuration.html)
    -   [Типы ресурсов](imap.resources.html)
-   [Предопределённые константы](imap.constants.html)
-   [Функции IMAP](ref.imap.html)
    -   [imap\_8bit](function.imap-8bit.html) — Конвертує 8-бітний рядок у рядок у форматі quoted-printable
    -   [imap\_alerts](function.imap-alerts.html) — Повертає всі попереджувальні повідомлення IMAP.
    -   [imap\_append](function.imap-append.html) — Додає рядкове повідомлення до вказаної поштової скриньки
    -   [imap\_base64](function.imap-base64.html) — Декодувати текст закодований BASE64
    -   [imap\_binary](function.imap-binary.html) — Конвертує 8-бітовий рядок у рядок base64
    -   [imap\_body](function.imap-body.html) — Прочитати тіло повідомлення
    -   [imap\_bodystruct](function.imap-bodystruct.html) — Прочитати структуру вказаної секції тіла заданого повідомлення
    -   [imap\_check](function.imap-check.html) — Перевірити поточну поштову скриньку
    -   [imap\_clearflag\_full](function.imap-clearflag-full.html) — Зняти з повідомлення встановлені прапори
    -   [imap\_close](function.imap-close.html) — Закрити потік IMAP
    -   [imap\_create](function.imap-create.html) - Псевдонім imapcreatemailbox
    -   [imap\_createmailbox](function.imap-createmailbox.html) — Створити нову поштову скриньку
    -   [imap\_delete](function.imap-delete.html) — Позначити повідомлення для видалення
    -   [imap\_deletemailbox](function.imap-deletemailbox.html) — Видалити поштову скриньку
    -   [imap\_errors](function.imap-errors.html) — Отримати всі помилки, що відбулися IMAP
    -   [imap\_expunge](function.imap-expunge.html) — Видалити всі позначені для видалення повідомлення
    -   [imap\_fetch\_overview](function.imap-fetch-overview.html) — Огляд інформації, що міститься в заголовках повідомлень
    -   [imap\_fetchbody](function.imap-fetchbody.html) — Витягти конкретну секцію тіла повідомлення
    -   [imap\_fetchheader](function.imap-fetchheader.html) — Отримати назву повідомлення
    -   [imap\_fetchmime](function.imap-fetchmime.html) — Вийняти MIME-заголовки для конкретного розділу повідомлення
    -   [imap\_fetchstructure](function.imap-fetchstructure.html) — Прочитати структуру вказаного повідомлення
    -   [imap\_fetchtext](function.imap-fetchtext.html) - Псевдонім imapbody
    -   [imap\_gc](function.imap-gc.html) — Очистити кеш IMAP
    -   [imap\_get\_quota](function.imap-get-quota.html) — Отримати налаштування рівня квоти та статистику використання поштових скриньок
    -   [imap\_get\_quotaroot](function.imap-get-quotaroot.html) — Отримати параметри квоти для кожного користувача
    -   [imap\_getacl](function.imap-getacl.html) — Отримати ACL для заданої поштової скриньки
    -   [imap\_getmailboxes](function.imap-getmailboxes.html) — Прочитати список поштових скриньок, повертаючи докладну інформацію щодо кожної з них
    -   [imap\_getsubscribed](function.imap-getsubscribed.html) — Список усіх поштових скриньок, на які ви підписані
    -   [imap\_header](function.imap-header.html) - Псевдонім imapheaderinfo
    -   [imap\_headerinfo](function.imap-headerinfo.html) — Прочитати заголовок повідомлення
    -   [imap\_headers](function.imap-headers.html) — Отримати заголовки всіх повідомлень у поштовій скриньці
    -   [imap\_last\_error](function.imap-last-error.html) — Отримати останню помилку IMAP у поточному запиті
    -   [imap\_list](function.imap-list.html) — Прочитати список поштових скриньок
    -   [imap\_listmailbox](function.imap-listmailbox.html) - Псевдонім imaplist
    -   [imap\_listscan](function.imap-listscan.html) — Отримати список поштових скриньок, імена яких містять заданий рядок
    -   [imap\_listsubscribed](function.imap-listsubscribed.html) - Псевдонім imaplsub
    -   [imap\_lsub](function.imap-lsub.html) — Список усіх підписаних поштових скриньок
    -   [imap\_mail\_compose](function.imap-mail-compose.html) — Створити MIME-повідомлення на основі заданих обгортки та тіла
    -   [imap\_mail\_copy](function.imap-mail-copy.html) — Копіювати повідомлення до вказаної поштової скриньки
    -   [imap\_mail\_move](function.imap-mail-move.html) — Перемістити вказані повідомлення до вказаної поштової скриньки
    -   [imap\_mail](function.imap-mail.html) — Надіслати email
    -   [imap\_mailboxmsginfo](function.imap-mailboxmsginfo.html) — Отримати інформацію про поточну поштову скриньку
    -   [imap\_mime\_header\_decode](function.imap-mime-header-decode.html) - Декодувати елементи заголовка
    -   [imap\_msgno](function.imap-msgno.html) — Отримати номер повідомлення із заданим UID
    -   [imap\_mutf7\_to\_utf8](function.imap-mutf7-to-utf8.html) — Декодувати змінений рядок UTF-7 у UTF-8
    -   [imap\_num\_msg](function.imap-num-msg.html) — Отримати кількість повідомлень у поточній поштовій скриньці
    -   [imap\_num\_recent](function.imap-num-recent.html) — Отримати кількість нових повідомлень у поточній поштовій скриньці
    -   [imap\_open](function.imap-open.html) — Відкриває потік IMAP до поштової скриньки
    -   [imap\_ping](function.imap-ping.html) — Перевірити, чи активний потік IMAP
    -   [imap\_qprint](function.imap-qprint.html) — Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок
    -   [imap\_rename](function.imap-rename.html) - Псевдонім imaprenamemailbox
    -   [imap\_renamemailbox](function.imap-renamemailbox.html) — Перейменувати поштову скриньку
    -   [imap\_reopen](function.imap-reopen.html) — Відкриває потік IMAP до нової скриньки
    -   [imap\_rfc822\_parse\_adrlist](function.imap-rfc822-parse-adrlist.html) - Розбір адресного рядка
    -   [imap\_rfc822\_parse\_headers](function.imap-rfc822-parse-headers.html) - Розбір рядка заголовка листа
    -   [imap\_rfc822\_write\_address](function.imap-rfc822-write-address.html) — Отримати коректно сформовану e-mail адресу, задану ім'ям скриньки, хоста та персональною інформацією
    -   [imap\_savebody](function.imap-savebody.html) — Зберегти частину тіла повідомлення у файл
    -   [imap\_scan](function.imap-scan.html) - Псевдонім imaplistscan
    -   [imap\_scanmailbox](function.imap-scanmailbox.html) - Псевдонім imaplistscan
    -   [imap\_search](function.imap-search.html) — Отримати повідомлення, які відповідають заданим критеріям
    -   [imap\_set\_quota](function.imap-set-quota.html) — Встановити квоту для заданої поштової скриньки
    -   [imap\_setacl](function.imap-setacl.html) — Встановлення ACL для заданої поштової скриньки
    -   [imap\_setflag\_full](function.imap-setflag-full.html) — Встановити прапори на повідомлення
    -   [imap\_sort](function.imap-sort.html) — Отримати та відсортувати повідомлення
    -   [imap\_status](function.imap-status.html) — Отримати інформацію про статус поштової скриньки
    -   [imap\_subscribe](function.imap-subscribe.html) — Передплатити поштову скриньку
    -   [imap\_thread](function.imap-thread.html) — Отримати дерево пов'язаних повідомлень
    -   [imap\_timeout](function.imap-timeout.html) — Встановити або отримати час очікування imap
    -   [imap\_uid](function.imap-uid.html) — Отримати UID за номером повідомлення
    -   [imap\_undelete](function.imap-undelete.html) — Знімає з повідомлення позначку видалення
    -   [imap\_unsubscribe](function.imap-unsubscribe.html) — Відписатися від поштової скриньки
    -   [imap\_utf7\_decode](function.imap-utf7-decode.html) — Декодує рядок із модифікованого кодування UTF-7
    -   [imap\_utf7\_encode](function.imap-utf7-encode.html) — Перетворює рядок ISO-8859-1 на модифікований UTF-7
    -   [imap\_utf8\_to\_mutf7](function.imap-utf8-to-mutf7.html) — Кодувати рядок UTF-8 у змінений UTF-7
    -   [imap\_utf8](function.imap-utf8.html) — Перетворює MIME-кодований текст на UTF-8
-   [IMAP\\Connection](class.imap-connection.html) - Клас IMAPConnection