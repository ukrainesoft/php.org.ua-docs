---
navigation:
  - imap.constants.md: « Зумовлені константи
  - function.imap-8bit.md: imap\_8bit »
  - index.md: PHP Manual
  - book.imap.md: IMAP
title: Функції IMAP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції IMAP

# Дивіться також

Цей документ не може вдаватися до деталей усіх питань, порушених представленими функціями. Додаткова інформація представлена ​​в документації клієнтської бібліотеки (docs/internal.txt) та в наступних документах RFC:

-   [» RFC2821](http://www.faqs.org/rfcs/rfc2821) `Simple Mail Transfer Protocol`(SMTP).
-   [» RFC2822](http://www.faqs.org/rfcs/rfc2822) `Standard for ARPA internet text messages`
-   [» RFC2060](http://www.faqs.org/rfcs/rfc2060) `Internet Message Access Protocol`(IMAP) Version 4rev1.
-   [» RFC1939](http://www.faqs.org/rfcs/rfc1939) `Post Office Protocol Version 3`(POP3).
-   [» RFC977](http://www.faqs.org/rfcs/rfc977) `Network News Transfer Protocol`(NNTP).
-   [» RFC2076](http://www.faqs.org/rfcs/rfc2076) `Common Internet Message Headers`
-   [» RFC2045](http://www.faqs.org/rfcs/rfc2045) [» RFC2046](http://www.faqs.org/rfcs/rfc2046) [» RFC2047](http://www.faqs.org/rfcs/rfc2047) [» RFC2048](http://www.faqs.org/rfcs/rfc2048) & [» RFC2049](http://www.faqs.org/rfcs/rfc2049) `Multipurpose Internet Mail Extensions`(MIME).

Детальний опис також доступний у книгах [»`Programming Internet Email`](http://www.oreilly.com/catalog/progintemail/noframes.md) Девіда Вуда (David Wood) та [» Managing IMAP](http://oreilly.com/catalog/9780596000127/) авторів Діани Маллет (Dianna Mullet) та Кевіна Маллет (Kevin Mullet).

## Зміст

-   [imap\_8bit](function.imap-8bit.md)— Конвертує 8-бітовий рядок у рядок у форматі quoted-printable
-   [imap\_alerts](function.imap-alerts.md)— Повертає всі попереджувальні повідомлення IMAP.
-   [imap\_append](function.imap-append.md)— Додає рядкове повідомлення до вказаної поштової скриньки
-   [imap\_base64](function.imap-base64.md) \- Декодує закодований BASE64 текст
-   [imap\_binary](function.imap-binary.md)— Конвертує 8-бітовий рядок у рядок base64
-   [imap\_body](function.imap-body.md)— Читає тіло повідомлення
-   [imap\_bodystruct](function.imap-bodystruct.md)— Читає структуру вказаної секції тіла заданого повідомлення
-   [imap\_check](function.imap-check.md)— Перевіряє поточну поштову скриньку
-   [imap\_clearflag\_full](function.imap-clearflag-full.md)— Знімає з повідомлення встановлені прапори
-   [imap\_close](function.imap-close.md)— Закриває потік IMAP
-   [imap\_create](function.imap-create.md) \- Псевдонім imap\_createmailbox
-   [imap\_createmailbox](function.imap-createmailbox.md)— Створює нову поштову скриньку
-   [imap\_delete](function.imap-delete.md)— Позначає повідомлення для видалення
-   [imap\_deletemailbox](function.imap-deletemailbox.md)— Видаляє поштову скриньку
-   [imap\_errors](function.imap-errors.md)— Отримує всі помилки, що відбулися IMAP
-   [imap\_expunge](function.imap-expunge.md)— Видаляє всі позначені для видалення повідомлення
-   [imap\_fetch\_overview](function.imap-fetch-overview.md)— Оглядає інформацію із заголовків повідомлень
-   [imap\_fetchbody](function.imap-fetchbody.md)— Витягує конкретну секцію тіла повідомлення
-   [imap\_fetchheader](function.imap-fetchheader.md)— Отримує заголовок повідомлення
-   [imap\_fetchmime](function.imap-fetchmime.md)— Витягує MIME-заголовки для конкретного розділу повідомлення
-   [imap\_fetchstructure](function.imap-fetchstructure.md)— Читає структуру вказаного повідомлення
-   [imap\_fetchtext](function.imap-fetchtext.md) \- Псевдонім imap\_body
-   [imap\_gc](function.imap-gc.md)— Очищує кеш IMAP
-   [imap\_get\_quota](function.imap-get-quota.md)— Отримує налаштування рівня квоти та статистику використання поштових скриньок
-   [imap\_get\_quotaroot](function.imap-get-quotaroot.md)— Отримує параметри квоти для кожного користувача
-   [imap\_getacl](function.imap-getacl.md)— Отримує ACL для заданої поштової скриньки
-   [imap\_getmailboxes](function.imap-getmailboxes.md)— Читає список поштових скриньок, повертаючи докладну інформацію щодо кожної з них
-   [imap\_getsubscribed](function.imap-getsubscribed.md)— Отримує список усіх поштових скриньок, на які оформлена передплата
-   [imap\_header](function.imap-header.md) \- Псевдонім imap\_headerinfo
-   [imap\_headerinfo](function.imap-headerinfo.md)— Читає заголовок повідомлення
-   [imap\_headers](function.imap-headers.md)— Отримує заголовки всіх повідомлень у поштовій скриньці
-   [imap\_is\_open](function.imap-is-open.md)— Перевіряє, чи потік IMAP все ще є коректним.
-   [imap\_last\_error](function.imap-last-error.md)— Отримує останню помилку IMAP у поточному запиті
-   [imap\_list](function.imap-list.md)— Читає список поштових скриньок
-   [imap\_listmailbox](function.imap-listmailbox.md) \- Псевдонім imap\_list
-   [imap\_listscan](function.imap-listscan.md)— Отримує список поштових скриньок, імена яких містять заданий рядок
-   [imap\_listsubscribed](function.imap-listsubscribed.md) \- Псевдонім imap\_lsub
-   [imap\_lsub](function.imap-lsub.md)— Отримує список усіх поштових скриньок, на які оформлена передплата
-   [imap\_mail\_compose](function.imap-mail-compose.md)— Створює MIME-повідомлення на основі заданих обгортки та тіла
-   [imap\_mail\_copy](function.imap-mail-copy.md)— Копіює повідомлення у вказану поштову скриньку
-   [imap\_mail\_move](function.imap-mail-move.md)— Переміщує вказані повідомлення до вказаної поштової скриньки
-   [imap\_mail](function.imap-mail.md)— Надсилає повідомлення
-   [imap\_mailboxmsginfo](function.imap-mailboxmsginfo.md)— Отримує інформацію про поточну поштову скриньку
-   [imap\_mime\_header\_decode](function.imap-mime-header-decode.md) \- Декодує елементи заголовка
-   [imap\_msgno](function.imap-msgno.md)— Отримує номер повідомлення із заданим UID
-   [imap\_mutf7\_to\_utf8](function.imap-mutf7-to-utf8.md)— Декодує змінений рядок UTF-7 у UTF-8
-   [imap\_num\_msg](function.imap-num-msg.md)— Отримує кількість повідомлень у поточній поштовій скриньці
-   [imap\_num\_recent](function.imap-num-recent.md)— Отримує кількість нових повідомлень у поточній поштовій скриньці
-   [imap\_open](function.imap-open.md)— Відкриває потік IMAP до поштової скриньки
-   [imap\_ping](function.imap-ping.md)— Перевіряє, чи активний потік IMAP
-   [imap\_qprint](function.imap-qprint.md)— Перетворює рядок із формату quoted-printable на 8-бітовий рядок
-   [imap\_rename](function.imap-rename.md) \- Псевдонім imap\_renamemailbox
-   [imap\_renamemailbox](function.imap-renamemailbox.md)— Перейменовує поштову скриньку
-   [imap\_reopen](function.imap-reopen.md)— Відкриває потік IMAP до нової скриньки
-   [imap\_rfc822\_parse\_adrlist](function.imap-rfc822-parse-adrlist.md)— Розбирає адресний рядок
-   [imap\_rfc822\_parse\_headers](function.imap-rfc822-parse-headers.md)— Розбирає рядок заголовка листа
-   [imap\_rfc822\_write\_address](function.imap-rfc822-write-address.md)— Отримує коректно сформовану адресу електронної пошти, задану ім'ям скриньки, хоста та персональною інформацією
-   [imap\_savebody](function.imap-savebody.md)— Зберігає частину тіла повідомлення у файл
-   [imap\_scan](function.imap-scan.md) \- Псевдонім imap\_listscan
-   [imap\_scanmailbox](function.imap-scanmailbox.md) \- Псевдонім imap\_listscan
-   [imap\_search](function.imap-search.md)— Отримує повідомлення, які відповідають заданим критеріям
-   [imap\_set\_quota](function.imap-set-quota.md)— Встановлює квоту для заданої поштової скриньки
-   [imap\_setacl](function.imap-setacl.md)— Встановлює ACL для заданої поштової скриньки
-   [imap\_setflag\_full](function.imap-setflag-full.md)— Встановлює прапори на повідомлення
-   [imap\_sort](function.imap-sort.md)— Отримує та сортує повідомлення
-   [imap\_status](function.imap-status.md)— Отримує інформацію про статус поштової скриньки
-   [imap\_subscribe](function.imap-subscribe.md)— Підписує на поштову скриньку
-   [imap\_thread](function.imap-thread.md)— Отримує дерево пов'язаних повідомлень
-   [imap\_timeout](function.imap-timeout.md)— Встановлює або отримує час очікування imap
-   [imap\_uid](function.imap-uid.md)— Отримує UID за номером повідомлення
-   [imap\_undelete](function.imap-undelete.md)— Знімає з повідомлення позначку видалення
-   [imap\_unsubscribe](function.imap-unsubscribe.md)— Відписує від поштової скриньки
-   [imap\_utf7\_decode](function.imap-utf7-decode.md)— Декодує рядок із модифікованого кодування UTF-7
-   [imap\_utf7\_encode](function.imap-utf7-encode.md)— Перетворює рядок у кодуванні ISO-8859-1 на модифіковане кодування UTF-7
-   [imap\_utf8\_to\_mutf7](function.imap-utf8-to-mutf7.md)— Кодує рядок UTF-8 у змінений UTF-7
-   [imap\_utf8](function.imap-utf8.md)— Перетворює MIME-кодований текст на UTF-8
