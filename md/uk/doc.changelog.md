---
navigation:
  - indexes.examples.md: « Список примеров
  - index.md: PHP Manual
  - appendices.md: Appendices
title: список змін
---
# список змін

Наступні зміни були здійснені з функціями вбудованих модулів.

| Version | Function | Description |
| --- | --- | --- |
| PECL OCI8 1.4 | [ocisetprefetch](function.oci-set-prefetch.md) | До цієї версії rows мав бути >=1. |
| PECL OCI8 1.3.4 | [ocisetprefetch](function.oci-set-prefetch.md) | До цієї версії попередня вибірка була обмежена до меншого зі значень рядків рядків і 1024 rows байт. Тепер обмеження за розміром байт знято. |
| PECL 3.0.0 | [IntlDateFormatter::format](intldateformatter.format.md) | Додано підтримку надання об'єктів IntlCalendar для параметра datetime. |
|  | [DateInterval::construct](dateinterval.construct.md) | Буде видно тільки y в f, invert і days, включаючи нову логічну властивість fromstring. |
|  | [DateInterval::createFromDateString](dateinterval.createfromdatestring.md) | Тільки властивості fromstring та datestring буде видно при створенні об'єкта DateInterval за допомогою цього методу. |
|  | [DateTimeInterface::format](datetime.format.md) | Додані символи форматування X та x. |
|  | [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md) | Додані специфікатори X та x параметру format. |
|  | [idate](function.idate.md) | Додані символи для параметра format: N (День тижня ISO-8601) та o (Рік ISO-8601). |
|  | [utf8decode](function.utf8-decode.md) | Функцію оголошено застарілою. |
|  | [utf8encode](function.utf8-encode.md) | Ця функція має бути неперевіреною. |
|  | [DateTime::setTime](datetime.settime.md) | Поведінка з подвійним існуючим годинником (під час переходу на літній час) змінилася. Раніше PHP вибирав друге входження (після переходу на літній час), а не перше (до переходу на літній час). |
|  | [DateTimeImmutable::setTime](datetimeimmutable.settime.md) | Поведінка з подвоєнням існуючого годинника (під час резервного переходу на літній час) змінилася. Раніше PHP вибирав друге входження (після переходу на літній час) замість першого входження (до переходу на літній час). |
|  | [DirectoryIterator::key](directoryiterator.key.md) | Якщо ітератор не ініціалізований, викидається помилка Error. Раніше метод повертав false. |
|  | [DOMDocument::createComment](domdocument.createcomment.md) | У разі помилки тепер викидає виняток DomException. Раніше натомість поверталося значення false. |
|  | [DOMDocument::createDocumentFragment](domdocument.createdocumentfragment.md) | У разі помилки тепер викидає виняток DomException. Раніше натомість поверталося значення false. |
|  | [DOMDocument::createTextNode](domdocument.createtextnode.md) | У разі помилки тепер викидає виняток DomException. Раніше натомість поверталося значення false. |
|  | [current](function.current.md) | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію getmangledobjectvars, або використовуйте ArrayIterator. |
|  | [datesunrise](function.date-sunrise.md) | Функція оголошена застарілою, використовуйте разом її datesuninfo. |
|  | [datesunset](function.date-sunset.md) | Функція оголошена застарілою, використовуйте разом її datesuninfo. |
|  | [end](function.end.md) | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію getmangledobjectvars, або використовуйте ArrayIterator. |
|  | [finfobuffer](function.finfo-buffer.md) | Параметр finfo тепер чекає на екземпляр finfo; раніше очікували ресурс (resource). |
|  | [finfoclose](function.finfo-close.md) | Параметр finfo тепер чекає на екземпляр finfo; раніше очікували ресурс (resource). |
|  | [finfofile](function.finfo-file.md) | Параметр finfo тепер чекає на екземпляр finfo; раніше очікували ресурс (resource). |
|  | [finfoopen](function.finfo-open.md) | Повертає екземпляр finfo; раніше повертався ресурс (resource). |
|  | [finfosetflags](function.finfo-set-flags.md) | Параметр finfo тепер чекає на екземпляр finfo; раніше очікували ресурс (resource). |
|  | [fputcsv](function.fputcsv.md) | Додано необов'язковий параметр eol. |
|  | [ftpalloc](function.ftp-alloc.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpappend](function.ftp-append.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpcdup](function.ftp-cdup.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpchdir](function.ftp-chdir.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpchmod](function.ftp-chmod.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpclose](function.ftp-close.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpconnect](function.ftp-connect.md) | Повертає екземпляр FTPConnection; раніше повертався ресурс (resource). |
|  | [ftpdelete](function.ftp-delete.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpexec](function.ftp-exec.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpfget](function.ftp-fget.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpfput](function.ftp-fput.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpget](function.ftp-get.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpgetoption](function.ftp-get-option.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftplogin](function.ftp-login.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpmdtm](function.ftp-mdtm.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpmkdir](function.ftp-mkdir.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpmlsd](function.ftp-mlsd.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpнбcontinue](function.ftp-nb-continue.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpнбfget](function.ftp-nb-fget.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpнбfput](function.ftp-nb-fput.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpнбget](function.ftp-nb-get.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpнбput](function.ftp-nb-put.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpnlist](function.ftp-nlist.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftppasv](function.ftp-pasv.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpput](function.ftp-put.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftppwd](function.ftp-pwd.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpraw](function.ftp-raw.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftprawlist](function.ftp-rawlist.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftprename](function.ftp-rename.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftprmdir](function.ftp-rmdir.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpsetoption](function.ftp-set-option.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpsite](function.ftp-site.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpsize](function.ftp-size.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [ftpsslconnect](function.ftp-ssl-connect.md) | Повертає екземпляр FTPConnection; раніше повертався ресурс (resource). |
|  | [ftpsystype](function.ftp-systype.md) | Параметр ftp тепер чекає на екземпляр FTPConnection; раніше очікували ресурс (resource). |
|  | [gethtmltranslationtable](function.get-html-translation-table.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [hash](function.hash.md) | Доданий параметр options. |
|  | [hashalgos](function.hash-algos.md) | Додано підтримку алгоритмів MurmurHash3 і xxHash. |
|  | [hashfile](function.hash-file.md) | Доданий параметр options. |
|  | [hashinit](function.hash-init.md) | Доданий параметр options. |
|  | [htmlentitydecode](function.html-entity-decode.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlentities](function.htmlentities.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlspecialchars](function.htmlspecialchars.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlspecialcharsdecode](function.htmlspecialchars-decode.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [imagechar](function.imagechar.md) | Параметр font тепер приймає як екземпляр GdFont, і ціле число (int); раніше приймалося лише ціле число (int). |
|  | [imagecharup](function.imagecharup.md) | Параметр font тепер приймає як екземпляр GdFont, і ціле число (int); раніше приймалося лише ціле число (int). |
|  | [imagefilledpolygon](function.imagefilledpolygon.md) | Параметр numpoints оголошено застарілим. |
|  | [imagefontheight](function.imagefontheight.md) | Параметр font тепер приймає як екземпляр GdFont, і ціле число (int); раніше приймалося лише ціле число (int). |
|  | [imagefontwidth](function.imagefontwidth.md) | Параметр font тепер приймає як екземпляр GdFont, і ціле число (int); раніше приймалося лише ціле число (int). |
|  | [imageloadfont](function.imageloadfont.md) | Повертає екземпляр GdFont; раніше поверталося ціле число (int). |
|  | [imageopenpolygon](function.imageopenpolygon.md) | Параметр numpoints оголошено застарілим. |
|  | [imagepolygon](function.imagepolygon.md) | Параметр numpoints оголошено застарілим. |
|  | [imagestring](function.imagestring.md) | Параметр font тепер приймає як екземпляр GdFont, і ціле число (int); раніше приймалося лише ціле число (int). |
|  | [imagestringup](function.imagestringup.md) | Параметр font тепер приймає як екземпляр GdFont, і ціле число (int); раніше приймалося лише ціле число (int). |
|  | [imagetypes](function.imagetypes.md) | Додано константу IMGAVIF. |
|  | [imapappend](function.imap-append.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapbody](function.imap-body.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapbodystruct](function.imap-bodystruct.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapcheck](function.imap-check.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapclearflagfull](function.imap-clearflag-full.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapclose](function.imap-close.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapcreatemailbox](function.imap-createmailbox.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapdelete](function.imap-delete.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapdeletemailbox](function.imap-deletemailbox.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapexpunge](function.imap-expunge.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapfetchoverview](function.imap-fetch-overview.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapfetchbody](function.imap-fetchbody.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapfetchheader](function.imap-fetchheader.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapfetchmime](function.imap-fetchmime.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapfetchstructure](function.imap-fetchstructure.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapгк](function.imap-gc.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapgetquota](function.imap-get-quota.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapgetquotaroot](function.imap-get-quotaroot.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapgetacl](function.imap-getacl.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapgetmailboxes](function.imap-getmailboxes.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapgetsubscribed](function.imap-getsubscribed.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapheaderinfo](function.imap-headerinfo.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapheaders](function.imap-headers.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imaplist](function.imap-list.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imaplistscan](function.imap-listscan.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imaplsub](function.imap-lsub.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapmailcopy](function.imap-mail-copy.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapmailmove](function.imap-mail-move.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapmailboxmsginfo](function.imap-mailboxmsginfo.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapmsgno](function.imap-msgno.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapnummsg](function.imap-num-msg.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapnumrecent](function.imap-num-recent.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapopen](function.imap-open.md) | Повертає екземпляр IMAPConnection; раніше повертався ресурс (resource). |
|  | [imapping](function.imap-ping.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imaprenamemailbox](function.imap-renamemailbox.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapreopen](function.imap-reopen.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsavebody](function.imap-savebody.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsearch](function.imap-search.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsetquota](function.imap-set-quota.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsetacl](function.imap-setacl.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsetflagfull](function.imap-setflag-full.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsort](function.imap-sort.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapstatus](function.imap-status.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapsubscribe](function.imap-subscribe.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapthread](function.imap-thread.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapuid](function.imap-uid.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapundelete](function.imap-undelete.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [imapunsubscribe](function.imap-unsubscribe.md) | Параметр imap тепер чекає на екземпляр IMAPConnection; раніше очікували ресурс (resource). |
|  | [iniset](function.ini-set.md) | Параметр value тепер приймає будь-який скалярний тип (включаючи null). Раніше допускалися лише строкові (string) значення. |
|  | [key](function.key.md) | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію getmangledobjectvars, або використовуйте ArrayIterator. |
|  | [ldapadd](function.ldap-add.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapaddext](function.ldap-add-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapaddext](function.ldap-add-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapbind](function.ldap-bind.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapbindext](function.ldap-bind-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapbindext](function.ldap-bind-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapcompare](function.ldap-compare.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapconnect](function.ldap-connect.md) | Повертає екземпляр LDAPConnection; раніше повертався ресурс (resource). |
|  | [ldapcountentries](function.ldap-count-entries.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapcountentries](function.ldap-count-entries.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapcountreferences](function.ldap-count-references.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapcountreferences](function.ldap-count-references.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapdelete](function.ldap-delete.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapdeleteext](function.ldap-delete-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapdeleteext](function.ldap-delete-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldaperrno](function.ldap-errno.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldaperror](function.ldap-error.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapexop](function.ldap-exop.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapexoppasswd](function.ldap-exop-passwd.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapexoprefresh](function.ldap-exop-refresh.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapexopwhoami](function.ldap-exop-whoami.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapfirstattribute](function.ldap-first-attribute.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldapfirstattribute](function.ldap-first-attribute.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapfirstentry](function.ldap-first-entry.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapfirstentry](function.ldap-first-entry.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapfirstentry](function.ldap-first-entry.md) | Повертає екземпляр LDAPResultEntry; раніше повертався ресурс (resource). |
|  | [ldapfreeresult](function.ldap-free-result.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapgetattributes](function.ldap-get-attributes.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapgetattributes](function.ldap-get-attributes.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldapgetдн](function.ldap-get-dn.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldapgetдн](function.ldap-get-dn.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapgetentries](function.ldap-get-entries.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapgetentries](function.ldap-get-entries.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapgetoption](function.ldap-get-option.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapgetvalues](function.ldap-get-values.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapgetvalues](function.ldap-get-values.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldapgetvalueslen](function.ldap-get-values-len.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapgetvalueslen](function.ldap-get-values-len.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldaplist](function.ldap-list.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldaplist](function.ldap-list.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapmodadd](function.ldap-mod-add.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmoddel](function.ldap-mod-del.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmodreplace](function.ldap-mod-replace.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmodifybatch](function.ldap-modify-batch.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmodaddext](function.ldap-mod_add-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapmodaddext](function.ldap-mod_add-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmoddelext](function.ldap-mod_del-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmoddelext](function.ldap-mod_del-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapmodreplaceext](function.ldap-mod_replace-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapmodreplaceext](function.ldap-mod_replace-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapnextattribute](function.ldap-next-attribute.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldapnextattribute](function.ldap-next-attribute.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapnextentry](function.ldap-next-entry.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapnextentry](function.ldap-next-entry.md) | Параметр entry тепер чекає на екземпляр LDAPResultEntry; раніше очікували ресурс (resource). |
|  | [ldapnextentry](function.ldap-next-entry.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapparseexop](function.ldap-parse-exop.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapparseexop](function.ldap-parse-exop.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapparseresult](function.ldap-parse-result.md) | Параметр result тепер чекає на екземпляр LDAPResult; раніше очікували ресурс (resource). |
|  | [ldapparseresult](function.ldap-parse-result.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapread](function.ldap-read.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapread](function.ldap-read.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldaprename](function.ldap-rename.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldaprenameext](function.ldap-rename-ext.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldaprenameext](function.ldap-rename-ext.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapsaslbind](function.ldap-sasl-bind.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapsearch](function.ldap-search.md) | Повертає екземпляр LDAPResult; раніше повертався ресурс (resource). |
|  | [ldapsearch](function.ldap-search.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapsetoption](function.ldap-set-option.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapsetrebindproc](function.ldap-set-rebind-proc.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [ldapunbind](function.ldap-unbind.md) | Параметр ldap тепер чекає на екземпляр LDAPConnection; раніше очікували ресурс (resource). |
|  | [mhash](function.mhash.md) | Функцію оголошено застарілою. Використовуйте замість неї функції hash |
|  | [mhashcount](function.mhash-count.md) | Функцію оголошено застарілою. Використовуйте замість неї функції hash |
|  | [mhashgetblocksize](function.mhash-get-block-size.md) | Функцію оголошено застарілою. Використовуйте замість неї функції hash |
|  | [mhashgethashname](function.mhash-get-hash-name.md) | Функцію оголошено застарілою. Використовуйте замість неї функції hash |
|  | [mhashkeygens2k](function.mhash-keygen-s2k.md) | Функцію оголошено застарілою. Використовуйте замість неї функції hash |
|  | [next](function.next.md) | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію getmangledobjectvars, або використовуйте ArrayIterator. |
|  | [odbcresultall](function.odbc-result-all.md) | Функцію оголошено застарілою. |
|  | [opensslcmsencrypt](function.openssl-cms-encrypt.md) | Алгоритм шифрування за промовчанням (cipheralgo) тепер AES-128-CBC (OPENSSLCIPHERAESCBC). Раніше використовувався алгоритм PKCS7/CMS (OPENSSLCIPHERRC2 |
|  | [openssldecrypt](function.openssl-decrypt.md) | Параметр tag тепер припускає значення null. |
|  | [opensslpkcs7encrypt](function.openssl-pkcs7-encrypt.md) | Алгоритм шифрування за промовчанням (cipheralgo) тепер AES-128-CBC (OPENSSLCIPHERAESCBC). Раніше використовувався алгоритм PKCS7/CMS (OPENSSLCIPHERRC2 |
|  | [пгaffectedrows](function.pg-affected-rows.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгcancelquery](function.pg-cancel-query.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгclientencoding](function.pg-client-encoding.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгclose](function.pg-close.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгconnect](function.pg-connect.md) | Повертає екземпляр PgSqlConnection; раніше повертався ресурс (resource). |
|  | [пгconnectpoll](function.pg-connect-poll.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгconnectionbusy](function.pg-connection-busy.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгconnectionreset](function.pg-connection-reset.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгconnectionstatus](function.pg-connection-status.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгconsumeinput](function.pg-consume-input.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгconvert](function.pg-convert.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгcopyfrom](function.pg-copy-from.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгcopyто](function.pg-copy-to.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгdbname](function.pg-dbname.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгdelete](function.pg-delete.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгendcopy](function.pg-end-copy.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгescapebytea](function.pg-escape-bytea.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгescapeidentifier](function.pg-escape-identifier.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгescapeliteral](function.pg-escape-literal.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгescapestring](function.pg-escape-string.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгexecute](function.pg-execute.md) | Повертає екземпляр PgSqlResult; раніше повертався ресурс (resource). |
|  | [пгexecute](function.pg-execute.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгfetchall](function.pg-fetch-all.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfetchallcolumns](function.pg-fetch-all-columns.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfetcharray](function.pg-fetch-array.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfetchassoc](function.pg-fetch-assoc.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfetchobject](function.pg-fetch-object.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfetchresult](function.pg-fetch-result.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfetchrow](function.pg-fetch-row.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldісnull](function.pg-field-is-null.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldname](function.pg-field-name.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldnum](function.pg-field-num.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldprtlen](function.pg-field-prtlen.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldsize](function.pg-field-size.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldtable](function.pg-field-table.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldtype](function.pg-field-type.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгfieldtypeoid](function.pg-field-type-oid.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгflush](function.pg-flush.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгfreeresult](function.pg-free-result.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгgetnotify](function.pg-get-notify.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгgetpid](function.pg-get-pid.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгgetresult](function.pg-get-result.md) | Повертає екземпляр PgSqlResult; раніше повертався ресурс (resource). |
|  | [пгgetresult](function.pg-get-result.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгhost](function.pg-host.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгinsert](function.pg-insert.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгinsert](function.pg-insert.md) | Повертає екземпляр PgSqlResult; раніше повертався ресурс (resource). |
|  | [пгlasterror](function.pg-last-error.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгlastnotice](function.pg-last-notice.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгlastoid](function.pg-last-oid.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пглоclose](function.pg-lo-close.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пглоcreate](function.pg-lo-create.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пглоexport](function.pg-lo-export.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пглоimport](function.pg-lo-import.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пглоopen](function.pg-lo-open.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пглоopen](function.pg-lo-open.md) | Повертає екземпляр PgSqlLob; раніше повертався ресурс (resource). |
|  | [пглоread](function.pg-lo-read.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пглоreadall](function.pg-lo-read-all.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пглоseek](function.pg-lo-seek.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пглоtell](function.pg-lo-tell.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пглоtruncate](function.pg-lo-truncate.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пглоunlink](function.pg-lo-unlink.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пглоwrite](function.pg-lo-write.md) | Параметр lob тепер чекає на екземпляр PgSqlLob; раніше очікували ресурс (resource). |
|  | [пгmetadata](function.pg-meta-data.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгnumfields](function.pg-num-fields.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгnumrows](function.pg-num-rows.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгoptions](function.pg-options.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгparameterstatus](function.pg-parameter-status.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгpconnect](function.pg-pconnect.md) | Повертає екземпляр PgSqlConnection; раніше повертався ресурс (resource). |
|  | [пгping](function.pg-ping.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгport](function.pg-port.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгprepare](function.pg-prepare.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгprepare](function.pg-prepare.md) | Повертає екземпляр PgSqlResult; раніше повертався ресурс (resource). |
|  | [пгputline](function.pg-put-line.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгquery](function.pg-query.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгquery](function.pg-query.md) | Повертає екземпляр PgSqlResult; раніше повертався ресурс (resource). |
|  | [пгqueryparams](function.pg-query-params.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгqueryparams](function.pg-query-params.md) | Повертає екземпляр PgSqlResult; раніше повертався ресурс (resource). |
|  | [пгresulterror](function.pg-result-error.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгresulterrorfield](function.pg-result-error-field.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгresultseek](function.pg-result-seek.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгresultstatus](function.pg-result-status.md) | Параметр result тепер чекає на екземпляр PgSqlResult; раніше очікували ресурс (resource). |
|  | [пгselect](function.pg-select.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгsendexecute](function.pg-send-execute.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгsendprepare](function.pg-send-prepare.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгsendquery](function.pg-send-query.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгsendqueryparams](function.pg-send-query-params.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгsetclientencoding](function.pg-set-client-encoding.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгseterrorverbosity](function.pg-set-error-verbosity.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгsocket](function.pg-socket.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгtrace](function.pg-trace.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгtransactionstatus](function.pg-transaction-status.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгtty](function.pg-tty.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгuntrace](function.pg-untrace.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгupdate](function.pg-update.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [пгversion](function.pg-version.md) | Параметр connection тепер чекає на екземпляр PgSqlConnection; раніше очікували ресурс (resource). |
|  | [prev](function.prev.md) | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію getmangledobjectvars, або використовуйте ArrayIterator. |
|  | [pspelladdтоpersonal](function.pspell-add-to-personal.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [pspelladdтоsession](function.pspell-add-to-session.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [pspellcheck](function.pspell-check.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [pspellclearsession](function.pspell-clear-session.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [pspellconfigcreate](function.pspell-config-create.md) | Повертає екземпляр PSpellConfig; раніше повертався ресурс (resource). |
|  | [pspellconfigdatadir](function.pspell-config-data-dir.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigdictdir](function.pspell-config-dict-dir.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigignore](function.pspell-config-ignore.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigmode](function.pspell-config-mode.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigpersonal](function.pspell-config-personal.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigrepl](function.pspell-config-repl.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigruntogether](function.pspell-config-runtogether.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellconfigsaverepl](function.pspell-config-save-repl.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellnew](function.pspell-new.md) | Повертає екземпляр PSpellDictionary; раніше повертався ресурс (resource). |
|  | [pspellnewconfig](function.pspell-new-config.md) | Параметр config тепер чекає на екземпляр PSpellConfig; раніше очікували ресурс (resource). |
|  | [pspellnewconfig](function.pspell-new-config.md) | Повертає екземпляр PSpellDictionary; раніше повертався ресурс (resource). |
|  | [pspellnewpersonal](function.pspell-new-personal.md) | Повертає екземпляр PSpellDictionary; раніше повертався ресурс (resource). |
|  | [pspellsavewordlist](function.pspell-save-wordlist.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [pspellstorereplacement](function.pspell-store-replacement.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [pspellsuggest](function.pspell-suggest.md) | Параметр dictionary тепер чекає екземпляр PSpellDictionary; раніше очікували ресурс (resource). |
|  | [reset](function.reset.md) | Виклик функції в об'єкті (object) оголошено застарілим. Або спочатку використовуйте для об'єкта (object) функцію getmangledobjectvars, або використовуйте ArrayIterator. |
|  | [snmpv3get](function.snmp3-get.md) | Параметр authprotocol тепер приймає "SHA256" та "SHA512", якщо підтримується libnetsnmp. |
|  | [snmpv3getnext](function.snmp3-getnext.md) | Параметр authprotocol тепер приймає "SHA256" та "SHA512", якщо підтримується libnetsnmp. |
|  | [snmpv3realwalk](function.snmp3-real-walk.md) | Параметр authprotocol тепер приймає "SHA256" та "SHA512", якщо підтримується libnetsnmp. |
|  | [snmpv3walk](function.snmp3-walk.md) | Параметр authprotocol тепер приймає "SHA256" та "SHA512", якщо підтримується libnetsnmp. |
|  | [streamselect](function.stream-select.md) | Параметр microseconds тепер допускає значення null. |
|  | [strptime](function.strptime.md) | Функцію оголошено застарілою. Замість неї використовуйте dateparsefromformat (для синтаксичного аналізу, який не залежить від мовного стандарту) або IntlDateFormatter::parse (для синтаксичного аналізу, що залежить від мовного стандарту). |
|  | [MultipleIterator::current](multipleiterator.current.md) | Тепер викидається виняток RuntimeException, якщо MultipleIterator::key викликається на неприпустимому ітераторі. Раніше натомість поверталося значення false. |
|  | [MultipleIterator::key](multipleiterator.key.md) | Тепер викидається виняток RuntimeException, якщо MultipleIterator::key викликається на неприпустимому ітераторі. Раніше натомість поверталося значення false. |
|  | [mysqlidriver::$reportmode](mysqli-driver.report-mode.md) | Тепер за замовчуванням встановлено значення MYSQLIREPORTERROR |
|  | [mysqliresult::fetchall](mysqli-result.fetch-all.md) | Тепер також доступно при збиранні з libmysqlclient. |
|  | [mysqlistmt::execute](mysqli-stmt.execute.md) | Додано необов'язковий параметр params. |
|  | [mysqlistmt::nextresult](mysqli-stmt.next-result.md) | Тепер також доступно при збиранні з libmysqlclient. |
|  | [mysqli::$clientinfo](mysqli.get-client-info.md) | Об'єктно-орієнтований стиль виклику методу mysqli::getclientinfo застарів. |
|  | [mysqli::$clientinfo](mysqli.get-client-info.md) | Виклик функції mysqligetclientinfo з аргументом mysql застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
|  | [mysqli::init](mysqli.init.md) | Об'єктно-орієнтований стиль виклику методу mysqli::init застарів. Замініть виклик методу parent::init за допомогою parent::construct. |
|  | [Phar::buildFromDirectory](phar.buildfromdirectory.md) | Phar::buildFromDirectory більше не повертає значення false. |
|  | [Phar::buildFromIterator](phar.buildfromiterator.md) | Phar::buildFromIterator більше не повертає значення false. |
|  | [PharData::buildFromDirectory](phardata.buildfromdirectory.md) | PharData::buildFromDirectory більше не повертає значення false. |
|  | [PharData::buildFromIterator](phardata.buildfromiterator.md) | PharData::buildFromIterator більше не повертає значення false. |
|  | [ReflectionClassConstant::getName](reflectionclassconstant.getname.md) | Викидає помилку Error у випадку, якщо властивість name не була ініціалізована. Раніше, у разі помилки, метод повертав false. |
|  | [ReflectionExtension::clone](reflectionextension.clone.md) | Метод не є остаточним (final). |
|  | [ReflectionFunctionAbstract::clone](reflectionfunctionabstract.clone.md) | Метод не є остаточним (final). |
|  | [ReflectionParameter::clone](reflectionparameter.clone.md) | Метод не є остаточним (final). |
|  | [ReflectionProperty::clone](reflectionproperty.clone.md) | Метод не є остаточним (final). |
|  | [ReflectionZendExtension::clone](reflectionzendextension.clone.md) | Метод не є остаточним (final). |
|  | [SplFileObject::fputcsv](splfileobject.fputcsv.md) | Додано необов'язковий параметр eol. |
|  | [SplObjectStorage::current](splobjectstorage.current.md) | Метод SplObjectStorage::current тепер викидає виняток Error, якщо ця позиція неприпустима. Раніше натомість поверталося значення false. |
|  | [imageinterlace](function.imageinterlace.md) | imageinterlace тепер повертає логічне значення (bool); раніше вона повертала ціле число (int). (Ненульове значення для зображень з інтерлейсингом, інакше - нуль). |
|  | [DOMDocument::getElementsByTagNameNS](domdocument.getelementsbytagnamens.md) | namespace тепер допускає значення null. |
|  | [DOMElement::getElementsByTagNameNS](domelement.getelementsbytagnamens.md) | namespace тепер допускає значення null. |
|  | [DOMImplementation::createDocument](domimplementation.createdocument.md) | namespace тепер допускає значення null. |
|  | [finfo::construct](finfo.construct.md) | magicDatabase тепер допускає значення null. |
|  | [bindtextdomaincodeset](function.bind-textdomain-codeset.md) | codeset тепер допускає значення null. Раніше було неможливо отримати поточне встановлене кодування. |
|  | [bindtextdomain](function.bindtextdomain.md) | directory тепер допускає значення null. Раніше неможливо було отримати поточний встановлений каталог. |
|  | [finfoopen](function.finfo-open.md) | magicDatabase тепер допускає значення null. |
|  | [imagegd](function.imagegd.md) | file тепер припускає значення null. |
|  | [imagegd2](function.imagegd2.md) | file тепер припускає значення null. |
|  | [SoapClient::setLocation](soapclient.setlocation.md) | location тепер допускає значення null. |
|  | [SoapVar::construct](soapvar.construct.md) | typeName, typeNamespace, nodeName та nodeNamespace тепер допускають значення null. |
| 8.0.0, PECL OCI8 3.0.0 | [ociconnect](function.oci-connect.md) | connectionstring тепер допускає значення null. |
|  | [ocierror](function.oci-error.md) | connectionорstatement тепер допускає значення null. |
|  | [ocilobcopy](function.oci-lob-copy.md) | length тепер припускає значення null. |
|  | [ocinewcollection](function.oci-new-collection.md) | schema тепер допускає значення null. |
|  | [ocinewconnect](function.oci-new-connect.md) | connectionstring тепер допускає значення null. |
|  | [OCICollection::append](ocicollection.append.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::assign](ocicollection.assign.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::assignElem](ocicollection.assignelem.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::free](ocicollection.free.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::getElem](ocicollection.getelem.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::max](ocicollection.max.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::size](ocicollection.size.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCICollection::trim](ocicollection.trim.md) | Клас OCI-Collection перейменований на OCICollection відповідно до стандартів іменування PHP. |
|  | [OCILob::append](ocilob.append.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::close](ocilob.close.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::eof](ocilob.eof.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::erase](ocilob.erase.md) | offset і length тепер допускають значення null. |
|  | [OCILob::erase](ocilob.erase.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::export](ocilob.export.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::export](ocilob.export.md) | offset і length тепер допускають значення null. |
|  | [OCILob::flush](ocilob.flush.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::free](ocilob.free.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::getBuffering](ocilob.getbuffering.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::import](ocilob.import.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::load](ocilob.load.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::read](ocilob.read.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::rewind](ocilob.rewind.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::save](ocilob.save.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::saveFile](ocilob.savefile.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::seek](ocilob.seek.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::setBuffering](ocilob.setbuffering.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::size](ocilob.size.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::tell](ocilob.tell.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::truncate](ocilob.truncate.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::write](ocilob.write.md) | length тепер припускає значення null. |
|  | [OCILob::write](ocilob.write.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::writeTemporary](ocilob.writetemporary.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [OCILob::writeToFile](ocilob.writetofile.md) | offset і length тепер допускають значення null. |
|  | [OCILob::writeToFile](ocilob.writetofile.md) | Клас OCI-Lob перейменований на OCILob відповідно до стандартів іменування PHP. |
|  | [ZipArchive::addGlob](ziparchive.addglob.md) | Додані параметри "compметод", "compflags", "encmethod" та "encpassword" в options. |
|  | [ZipArchive::addEmptyDir](ziparchive.addemptydir.md) | Додано параметр flags. |
|  | [ZipArchive::addFile](ziparchive.addfile.md) | Додано параметр flags. |
|  | [ZipArchive::addFromString](ziparchive.addfromstring.md) | Додано параметр flags. |
|  | [ZipArchive::addGlob](ziparchive.addglob.md) | Доданий параметр "flags" у options. |
|  | [ZipArchive::getStatusString](ziparchive.getstatusstring.md) | Метод більше не повертає false у разі виникнення помилки. |
|  | [ZipArchive::getStatusString](ziparchive.getstatusstring.md) | Метод можна викликати у закритому архіві. |
|  | [CURLFile::construct](curlfile.construct.md) | mimetype і postedfilename тепер допускають значення null; раніше значенням за промовчанням був 0. |
|  | [DateInterval::construct](dateinterval.construct.md) | W тепер може використовуватися разом із D. |
|  | [DateTimeInterface::format](datetime.format.md) | До цієї версії у разі виникнення помилки поверталося false. |
|  | [DateTimeInterface::format](datetime.format.md) | Доданий символ форматування p. |
|  | [DateTimeInterface::getOffset](datetime.getoffset.md) | До цієї версії у разі виникнення помилки поверталося false. |
|  | [DateTimeInterface::getTimestamp](datetime.gettimestamp.md) | Функції більше не повертають false у разі виникнення помилки. |
|  | [DateTimeZone::getOffset](datetimezone.getoffset.md) | До цієї версії у разі виникнення помилки поверталося false. |
|  | [DateTimeZone::listIdentifiers](datetimezone.listidentifiers.md) | До цієї версії у разі виникнення помилки поверталося false. |
|  | [Directory::close](directory.close.md) | Настройки не приймаються. Раніше як аргумент можна було передати дескриптор каталогу. |
|  | [Directory::read](directory.read.md) | Настройки не приймаються. Раніше як аргумент можна було передати дескриптор каталогу. |
|  | [Directory::rewind](directory.rewind.md) | Настройки не приймаються. Раніше як аргумент можна було передати дескриптор каталогу. |
|  | [DirectoryIterator::construct](directoryiterator.construct.md) | Тепер викидає виняток ValueError, якщо параметр directory містить порожній рядок; Раніше викидався виняток RuntimeException. |
|  | [DOMImplementation::createDocument](domimplementation.createdocument.md) | doctype тепер допускає значення null. |
|  | [FFI::cdef](ffi.cdef.md) | lib тепер припускає значення null. |
|  | [FFI::string](ffi.string.md) | size тепер припускає значення null; раніше значенням за замовчуванням було 0. |
|  | [FilesystemIterator::construct](filesystemiterator.construct.md) | Тепер викидає виняток ValueError, якщо параметр directory містить порожній рядок; Раніше викидався виняток RuntimeException. |
|  | [abs](function.abs.md) | num більше не приймає внутрішні об'єкти, що підтримують числове перетворення. |
|  | [apachenote](function.apache-note.md) | notevalue тепер допускає значення null. |
|  | [arraychunk](function.array-chunk.md) | Якщо параметр length менше 1, буде викинуто виняток ValueError; раніше, натомість видавалася помилка рівня EWARNING та функція повертала null. |
|  | [arraycolumn](function.array-column.md) | Об'єкти в стовпцях, позначені параметром indexkey, більше не будуть перетворені на рядок і замість цього будуть видавати TypeError. |
|  | [arraycombine](function.array-combine.md) | Функція arraycombine тепер викидає помилку ValueError, якщо кількість елементів у масивах не збігається; раніше функція повертала значення false. |
|  | [arraydiff](function.array-diff.md) | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |
|  | [arraydiffassoc](function.array-diff-assoc.md) | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |
|  | [arraydiffkey](function.array-diff-key.md) | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |
|  | [arrayfill](function.array-fill.md) | Функція arrayfill тепер викидає виняток ValueError, якщо параметр count виходить межі діапазону; раніше видавалась помилка рівня EWARNING, а функція повертала значення false. |
|  | [arrayfilter](function.array-filter.md) | callback тепер допускає значення null. |
|  | [arrayfilter](function.array-filter.md) | Якщо параметр callback очікує, що буде передано значення посилання, функція тепер видасть помилку рівня EWARNING. |
|  | [arrayintersect](function.array-intersect.md) | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |
|  | [arrayintersectassoc](function.array-intersect-assoc.md) | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |
|  | [arrayintersectkey](function.array-intersect-key.md) | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |
|  | [arraymap](function.array-map.md) | Якщо параметр callback очікує, що буде передано значення посилання, функція тепер видасть помилку рівня EWARNING. |
|  | [arrayreduce](function.array-reduce.md) | Якщо параметр callback очікує, що буде передано значення посилання, функція тепер видасть помилку рівня EWARNING. |
|  | [arraysplice](function.array-splice.md) | length тепер припускає значення null. |
|  | [arraywalk](function.array-walk.md) | Якщо параметр callback очікує, що значення другого або третього параметра буде передано за посиланням, тепер функція видасть помилку рівня EWARNING. |
|  | [assert](function.assert.md) | Функція assert більше не оцінюватиме рядкові аргументи, натомість вони розглядатимуться як будь-який інший аргумент. Замість assert($a == $b) слід використовувати assert('$a == $b'). Директива assert.quieteval php.ini та константа ASSERTQUIETEVAL також були видалені, оскільки вони не мають сенсу. |
|  | [assert](function.assert.md) | Оголошення функції з іменем assert() всередині простору імен тепер заборонено та викликає ECOMPILEERROR. |
|  | [bcadd](function.bcadd.md) | scale тепер допускає значення null. |
|  | [bccomp](function.bccomp.md) | scale тепер допускає значення null. |
|  | [bcdiv](function.bcdiv.md) | scale тепер допускає значення null. |
|  | [bcmod](function.bcmod.md) | scale тепер допускає значення null. |
|  | [bcmul](function.bcmul.md) | scale тепер допускає значення null. |
|  | [bcpowmod](function.bcpowmod.md) | scale тепер допускає значення null. |
|  | [bcscale](function.bcscale.md) | scale is now nullable. |
|  | [bcsqrt](function.bcsqrt.md) | scale тепер допускає значення null. |
|  | [bcsub](function.bcsub.md) | scale тепер допускає значення null. |
|  | [bzdecompress](function.bzdecompress.md) | Тип uselessmemory змінено з int на bool. Раніше значенням за промовчанням був 0. |
|  | [bzwrite](function.bzwrite.md) | length тепер припускає значення null. |
|  | [calluserfuncarray](function.call-user-func-array.md) | Ключі параметра args тепер інтерпретуються як імена параметрів, а чи не ігноруються. |
|  | [ceil](function.ceil.md) | num більше не приймає внутрішні об'єкти, що підтримують числове перетворення. |
|  | [comeventsink](function.com-event-sink.md) | sinkinterface тепер допускає значення null. |
|  | [comgetactiveobject](function.com-get-active-object.md) | codepage тепер допускає значення null. |
|  | [constant](function.constant.md) | Якщо константа не визначена, функція constant тепер викидає виняток Error; раніше видавалась помилка рівня EWARNING та поверталося значення null. |
|  | [convertuuencode](function.convert-uuencode.md) | До цієї версії при спробі перетворити порожній рядок поверталося false без особливих причин. |
|  | [count](function.count.md) | count тепер викидає TypeError, якщо передано неприпустимий обчислюваний тип параметр value. |
|  | [countchars](function.count-chars.md) | До цієї версії функція повертала false у разі виникнення помилки. |
|  | [crypt](function.crypt.md) | salt більше не є необов'язковим. |
|  | [curlclose](function.curl-close.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlcopyhandle](function.curl-copy-handle.md) | У разі успішного виконання повертає екземпляр CurlHandle; раніше повертався ресурс (resource). |
|  | [curlcopyhandle](function.curl-copy-handle.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlerrno](function.curl-errno.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlerror](function.curl-error.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlescape](function.curl-escape.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlexec](function.curl-exec.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlgetinfo](function.curl-getinfo.md) | option is nullable now; previously, the default був 0. |
|  | [curlgetinfo](function.curl-getinfo.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlinit](function.curl-init.md) | url тепер припускає значення null. |
|  | [curlinit](function.curl-init.md) | У разі успішного виконання повертає екземпляр CurlHandle; раніше, повертався ресурс (resource). |
|  | [curlmultiaddhandle](function.curl-multi-add-handle.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultiaddhandle](function.curl-multi-add-handle.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlmulticlose](function.curl-multi-close.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultierrno](function.curl-multi-errno.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [curlmultierrno](function.curl-multi-errno.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultiexec](function.curl-multi-exec.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultigetcontent](function.curl-multi-getcontent.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlmultiinforead](function.curl-multi-info-read.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultiinit](function.curl-multi-init.md) | У разі успішного виконання повертає екземпляр CurlMultiHandle; раніше, повертався ресурс (resource). |
|  | [curlmultiremovehandle](function.curl-multi-remove-handle.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultiremovehandle](function.curl-multi-remove-handle.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlmultiselect](function.curl-multi-select.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlmultisetopt](function.curl-multi-setopt.md) | multihandle тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | [curlpause](function.curl-pause.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlreset](function.curl-reset.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlsetopt](function.curl-setopt.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlsetoptarray](function.curl-setopt-array.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlshareclose](function.curl-share-close.md) | sharehandle expects на CurlShareHandle instance now; Попередньо, як ресурс був виявлений. |
|  | [curlshareerrno](function.curl-share-errno.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [curlshareerrno](function.curl-share-errno.md) | sharehandle expects на CurlShareHandle instance now; Попередньо, як ресурс був виявлений. |
|  | [curlshareinit](function.curl-share-init.md) | Функція повертає екземпляр CurlShareHandle; раніше, повертався ресурс (resource). |
|  | [curlsharesetopt](function.curl-share-setopt.md) | sharehandle expects на CurlShareHandle instance now; Попередньо, як ресурс був виявлений. |
|  | [curlunescape](function.curl-unescape.md) | handle тепер чекає екземпляр CurlHandle; раніше, очікувався ресурс (resource). |
|  | [curlversion](function.curl-version.md) | Необов'язковий параметр age видалено. |
|  | [date](function.date.md) | timestamp тепер допускає значення null. |
|  | [datesunrise](function.date-sunrise.md) | latitude, longitude, zenith і utcOffset тепер допускають значення null. |
|  | [datesunset](function.date-sunset.md) | latitude, longitude, zenith і utcOffset тепер допускають значення null. |
|  | [define](function.define.md) | Передача true у випадкуinsensitive тепер видає помилку рівня EWARNING. Передача false все ще дозволена. |
|  | [deflateadd](function.deflate-add.md) | context чекає екземпляр DeflateContext; раніше, очікувався ресурс (resource). |
|  | [deflateinit](function.deflate-init.md) | У разі успішного виконання функція повертає екземпляр DeflateContext; раніше, повертався ресурс (resource). |
|  | [dir](function.dir.md) | context тепер припускає значення null. |
|  | [domimportsimplexml](function.dom-import-simplexml.md) | Функція більше не повертає null у разі помилки. |
|  | [easterdate](function.easter-date.md) | year тепер припускає значення null. |
|  | [easterdays](function.easter-days.md) | year тепер припускає значення null. |
|  | [enchantbrokerdescribe](function.enchant-broker-describe.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerdescribe](function.enchant-broker-describe.md) | До цієї версії функція повертала false у разі виникнення помилки. |
|  | [enchantbrokerdictexists](function.enchant-broker-dict-exists.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerfree](function.enchant-broker-free.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerfreedict](function.enchant-broker-free-dict.md) | dictionary очікує EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantbrokergetdictpath](function.enchant-broker-get-dict-path.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokergeterror](function.enchant-broker-get-error.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerinit](function.enchant-broker-init.md) | У разі успішного виконання, функція повертає екземпляр EnchantBroker; Раніше повертався ресурс (Resource). |
|  | [enchantbrokerlistdicts](function.enchant-broker-list-dicts.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerlistdicts](function.enchant-broker-list-dicts.md) | До цієї версії функція повертала false у разі виникнення помилки. |
|  | [enchantbrokerrequestdict](function.enchant-broker-request-dict.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerrequestdict](function.enchant-broker-request-dict.md) | У разі успішного виконання функція повертає екземпляр EnchantDictionary; Раніше повертався ресурс (Resource). |
|  | [enchantbrokerrequestpwldict](function.enchant-broker-request-pwl-dict.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokerrequestpwldict](function.enchant-broker-request-pwl-dict.md) | У разі успішного виконання функція повертає екземпляр EnchantDictionary; Раніше повертався ресурс (Resource). |
|  | [enchantbrokersetdictpath](function.enchant-broker-set-dict-path.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantbrokersetordering](function.enchant-broker-set-ordering.md) | broker очікує екземпляр EnchantBroker; Раніше очікували ресурс (resource). |
|  | [enchantdictadd](function.enchant-dict-add.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictaddтоsession](function.enchant-dict-add-to-session.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictcheck](function.enchant-dict-check.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictdescribe](function.enchant-dict-describe.md) | До цієї версії функція повертала false у разі виникнення помилки. |
|  | [enchantdictdescribe](function.enchant-dict-describe.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictgeterror](function.enchant-dict-get-error.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictісadded](function.enchant-dict-is-added.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictquickcheck](function.enchant-dict-quick-check.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictstorereplacement](function.enchant-dict-store-replacement.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [enchantdictsuggest](function.enchant-dict-suggest.md) | dictionary чекає екземпляр EnchantDictionary; Раніше очікували ресурс (resource). |
|  | [errorlog](function.error-log.md) | Параметр destination та additionalheaders тепер допускають значення null. |
|  | [errorreporting](function.error-reporting.md) | errorlevel тепер припускає значення null. |
|  | [exifreaddata](function.exif-read-data.md) | requiredsections тепер допускає значення null. |
|  | [explode](function.explode.md) | explode тепер викидає TypeError, якщо параметр separator є порожнім рядком (""). Раніше замість вилучення explode повертала false. |
|  | [fgetcsv](function.fgetcsv.md) | Параметр length тепер припускає значення null. |
|  | [filegetcontents](function.file-get-contents.md) | Параметр length тепер припускає значення null. |
|  | [finfobuffer](function.finfo-buffer.md) | context тепер припускає значення null. |
|  | [finfofile](function.finfo-file.md) | context тепер припускає значення null. |
|  | [floor](function.floor.md) | num більше не приймає внутрішні об'єкти, що підтримують числове перетворення. |
|  | [fsockopen](function.fsockopen.md) | timeout тепер допускає значення null. |
|  | [fwrite](function.fwrite.md) | Параметр length тепер припускає значення null. |
|  | [getclass](function.get-class.md) | Виклик функції поза класом без жодних аргументів викликає виняток Error. Раніше видавалася помилка рівня EWARNING та функція повертала значення false. |
|  | [getclassmethods](function.get-class-methods.md) | Параметр objectорclass тепер приймає лише об'єкти чи коректні імена класів. |
|  | [getdefinedfunctions](function.get-defined-functions.md) | Значення параметра excludedisabled за умовчанням змінено з false на true. |
|  | [getheaders](function.get-headers.md) | Тип параметра associative було змінено з цілого числа (int) на логічне значення (bool). |
|  | [getparentclass](function.get-parent-class.md) | Параметр objectорclass тепер приймає лише об'єкти чи коректні імена класів |
|  | [getresources](function.get-resources.md) | type тепер допускає значення null. |
|  | [getdate](function.getdate.md) | timestamp тепер допускає значення null. |
|  | [gmdate](function.gmdate.md) | timestamp тепер допускає значення null. |
|  | [gmmktime](function.gmmktime.md) | minute, second, month, day і year тепер допускають значення null. |
|  | [gmmktime](function.gmmktime.md) | hour більше не є необов'язковим. |
|  | [gmpbinomial](function.gmp-binomial.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [gmpexport](function.gmp-export.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [gmpimport](function.gmp-import.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [gmstrftime](function.gmstrftime.md) | timestamp тепер допускає значення null. |
|  | [graphemesubstr](function.grapheme-substr.md) | Функція тепер послідовно притискає зсуви, що виходять за межі, до кордону рядка. Раніше у деяких випадках замість порожнього рядка поверталося значення false. |
|  | [gzgets](function.gzgets.md) | length тепер припускає значення null; раніше значення за промовчанням було 1024. |
|  | [gzwrite](function.gzwrite.md) | length тепер припускає значення null; раніше значенням за промовчанням був 0. |
|  | [hash](function.hash.md) | Функція hash тепер викидає виняток ValueError, якщо алгоритм невідомий; раніше натомість поверталося значення false. |
|  | [hashhmac](function.hash-hmac.md) | Функція hash тепер викидає виняток ValueError, якщо алгоритм невідомий; раніше натомість поверталося значення false. |
|  | [hashupdatefile](function.hash-update-file.md) | streamcontext тепер припускає значення null. |
|  | [headerremove](function.header-remove.md) | name тепер припускає значення null. |
|  | [htmlentitydecode](function.html-entity-decode.md) | encoding тепер допускає значення null. |
|  | [htmlentities](function.htmlentities.md) | encoding тепер допускає значення null. |
|  | [iconvmimedecode](function.iconv-mime-decode.md) | encoding тепер допускає значення null. |
|  | [iconvmimedecodeheaders](function.iconv-mime-decode-headers.md) | encoding тепер допускає значення null. |
|  | [iconvstrlen](function.iconv-strlen.md) | encoding тепер допускає значення null. |
|  | [iconvstrpos](function.iconv-strpos.md) | encoding тепер допускає значення null. |
|  | [iconvstrrpos](function.iconv-strrpos.md) | encoding тепер допускає значення null. |
|  | [iconvsubstr](function.iconv-substr.md) | length та encoding тепер допускають значення null. |
|  | [idate](function.idate.md) | timestamp тепер допускає значення null. |
|  | [ignoreuserabort](function.ignore-user-abort.md) | enable тепер допускає значення null. |
|  | [imageaffine](function.imageaffine.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imageaffine](function.imageaffine.md) | clip тепер припускає значення null. |
|  | [imagealphablending](function.imagealphablending.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageantialias](function.imageantialias.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagearc](function.imagearc.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagebmp](function.imagebmp.md) | Тип параметра compressed тепер логічне значення (bool); раніше був цілим числом (int). |
|  | [imagebmp](function.imagebmp.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagechar](function.imagechar.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecharup](function.imagecharup.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorallocate](function.imagecolorallocate.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorallocatealpha](function.imagecolorallocatealpha.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorat](function.imagecolorat.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorclosest](function.imagecolorclosest.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorclosesthwb](function.imagecolorclosesthwb.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolordeallocate](function.imagecolordeallocate.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorexact](function.imagecolorexact.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorexactalpha](function.imagecolorexactalpha.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolormatch](function.imagecolormatch.md) | image1 і image2 тепер чекають на екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorresolve](function.imagecolorresolve.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorresolvealpha](function.imagecolorresolvealpha.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorset](function.imagecolorset.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorsforindex](function.imagecolorsforindex.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolorsforindex](function.imagecolorsforindex.md) | Функція imagecolorsforindex тепер викидає виключення ValueError, якщо параметр color поза допустимим діапазоном; раніше натомість поверталося значення false. |
|  | [imagecolorstotal](function.imagecolorstotal.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolortransparent](function.imagecolortransparent.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecolortransparent](function.imagecolortransparent.md) | color тепер припускає значення null. |
|  | [imageconvolution](function.imageconvolution.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecopy](function.imagecopy.md) | dstimage та srcimage тепер чекають екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecopymerge](function.imagecopymerge.md) | dstimage та srcimage тепер чекають екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecopymergegray](function.imagecopymergegray.md) | dstimage та srcimage тепер чекають екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecopyresampled](function.imagecopyresampled.md) | dstimage та srcimage тепер чекають екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecopyresized](function.imagecopyresized.md) | dstimage та srcimage тепер чекають екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecreate](function.imagecreate.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefrombmp](function.imagecreatefrombmp.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromgd](function.imagecreatefromgd.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromgd2](function.imagecreatefromgd2.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromgd2part](function.imagecreatefromgd2part.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromgif](function.imagecreatefromgif.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromjpeg](function.imagecreatefromjpeg.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefrompng](function.imagecreatefrompng.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromstring](function.imagecreatefromstring.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromtga](function.imagecreatefromtga.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromwbmp](function.imagecreatefromwbmp.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromwebp](function.imagecreatefromwebp.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromxbm](function.imagecreatefromxbm.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatefromxpm](function.imagecreatefromxpm.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecreatetruecolor](function.imagecreatetruecolor.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecrop](function.imagecrop.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagecrop](function.imagecrop.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecropauto](function.imagecropauto.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagecropauto](function.imagecropauto.md) | У разі успішного виконання, функція тепер повертає об'єкт GDImage; раніше повертався ресурс (resource). |
|  | [imagedashedline](function.imagedashedline.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagedestroy](function.imagedestroy.md) | Функція тепер є NOP. |
|  | [imagedestroy](function.imagedestroy.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageellipse](function.imageellipse.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefill](function.imagefill.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefilledarc](function.imagefilledarc.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefilledellipse](function.imagefilledellipse.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefilledpolygon](function.imagefilledpolygon.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefilledrectangle](function.imagefilledrectangle.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefilltoborder](function.imagefilltoborder.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefilter](function.imagefilter.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageflip](function.imageflip.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagefttext](function.imagefttext.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegammacorrect](function.imagegammacorrect.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegd](function.imagegd.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegd2](function.imagegd2.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegetclip](function.imagegetclip.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegetinterpolation](function.imagegetinterpolation.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegif](function.imagegif.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagegrabscreen](function.imagegrabscreen.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagegrabwindow](function.imagegrabwindow.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagegrabwindow](function.imagegrabwindow.md) | clientarea тепер очікує логічне значення (bool); раніше очікувалося ціле число (int). |
|  | [imageinterlace](function.imageinterlace.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageinterlace](function.imageinterlace.md) | enable тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int). |
|  | [imageistruecolor](function.imageistruecolor.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagejpeg](function.imagejpeg.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagelayereffect](function.imagelayereffect.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageline](function.imageline.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageopenpolygon](function.imageopenpolygon.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagepalettecopy](function.imagepalettecopy.md) | dst і src тепер очікують на екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagepalettetotruecolor](function.imagepalettetotruecolor.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagepng](function.imagepng.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagepolygon](function.imagepolygon.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagerectangle](function.imagerectangle.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imageresolution](function.imageresolution.md) | resolutionx та resolutiony тепер допускають значення null. |
|  | [imagerotate](function.imagerotate.md) | Невикористовуваний v тепер очікує логічне значення (bool); раніше очікувалося ціле число (int). |
|  | [imagerotate](function.imagerotate.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagerotate](function.imagerotate.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagesavealpha](function.imagesavealpha.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagescale](function.imagescale.md) | У разі успішного виконання, функція тепер повертає екземпляр GDImage; раніше повертався ресурс (resource). |
|  | [imagescale](function.imagescale.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesetbrush](function.imagesetbrush.md) | image та brush тепер очікують екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesetclip](function.imagesetclip.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesetinterpolation](function.imagesetinterpolation.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesetpixel](function.imagesetpixel.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesetthickness](function.imagesetthickness.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesettile](function.imagesettile.md) | image і tile тепер чекають на екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagestring](function.imagestring.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagestringup](function.imagestringup.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesx](function.imagesx.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagesy](function.imagesy.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagetruecolortopalette](function.imagetruecolortopalette.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagettfbbox](function.imagettfbbox.md) | Доданий параметр options. |
|  | [imagettftext](function.imagettftext.md) | Доданий параметр options. |
|  | [imagewbmp](function.imagewbmp.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagewbmp](function.imagewbmp.md) | foregroundcolor тепер припускає значення null. |
|  | [imagewebp](function.imagewebp.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagexbm](function.imagexbm.md) | foregroundcolor тепер припускає значення null. |
|  | [imagexbm](function.imagexbm.md) | image тепер чекає екземпляр GdImage; раніше очікували ресурс (resource). |
|  | [imagexbm](function.imagexbm.md) | Четвертий параметр, який не використовувався, було видалено. |
|  | [imapappend](function.imap-append.md) | options та internaldate тепер допускають значення null. |
|  | [imapheaderinfo](function.imap-headerinfo.md) | Невикористовуваний параметр defaulthost було видалено. |
|  | [imapmail](function.imap-mail.md) | additionalheaders, cc, bcc та returnpath тепер допускають значення null. |
|  | [imapsort](function.imap-sort.md) | reverse є логічним типом (bool) замість цілого числа (int). |
|  | [imapsort](function.imap-sort.md) | searchcriteria і charset тепер nullable. |
|  | [implode](function.implode.md) | Передача separator після array більше не підтримується. |
|  | [inflateadd](function.inflate-add.md) | context чекає екземпляр InflateContext; раніше, очікувався ресурс (resource). |
|  | [inflategetreadlen](function.inflate-get-read-len.md) | context чекає екземпляр InflateContext; раніше, очікувався ресурс (resource). |
|  | [inflategetstatus](function.inflate-get-status.md) | context чекає екземпляр InflateContext; раніше, очікувався ресурс (resource). |
|  | [inflateinit](function.inflate-init.md) | У разі успішного виконання функція повертає екземпляр InflateContext; раніше повертався ресурс (resource). |
|  | [ісnumeric](function.is-numeric.md) | Рядки, що складаються з чисел, що закінчуються пробілом ("42"), тепер повертатимуть true. Раніше натомість поверталося false. |
|  | [jdtounix](function.jdtounix.md) | Функція більше не повертає false у разі виникнення помилки, натомість викидає ValueError. |
|  | [ldapadd](function.ldap-add.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapaddext](function.ldap-add-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapbindext](function.ldap-bind-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapcompare](function.ldap-compare.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapcontrolpagedresult](function.ldap-control-paged-result.md) | Функцію було видалено. |
|  | [ldapcontrolpagedresultresponse](function.ldap-control-paged-result-response.md) | Функцію було видалено. |
|  | [ldapdelete](function.ldap-delete.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapdeleteext](function.ldap-delete-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapexoppasswd](function.ldap-exop-passwd.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldaplist](function.ldap-list.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmodadd](function.ldap-mod-add.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmoddel](function.ldap-mod-del.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmodreplace](function.ldap-mod-replace.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmodifybatch](function.ldap-modify-batch.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmodaddext](function.ldap-mod_add-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmoddelext](function.ldap-mod_del-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapmodreplaceext](function.ldap-mod_replace-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapread](function.ldap-read.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldaprename](function.ldap-rename.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldaprenameext](function.ldap-rename-ext.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapsaslbind](function.ldap-sasl-bind.md) | dn, password, mech, realm, authcid, authzid and props тепер допускають значення null. |
|  | [ldapsearch](function.ldap-search.md) | controls тепер допускає значення null; раніше значення за умовчанням було |
|  | [ldapsetrebindproc](function.ldap-set-rebind-proc.md) | callback тепер допускає значення null. |
|  | [ldapsort](function.ldap-sort.md) | Функцію було видалено. |
|  | [levenshtein](function.levenshtein.md) | До цієї версії levenshtein потрібно було викликати з двома чи п'ятьма аргументами. |
|  | [libxmluseinternalerrors](function.libxml-use-internal-errors.md) | useerrors тепер допускає значення null. Раніше значенням за промовчанням було false. |
|  | [localtime](function.localtime.md) | timestamp тепер допускає значення null. |
|  | [мбcheckencoding](function.mb-check-encoding.md) | Параметри value та encoding можуть набувати значення null. |
|  | [мбchr](function.mb-chr.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбconvertencoding](function.mb-convert-encoding.md) | Тепер відencoding може бути null. |
|  | [мбconvertencoding](function.mb-convert-encoding.md) | мбconvertencoding тепер викидає ValueError, якщо передано неприпустиме кодування fromencoding. |
|  | [мбconvertencoding](function.mb-convert-encoding.md) | мбconvertencoding тепер викидає ValueError, якщо передано неприпустиме кодування в toencoding. |
|  | [мбconvertkana](function.mb-convert-kana.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбdecodenumericentity](function.mb-decode-numericentity.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбdetectorder](function.mb-detect-order.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбencodemimeheader](function.mb-encode-mimeheader.md) | charset та transferencoding тепер допускають значення null. |
|  | [мбencodenumericentity](function.mb-encode-numericentity.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбereg](function.mb-ereg.md) | Тепер у разі успішного завершення ця функція повертає true. Раніше вона повертала довжину знайденого входження pattern у рядку string у разі, якщо було передано параметр matches. Якщо опціональний параметр matches не був заданий, або довжина рядка, що перевіряється дорівнювала 0, ця функція повертала число 1. |
|  | [мбeregmatch](function.mb-ereg-match.md) | options тепер допускає значення null. |
|  | [мбeregreplace](function.mb-ereg-replace.md) | options тепер допускає значення null. |
|  | [мбeregreplacecallback](function.mb-ereg-replace-callback.md) | options тепер допускає значення null. |
|  | [мбeregsearch](function.mb-ereg-search.md) | pattern та options тепер допускають значення null. |
|  | [мбeregsearchinit](function.mb-ereg-search-init.md) | pattern та options тепер допускають значення null. |
|  | [мбeregsearchpos](function.mb-ereg-search-pos.md) | pattern та options тепер допускають значення null. |
|  | [мбeregsearchregs](function.mb-ereg-search-regs.md) | pattern та options тепер допускають значення null. |
|  | [мбeregi](function.mb-eregi.md) | Тепер ця функція повертає true у разі успішного виконання. Раніше, якщо було встановлено параметр matches і було знайдено входження pattern у рядку string, поверталася довжина знайденої підрядки в байтах. Якщо параметр matches не задавався або довжина знайденого підрядка дорівнювала 0, функція повертала 1. |
|  | [мбeregireplace](function.mb-eregi-replace.md) | Параметр options тепер може набувати значення null. |
|  | [мбgetinfo](function.mb-get-info.md) | type більше не підтримує "funcoverload" та "funcoverloadList". |
|  | [мбhttpinput](function.mb-http-input.md) | type тепер може задаватися як null. |
|  | [мбhttpoutput](function.mb-http-output.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбinternalencoding](function.mb-internal-encoding.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбinternalencoding](function.mb-internal-encoding.md) | Тепер викидається виняток ValueError, якщо значення параметра encoding є неприпустимим кодуванням. Раніше натомість видавалася помилка рівня EWARNING. |
|  | [мбlanguage](function.mb-language.md) | Тепер параметр language може набувати значення null. |
|  | [мбord](function.mb-ord.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбparsestr](function.mb-parse-str.md) | Другий параметр став обов'язковим. |
|  | [мбregexencoding](function.mb-regex-encoding.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбregexsetoptions](function.mb-regex-set-options.md) | Якщо параметр options заданий і дорівнює null, повертаються попередні параметри. Раніше поточні параметри поверталися. |
|  | [мбregexsetoptions](function.mb-regex-set-options.md) | Параметр options може набувати значення null. |
|  | [мбscrub](function.mb-scrub.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrsplit](function.mb-str-split.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrsplit](function.mb-str-split.md) | Функція більше не повертає false у разі невдачі. |
|  | [мбstrcut](function.mb-strcut.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrimwidth](function.mb-strimwidth.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstripos](function.mb-stripos.md) | needle тепер приймає порожній рядок. |
|  | [мбstripos](function.mb-stripos.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstristr](function.mb-stristr.md) | needle тепер приймає порожній рядок. |
|  | [мбstristr](function.mb-stristr.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrlen](function.mb-strlen.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrpos](function.mb-strpos.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrpos](function.mb-strpos.md) | needle тепер приймає порожній рядок. |
|  | [мбstrrchr](function.mb-strrchr.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrrchr](function.mb-strrchr.md) | needle тепер приймає порожній рядок. |
|  | [мбstrrichr](function.mb-strrichr.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrrichr](function.mb-strrichr.md) | needle тепер приймає порожній рядок. |
|  | [мбstrripos](function.mb-strripos.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrripos](function.mb-strripos.md) | needle тепер приймає порожній рядок. |
|  | [мбstrrpos](function.mb-strrpos.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrrpos](function.mb-strrpos.md) | Передача encoding як третій аргумент замість offset була видалена. |
|  | [мбstrrpos](function.mb-strrpos.md) | needle тепер приймає порожній рядок. |
|  | [мбstrstr](function.mb-strstr.md) | needle тепер приймає порожній рядок. |
|  | [мбstrstr](function.mb-strstr.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбstrwidth](function.mb-strwidth.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбsubstitutecharacter](function.mb-substitute-character.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбsubstitutecharacter](function.mb-substitute-character.md) | Передача порожнього рядка у substitutecharacter більше не підтримується; натомість використовуйте "none". |
|  | [мбsubstr](function.mb-substr.md) | Тепер параметр encoding може набувати значення null. |
|  | [мбsubstrcount](function.mb-substr-count.md) | Тепер параметр encoding може набувати значення null. |
|  | [metaphone](function.metaphone.md) | Функція повертала false у разі виникнення помилки. |
|  | [mhash](function.mhash.md) | key тепер припускає значення null. |
|  | [mktime](function.mktime.md) | minute, second, month, day і year тепер допускають значення null. |
|  | [mktime](function.mktime.md) | hour більше не є необов'язковим. |
|  | [msggetqueue](function.msg-get-queue.md) | У разі успішного виконання, функція тепер повертає екземпляр SysvMessageQueue; раніше повертався ресурс (resource). |
|  | [msgreceive](function.msg-receive.md) | Параметр queue тепер чекає на екземпляр SysvMessageQueue; раніше очікували ресурс (resource). |
|  | [msgremovequeue](function.msg-remove-queue.md) | Параметр queue тепер чекає на екземпляр SysvMessageQueue; раніше очікували ресурс (resource). |
|  | [msgsend](function.msg-send.md) | Параметр queue тепер чекає на екземпляр SysvMessageQueue; раніше очікували ресурс (resource). |
|  | [msgsetqueue](function.msg-set-queue.md) | Параметр queue тепер чекає на екземпляр SysvMessageQueue; раніше очікували ресурс (resource). |
|  | [msgstatqueue](function.msg-stat-queue.md) | Параметр queue тепер чекає на екземпляр SysvMessageQueue; раніше очікували ресурс (resource). |
|  | [numberformat](function.number-format.md) | До цієї версії функція numberformat приймала один, два чи чотири параметри (але не три). |
|  | [про implicit flush](function.ob-implicit-flush.md) | enable тепер набуває логічного значення (bool); раніше приймалося ціле число (int). |
|  | [odbccolumns](function.odbc-columns.md) | schema, table і column тепер допускають значення null. |
|  | [odbcerror](function.odbc-error.md) | odbc тепер допускає значення null. |
|  | [odbcerrormsg](function.odbc-errormsg.md) | odbc тепер допускає значення null. |
|  | [odbcexec](function.odbc-exec.md) | Параметр flags був вилучений. |
|  | [odbcfetchrow](function.odbc-fetch-row.md) | row тепер припускає значення null. |
|  | [odbcprocedurecolumns](function.odbc-procedurecolumns.md) | До цієї версії функцію можна було викликати лише з одним або п'ятьма аргументами. |
|  | [odbcprocedures](function.odbc-procedures.md) | До цієї версії функцію можна було викликати лише з одним чи чотирма аргументами. |
|  | [odbctables](function.odbc-tables.md) | schema, table і types тепер можуть набувати значення null. |
|  | [opendir](function.opendir.md) | context тепер припускає значення null. |
|  | [opensslcsrexport](function.openssl-csr-export.md) | csr тепер приймає екземпляр OpenSSLCertificateSigningRequest; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrexportтоfile](function.openssl-csr-export-to-file.md) | csr тепер приймає екземпляр OpenSSLCertificateSigningRequest; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrgetpublickey](function.openssl-csr-get-public-key.md) | У разі успішного виконання повертає екземпляр OpenSSLAsymmetricKey; раніше повертався ресурс (resource) типу OpenSSL key. |
|  | [opensslcsrgetpublickey](function.openssl-csr-get-public-key.md) | csr тепер приймає екземпляр OpenSSLCertificateSigningRequest; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrgetsubject](function.openssl-csr-get-subject.md) | csr тепер приймає екземпляр OpenSSLCertificateSigningRequest; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrnew](function.openssl-csr-new.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey; раніше приймався ресурс (resource) типу OpenSSL key. |
|  | [opensslcsrnew](function.openssl-csr-new.md) | csr тепер приймає екземпляр OpenSSLCertificateSigningRequest; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrsign](function.openssl-csr-sign.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrsign](function.openssl-csr-sign.md) | csr тепер приймає екземпляр OpenSSLCertificateSigningRequest; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrsign](function.openssl-csr-sign.md) | каcertificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslcsrsign](function.openssl-csr-sign.md) | На успіх, ця функція відновить OpenSSLCertificate instance now; Попередньо, як ресурс типу OpenSSL X.509 був відновлений. |
|  | [opensslдхcomputekey](function.openssl-dh-compute-key.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslfreekey](function.openssl-free-key.md) | Функція застаріла, оскільки не має сенсу. |
|  | [opensslfreekey](function.openssl-free-key.md) | key тепер приймає OpenSSLAsymmetricKey; раніше брала ресурс (resource) типу OpenSSL key. |
|  | [opensslopen](function.openssl-open.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509 CSR. |
|  | [opensslopen](function.openssl-open.md) | cipheralgo більше не є необов'язковим параметром. |
|  | [opensslpkcs7decrypt](function.openssl-pkcs7-decrypt.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509 CSR. |
|  | [opensslpkcs7encrypt](function.openssl-pkcs7-encrypt.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslpkcs7sign](function.openssl-pkcs7-sign.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslpkcs7sign](function.openssl-pkcs7-sign.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509 CSR. |
|  | [opensslpkcs7verify](function.openssl-pkcs7-verify.md) | signerscertificatesfilename, untrustedcertificatesfilename, content та outputfilename тепер допускають значення null. |
|  | [opensslpkcs12export](function.openssl-pkcs12-export.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslpkcs12export](function.openssl-pkcs12-export.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpkcs12exportтоfile](function.openssl-pkcs12-export-to-file.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509 CSR. |
|  | [opensslpkcs12exportтоfile](function.openssl-pkcs12-export-to-file.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpkeyexport](function.openssl-pkey-export.md) | key тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpkeyexportтоfile](function.openssl-pkey-export-to-file.md) | key тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpkeyfree](function.openssl-pkey-free.md) | Функція застаріла, оскільки не має сенсу. |
|  | [opensslpkeyfree](function.openssl-pkey-free.md) | key тепер приймає екземпляр OpenSSLAsymmetricKey; раніше приймався ресурс (resource) типу OpenSSL key. |
|  | [opensslpkeygetdetails](function.openssl-pkey-get-details.md) | key тепер приймає екземпляр OpenSSLAsymmetricKey; раніше приймався ресурс (resource) типу OpenSSL key. |
|  | [opensslpkeygetprivate](function.openssl-pkey-get-private.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpkeygetprivate](function.openssl-pkey-get-private.md) | У разі успішного виконання функція повертає екземпляр OpenSSLAsymmetricKey; раніше повертався ресурс (resource) типу OpenSSL key. |
|  | [opensslpkeygetprivate](function.openssl-pkey-get-private.md) | passphrase тепер допускає значення null. |
|  | [opensslpkeygetpublic](function.openssl-pkey-get-public.md) | publickey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpkeygetpublic](function.openssl-pkey-get-public.md) | У разі успішного виконання функція повертає екземпляр OpenSSLAsymmetricKey; раніше повертався ресурс (resource) типу OpenSSL key. |
|  | [opensslpkeynew](function.openssl-pkey-new.md) | У разі успішного виконання функція повертає екземпляр OpenSSLAsymmetricKey; раніше повертався ресурс (resource) типу OpenSSL key. |
|  | [opensslprivatedecrypt](function.openssl-private-decrypt.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslprivateencrypt](function.openssl-private-encrypt.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpublicdecrypt](function.openssl-public-decrypt.md) | publickey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslpublicencrypt](function.openssl-public-encrypt.md) | publickey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslrandompseudobytes](function.openssl-random-pseudo-bytes.md) | strongresult тепер допускає значення null. |
|  | [opensslseal](function.openssl-seal.md) | cipheralgo більше не є необов'язковим параметром. |
|  | [opensslseal](function.openssl-seal.md) | iv тепер допускає значення null. |
|  | [opensslseal](function.openssl-seal.md) | publickey тепер приймає масив (array) екземплярів OpenSSLAsymmetricKey; раніше приймався масив (array) ресурсів (resource) типу OpenSSL key. |
|  | [opensslsign](function.openssl-sign.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslspkinew](function.openssl-spki-new.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey; раніше приймався ресурс (resource) типу OpenSSL key. |
|  | [opensslverify](function.openssl-verify.md) | publickey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslx509checkprivatekey](function.openssl-x509-check-private-key.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509checkprivatekey](function.openssl-x509-check-private-key.md) | privatekey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslx509checkpurpose](function.openssl-x509-checkpurpose.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509checkpurpose](function.openssl-x509-checkpurpose.md) | untrustedcertificatesfile тепер припускає значення null. |
|  | [opensslx509export](function.openssl-x509-export.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509exportтоfile](function.openssl-x509-export-to-file.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509fingerprint](function.openssl-x509-fingerprint.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509free](function.openssl-x509-free.md) | Функція застаріла, оскільки не має сенсу. |
|  | [opensslx509free](function.openssl-x509-free.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509parse](function.openssl-x509-parse.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509read](function.openssl-x509-read.md) | У разі успішного виконання повертає екземпляр OpenSSLCertificate; раніше повертався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509read](function.openssl-x509-read.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [opensslx509verify](function.openssl-x509-verify.md) | publickey тепер приймає екземпляр OpenSSLAsymmetricKey або OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL key або OpenSSL X.509. |
|  | [opensslx509verify](function.openssl-x509-verify.md) | certificate тепер приймає екземпляр OpenSSLCertificate; раніше приймався ресурс (resource) типу OpenSSL X.509. |
|  | [pack](function.pack.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [parsestr](function.parse-str.md) | result більше не є необов'язковим. |
|  | [parseurl](function.parse-url.md) | parseurl тепер розрізняє відсутні та порожні запити та фрагменти. |
|  | [passwordhash](function.password-hash.md) | Параметр algo тепер припускає значення null. |
|  | [passwordhash](function.password-hash.md) | passwordhash більше не повертає false у разі виникнення помилки. |
|  | [pcntlasyncsignals](function.pcntl-async-signals.md) | enable тепер допускає значення null. |
|  | [pcntlgetpriority](function.pcntl-getpriority.md) | processid тепер припускає значення null. |
|  | [pcntlsetpriority](function.pcntl-setpriority.md) | processid тепер припускає значення null. |
|  | [pfsockopen](function.pfsockopen.md) | timeout тепер допускає значення null. |
|  | [пгclientencoding](function.pg-client-encoding.md) | connection тепер допускає значення null. |
|  | [пгclose](function.pg-close.md) | connection тепер допускає значення null. |
|  | [пгdbname](function.pg-dbname.md) | connection тепер допускає значення null. |
|  | [пгendcopy](function.pg-end-copy.md) | connection тепер допускає значення null. |
|  | [пгfetchall](function.pg-fetch-all.md) | Функція pgfetchall тепер повертає порожній масив (array) замість значення false для наборів результатів без рядків. |
|  | [пгhost](function.pg-host.md) | connection тепер допускає значення null. |
|  | [пгlasterror](function.pg-last-error.md) | connection тепер допускає значення null. |
|  | [пглоwrite](function.pg-lo-write.md) | length тепер припускає значення null. |
|  | [пгoptions](function.pg-options.md) | connection тепер допускає значення null. |
|  | [пгping](function.pg-ping.md) | connection тепер допускає значення null. |
|  | [пгport](function.pg-port.md) | connection тепер допускає значення null. |
|  | [пгtrace](function.pg-trace.md) | connection тепер допускає значення null. |
|  | [пгtty](function.pg-tty.md) | connection тепер допускає значення null. |
|  | [пгuntrace](function.pg-untrace.md) | connection тепер допускає значення null. |
|  | [пгversion](function.pg-version.md) | connection тепер допускає значення null. |
|  | [phpversion](function.phpversion.md) | extension тепер допускає значення null. |
|  | [readdir](function.readdir.md) | dirhandle тепер допускає значення null. |
|  | [readlineinfo](function.readline-info.md) | varname і value тепер допускають значення null. |
|  | [readlinereadhistory](function.readline-read-history.md) | filename тепер допускає значення null. |
|  | [readlinewritehistory](function.readline-write-history.md) | filename тепер допускає значення null. |
|  | [rewinddir](function.rewinddir.md) | dirhandle тепер допускає значення null. |
|  | [round](function.round.md) | num більше не приймає внутрішні об'єкти, що підтримують числове перетворення. |
|  | [sapiwindowsvt100support](function.sapi-windows-vt100-support.md) | enable тепер допускає значення null. |
|  | [scandir](function.scandir.md) | context тепер припускає значення null. |
|  | [semacquire](function.sem-acquire.md) | Параметр semaphore тепер чекає на екземпляр SysvSemaphore; раніше очікували ресурс (resource). |
|  | [semget](function.sem-get.md) | Тип autorelease змінено з цілого числа (int) на логічне значення (bool). |
|  | [semget](function.sem-get.md) | У разі успішного виконання функція повертає екземпляр SysvSemaphore; раніше повертався ресурс (resource). |
|  | [semrelease](function.sem-release.md) | Параметр semaphore тепер чекає на екземпляр SysvSemaphore; раніше очікували ресурс (resource). |
|  | [semremove](function.sem-remove.md) | Параметр semaphore тепер чекає на екземпляр SysvSemaphore; раніше очікували ресурс (resource). |
|  | [sessioncacheexpire](function.session-cache-expire.md) | value може набувати значення null. |
|  | [sessioncachelimiter](function.session-cache-limiter.md) | value може набувати значення null. |
|  | [sessionід](function.session-id.md) | id тепер може бути null. |
|  | [sessionmodulename](function.session-module-name.md) | module тепер може бути null. |
|  | [sessionname](function.session-name.md) | module тепер може бути null. |
|  | [sessionsavepath](function.session-save-path.md) | path тепер може бути null. |
|  | [sessionsetcookieparams](function.session-set-cookie-params.md) | path, domain, secure і httponly тепер можуть бути null. |
|  | [seterrorhandler](function.set-error-handler.md) | Параметр errcontext був видалений і більше не передається в функцію обробки помилок. |
|  | [shmattach](function.shm-attach.md) | size тепер припускає значення null. |
|  | [shmattach](function.shm-attach.md) | У разі успішного виконання функція повертає екземпляр SysvSharedMemory; раніше повертався ресурс (resource). |
|  | [shmdetach](function.shm-detach.md) | shm очікує екземпляр SysvSharedMemory; раніше очікували ресурс (resource). |
|  | [shmgetvar](function.shm-get-var.md) | shm тепер чекає екземпляр SysvSharedMemory; раніше очікували ресурс (resource). |
|  | [shmhasvar](function.shm-has-var.md) | shm тепер чекає екземпляр SysvSharedMemory; раніше очікували ресурс (resource). |
|  | [shmputvar](function.shm-put-var.md) | shm тепер чекає екземпляр SysvSharedMemory; раніше очікували ресурс (resource). |
|  | [shmremove](function.shm-remove.md) | shm тепер чекає екземпляр SysvSharedMemory; раніше очікували ресурс (resource). |
|  | [shmremovevar](function.shm-remove-var.md) | shm тепер чекає екземпляр SysvSharedMemory; раніше очікували ресурс (resource). |
|  | [shmopclose](function.shmop-close.md) | Параметр shmop очікує екземпляр Shmop; раніше очікували ресурс (resource). |
|  | [shmopdelete](function.shmop-delete.md) | Параметр shmop очікує екземпляр Shmop; раніше очікували ресурс (resource). |
|  | [shmopopen](function.shmop-open.md) | У разі успішного виконання повертається екземпляр Shmop; раніше повертався ресурс (resource). |
|  | [shmopread](function.shmop-read.md) | Параметр shmop очікує екземпляр Shmop; раніше очікували ресурс (resource). |
|  | [shmopsize](function.shmop-size.md) | Параметр shmop очікує екземпляр Shmop; раніше очікували ресурс (resource). |
|  | [shmopwrite](function.shmop-write.md) | Параметр shmop очікує екземпляр Shmop; раніше очікували ресурс (resource). |
|  | [shmopwrite](function.shmop-write.md) | До PHP 8.0.0 у разі помилки поверталося false. |
|  | [socketaccept](function.socket-accept.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [socketaddrinfobind](function.socket-addrinfo-bind.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [socketaddrinfobind](function.socket-addrinfo-bind.md) | address тепер екземпляр класу AddressInfo; раніше був ресурсом (resource). |
|  | [socketaddrinfoconnect](function.socket-addrinfo-connect.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [socketaddrinfoconnect](function.socket-addrinfo-connect.md) | address тепер екземпляр класу AddressInfo; раніше був ресурсом (resource). |
|  | [socketaddrinfoexplain](function.socket-addrinfo-explain.md) | address тепер екземпляр класу AddressInfo; раніше був ресурсом (resource). |
|  | [socketaddrinfolookup](function.socket-addrinfo-lookup.md) | У разі успішного виконання функція повертає масив екземплярів AddressInfo; раніше повертався ресурс (resource). |
|  | [socketaddrinfolookup](function.socket-addrinfo-lookup.md) | Service тепер допускає значення null. |
|  | [socketbind](function.socket-bind.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketclearerror](function.socket-clear-error.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketclearerror](function.socket-clear-error.md) | socket тепер допускає значення null. |
|  | [socketclose](function.socket-close.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketconnect](function.socket-connect.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketconnect](function.socket-connect.md) | port тепер допускає значення null. |
|  | [socketcreate](function.socket-create.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [socketcreatelisten](function.socket-create-listen.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [socketcreatepair](function.socket-create-pair.md) | pair є посиланням на масив екземплярів Socket; раніше був посиланням на масив ресурсів (resource). |
|  | [socketexportstream](function.socket-export-stream.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketgetoption](function.socket-get-option.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketgetpeername](function.socket-getpeername.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketgetsockname](function.socket-getsockname.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketimportstream](function.socket-import-stream.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [socketlasterror](function.socket-last-error.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketlasterror](function.socket-last-error.md) | socket тепер допускає значення null. |
|  | [socketlisten](function.socket-listen.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketread](function.socket-read.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketrecv](function.socket-recv.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketrecvfrom](function.socket-recvfrom.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketrecvmsg](function.socket-recvmsg.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketsend](function.socket-send.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketsendmsg](function.socket-sendmsg.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketsendto](function.socket-sendto.md) | port тепер допускає значення null. |
|  | [socketsendto](function.socket-sendto.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketsetblock](function.socket-set-block.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketsetnonblock](function.socket-set-nonblock.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketsetoption](function.socket-set-option.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketshutdown](function.socket-shutdown.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketwrite](function.socket-write.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketwrite](function.socket-write.md) | length тепер припускає значення null. |
|  | [socketwsaprotocolinfoexport](function.socket-wsaprotocol-info-export.md) | socket тепер екземпляр класу Socket; раніше був ресурсом (resource). |
|  | [socketwsaprotocolinfoimport](function.socket-wsaprotocol-info-import.md) | У разі успішного виконання, функція повертає екземпляр Socket; раніше повертався ресурс (resource). |
|  | [soundex](function.soundex.md) | До цієї версії при виклику функції з порожнім рядком поверталося false без особливих причин. |
|  | [splautoload](function.spl-autoload.md) | fileextensions тепер допускає значення null. |
|  | [splautoloadextensions](function.spl-autoload-extensions.md) | fileextensions тепер допускає значення null. |
|  | [splautoloadregister](function.spl-autoload-register.md) | callback тепер допускає значення null. |
|  | [sprintf](function.sprintf.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [strsplit](function.str-split.md) | Тепер якщо параметр length менший за 1, буде викинута помилка ValueError; раніше, натомість видавалася помилка рівня EWARNING, а функція повертала false. |
|  | [strwordcount](function.str-word-count.md) | characters тепер допускає значення null. |
|  | [strcspn](function.strcspn.md) | length тепер припускає значення null. |
|  | [streamcontextcreate](function.stream-context-create.md) | Параметри options і params тепер допускають значення null. |
|  | [streamcontextgetdefault](function.stream-context-get-default.md) | Параметр options тепер дозволяє значення null. |
|  | [streamcopyтоstream](function.stream-copy-to-stream.md) | Параметр length тепер припускає значення null. |
|  | [streamgetcontents](function.stream-get-contents.md) | length тепер припускає значення null. |
|  | [streamsocketaccept](function.stream-socket-accept.md) | timeout тепер допускає значення null. |
|  | [streamsocketclient](function.stream-socket-client.md) | timeout і context тепер допускають значення null. |
|  | [streamsocketenablecrypto](function.stream-socket-enable-crypto.md) | sessionstream тепер припускає значення null. |
|  | [streamsocketserver](function.stream-socket-server.md) | Параметр context тепер припускає значення null. |
|  | [strftime](function.strftime.md) | timestamp тепер допускає значення null. |
|  | [striptags](function.strip-tags.md) | allowedtags тепер допускає значення null. |
|  | [stripos](function.stripos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [stristr](function.stristr.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strpos](function.strpos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strrchr](function.strrchr.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strripos](function.strripos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strrpos](function.strrpos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strspn](function.strspn.md) | length тепер припускає значення null. |
|  | [strstr](function.strstr.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strtotime](function.strtotime.md) | BaseTimestamp тепер допускає значення null. |
|  | [substr](function.substr.md) | Параметр length тепер припускає значення null. Якщо значення length явно задано як null, функція повертає підрядок, що закінчується в кінці рядка; раніше повертався порожній рядок. |
|  | [substr](function.substr.md) | Функція повертає порожній рядок, де раніше повертала false. |
|  | [substrcompare](function.substr-compare.md) | length тепер припускає значення null. |
|  | [substrcount](function.substr-count.md) | length тепер припускає значення null. |
|  | [substrreplace](function.substr-replace.md) | length тепер припускає значення null. |
|  | [touch](function.touch.md) | Параметр mtime та atime тепер допускають значення null. |
|  | [uasort](function.uasort.md) | Якщо параметр callback очікує, що буде передано значення посилання, функція тепер видасть помилку рівня EWARNING. |
|  | [uksort](function.uksort.md) | Якщо параметр callback очікує, що буде передано значення посилання, функція тепер видасть помилку рівня EWARNING. |
|  | [umask](function.umask.md) | Параметр mask тепер допускає значення null. |
|  | [unixtojd](function.unixtojd.md) | timestamp тепер допускає значення null. |
|  | [usort](function.usort.md) | Якщо параметр callback очікує, що буде передано значення посилання, функція тепер видасть помилку рівня EWARNING. |
|  | [vsprintf](function.vsprintf.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [xmlgetcurrentbyteindex](function.xml-get-current-byte-index.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlgetcurrentcolumnnumber](function.xml-get-current-column-number.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlgetcurrentlinenumber](function.xml-get-current-line-number.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlgeterrorcode](function.xml-get-error-code.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlparse](function.xml-parse.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlparseintostruct](function.xml-parse-into-struct.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlparsercreate](function.xml-parser-create.md) | Функція повертає тепер екземпляр XMLParser; раніше повертався ресурс (resource) чи false у разі виникнення помилки. |
|  | [xmlparsercreate](function.xml-parser-create.md) | encoding тепер допускає значення null. |
|  | [xmlparsercreateнс](function.xml-parser-create-ns.md) | Функція повертає тепер екземпляр XMLParser; раніше повертався ресурс (resource) чи false у разі виникнення помилки. |
|  | [xmlparsercreateнс](function.xml-parser-create-ns.md) | encoding тепер допускає значення null. |
|  | [xmlparserfree](function.xml-parser-free.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlparsergetoption](function.xml-parser-get-option.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlparsersetoption](function.xml-parser-set-option.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetcharacterdatahandler](function.xml-set-character-data-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetdefaulthandler](function.xml-set-default-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetelementhandler](function.xml-set-element-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetendnamespacedeclhandler](function.xml-set-end-namespace-decl-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetexternalentityrefhandler](function.xml-set-external-entity-ref-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetnotationdeclhandler](function.xml-set-notation-decl-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetobject](function.xml-set-object.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetprocessinginstructionhandler](function.xml-set-processing-instruction-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetstartnamespacedeclhandler](function.xml-set-start-namespace-decl-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [xmlsetunparsedentitydeclhandler](function.xml-set-unparsed-entity-decl-handler.md) | Параметр parser чекає на екземпляр XMLParser; раніше очікували ресурс (resource). |
|  | [zipclose](function.zip-close.md) | Функція застаріла на користь Object API дивіться ZipArchive::close. |
|  | [zipentryclose](function.zip-entry-close.md) | Функція застаріла на користь Object API. |
|  | [zipentrycompressedsize](function.zip-entry-compressedsize.md) | Функція застаріла на користь Object API, дивіться ZipArchive::statIndex. |
|  | [zipentrycompressionmethod](function.zip-entry-compressionmethod.md) | Функція застаріла на користь Object API, дивіться ZipArchive::statIndex. |
|  | [zipentryfilesize](function.zip-entry-filesize.md) | Функція застаріла на користь Object API, дивіться ZipArchive::statIndex. |
|  | [zipentryname](function.zip-entry-name.md) | Функція застаріла на користь Object API, дивіться ZipArchive::statIndex. |
|  | [zipentryopen](function.zip-entry-open.md) | Функція застаріла на користь Object API. |
|  | [zipentryread](function.zip-entry-read.md) | Функція застаріла на користь Object API дивіться ZipArchive::getFromIndex. |
|  | [zipopen](function.zip-open.md) | Функція застаріла на користь Object API дивіться ZipArchive::open. |
|  | [zipread](function.zip-read.md) | Функція застаріла на користь Object API, дивіться ZipArchive::statIndex. |
|  | [GlobIterator::construct](globiterator.construct.md) | Тепер викидає виняток ValueError, якщо параметр directory містить порожній рядок. Раніше викидався виняток RuntimeException. |
|  | [IntlTimeZone::getIDForWindowsID](intltimezone.getidforwindowsid.md) | Параметр region тепер допускає значення null. |
|  | [LimitIterator::construct](limititerator.construct.md) | Тепер викидає виняток ValueError, якщо усунення limit виявиться менше -1; Раніше викидався виняток RuntimeException. |
|  | [LimitIterator::construct](limititerator.construct.md) | Тепер викидає виняток ValueError, якщо зміщення offset виявиться меншим за 0; Раніше викидався виняток RuntimeException. |
|  | [Locale::getDisplayLanguage](locale.getdisplaylanguage.md) | displayLocale тепер допускає значення null. |
|  | [Locale::getDisplayName](locale.getdisplayname.md) | displayLocale тепер допускає значення null. |
|  | [Locale::getDisplayRegion](locale.getdisplayregion.md) | displayLocale тепер допускає значення null. |
|  | [Locale::getDisplayScript](locale.getdisplayscript.md) | displayLocale тепер допускає значення null. |
|  | [Locale::getDisplayVariant](locale.getdisplayvariant.md) | displayLocale тепер допускає значення null. |
|  | [mysqliresult::fetchobject](mysqli-result.fetch-object.md) | constructorargs тепер приймає для конструкторів без параметрів; раніше викидався виняток. |
|  | [mysqlistmt::construct](mysqli-stmt.construct.md) | query тепер припускає значення null. |
|  | [mysqli::begintransaction](mysqli.begin-transaction.md) | name тепер припускає значення null. |
|  | [mysqli::commit](mysqli.commit.md) | name тепер припускає значення null. |
|  | [mysqli::rollback](mysqli.rollback.md) | name тепер припускає значення null. |
|  | [NumberFormatter::create](numberformatter.create.md) | pattern тепер допускає значення null. |
|  | [PDOStatement::fetchAll](pdostatement.fetchall.md) | Метод тепер завжди повертає масив (array), раніше у разі помилки могло повертатися false. |
|  | [Phar::addFile](phar.addfile.md) | localName тепер допускає значення null. |
|  | [Phar::buildFromIterator](phar.buildfromiterator.md) | BaseDirectory тепер допускає значення null. |
|  | [Phar::compress](phar.compress.md) | extension тепер допускає значення null. |
|  | [Phar::convertToData](phar.converttodata.md) | format, compression і extension тепер допускають значення null. |
|  | [Phar::convertToExecutable](phar.converttoexecutable.md) | format, compression і localName тепер допускають значення null. |
|  | [Phar::createDefaultStub](phar.createdefaultstub.md) | index та webIndex тепер допускають значення null. |
|  | [Phar::decompress](phar.decompress.md) | extension тепер допускає значення null. |
|  | [Phar::getMetadata](phar.getmetadata.md) | Додано параметр unserializeOptions. |
|  | [Phar::setDefaultStub](phar.setdefaultstub.md) | webIndex тепер допускає значення null. |
|  | [Phar::setSignatureAlgorithm](phar.setsignaturealgorithm.md) | privateKey тепер допускає значення null. |
|  | [Phar::webPhar](phar.webphar.md) | fileNotFoundScript, mimeTypes і rewrite тепер допускають значення null. |
|  | [PharData::addFile](phardata.addfile.md) | localName тепер допускає значення null. |
|  | [PharData::buildFromIterator](phardata.buildfromiterator.md) | BaseDirectory тепер допускає значення null. |
|  | [PharData::compress](phardata.compress.md) | extension тепер допускає значення null. |
|  | [PharData::convertToData](phardata.converttodata.md) | format, compression і extension тепер допускають значення null. |
|  | [PharData::convertToExecutable](phardata.converttoexecutable.md) | format, compression і localName тепер допускають значення null. |
|  | [PharData::decompress](phardata.decompress.md) | extension тепер допускає значення null. |
|  | [PharData::setDefaultStub](phardata.setdefaultstub.md) | webIndex тепер допускає значення null. |
|  | [PharData::setSignatureAlgorithm](phardata.setsignaturealgorithm.md) | privateKey тепер допускає значення null. |
|  | [PharFileInfo::getMetadata](pharfileinfo.getmetadata.md) | Додано параметр unserializeOptions. |
|  | [PharFileInfo::isCompressed](pharfileinfo.iscompressed.md) | compression тепер допускає значення null. |
|  | [RecursiveDirectoryIterator::construct](recursivedirectoryiterator.construct.md) | Тепер викидає виняток ValueError, якщо параметр directory містить порожній рядок. Раніше викидався виняток RuntimeException. |
|  | [RecursiveIteratorIterator::getSubIterator](recursiveiteratoriterator.getsubiterator.md) | level тепер припускає значення null. |
|  | [ReflectionClass::getConstants](reflectionclass.getconstants.md) | Доданий параметр filter. |
|  | [ReflectionClass::getReflectionConstants](reflectionclass.getreflectionconstants.md) | Доданий параметр filter. |
|  | [ReflectionMethod::getClosure](reflectionmethod.getclosure.md) | object тепер допускає значення null. |
|  | [ReflectionParameter::getDefaultValue](reflectionparameter.getdefaultvalue.md) | Метод тепер дозволяє отримати значення за промовчанням для параметрів вбудованих функцій та вбудованих методів класу. Раніше викидалося ReflectionException. |
|  | [ReflectionParameter::getDefaultValueConstantName](reflectionparameter.getdefaultvalueconstantname.md) | Метод дозволяє отримувати імена значень за промовчанням для вбудованих функцій та вбудованих методів класу. Раніше викидалося ReflectionException. |
|  | [ReflectionProperty::getValue](reflectionproperty.getvalue.md) | object тепер допускає значення null. |
|  | [ReflectionProperty::isInitialized](reflectionproperty.isinitialized.md) | object тепер допускає значення null. |
|  | [SimpleXMLElement::asXML](simplexmlelement.asxml.md) | filename тепер допускає значення null. |
|  | [SoapClient::doRequest](soapclient.dorequest.md) | Тип oneWay тепер bool; раніше він був цілим числом (int). |
|  | [SoapClient::setCookie](soapclient.setcookie.md) | value тепер допускає значення null. |
|  | [SoapServer::handle](soapserver.handle.md) | request тепер допускає значення null. |
|  | [SplFileInfo::getFileInfo](splfileinfo.getfileinfo.md) | class тепер допускає значення null. |
|  | [SplFileInfo::getPathInfo](splfileinfo.getpathinfo.md) | class тепер допускає значення null. |
|  | [SplFileInfo::openFile](splfileinfo.openfile.md) | context тепер припускає значення null. |
|  | [SplFixedArray::construct](splfixedarray.construct.md) | Тепер викидає виняток ValueError, якщо параметр size негативний; раніше викидався виняток InvalidArgumentException. |
|  | [tidy::construct](tidy.construct.md) | filename, config, encoding та useIncludePath тепер допускають значення null. |
|  | [tidy::parseFile](tidy.parsefile.md) | config та encoding тепер допускають значення null. |
|  | [tidy::parseString](tidy.parsestring.md) | config та encoding тепер допускають значення null. |
|  | [tidy::repairFile](tidy.repairfile.md) | tidy::repairFile тепер статичний метод. |
|  | [tidy::repairFile](tidy.repairfile.md) | config та encoding тепер допускають значення null. |
|  | [tidy::repairString](tidy.repairstring.md) | tidy::repairString тепер статичний метод. |
|  | [tidy::repairString](tidy.repairstring.md) | config та encoding тепер допускають значення null. |
|  | [tidy::repairString](tidy.repairstring.md) | Функція більше не приймає useIncludePath. |
|  | [XMLReader::getAttribute](xmlreader.getattribute.md) | Функція більше не може повертати false. |
|  | [XMLReader::getAttributeNs](xmlreader.getattributens.md) | Функція більше не може повертати false. |
|  | [XMLReader::lookupNamespace](xmlreader.lookupnamespace.md) | Функція більше не може повертати false. |
|  | [XMLReader::next](xmlreader.next.md) | name тепер припускає значення null. |
|  | [XMLReader::open](xmlreader.open.md) | XMLReader::open тепер оголошений як статичний метод, але все ще може бути викликаний в екземплярі XMLReader. |
|  | [XMLReader::XML](xmlreader.xml.md) | XMLReader::XML тепер оголошений як статичний метод, але все ще може бути викликаний в екземплярі XMLReader. |
|  | [XMLWriter::endAttribute](xmlwriter.endattribute.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endCdata](xmlwriter.endcdata.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endComment](xmlwriter.endcomment.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endDocument](xmlwriter.enddocument.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endDtd](xmlwriter.enddtd.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endDtdAttlist](xmlwriter.enddtdattlist.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endDtdElement](xmlwriter.enddtdelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endDtdEntity](xmlwriter.enddtdentity.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endElement](xmlwriter.endelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::endPi](xmlwriter.endpi.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::flush](xmlwriter.flush.md) | Функція більше не може повертати false. |
|  | [XMLWriter::flush](xmlwriter.flush.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::fullEndElement](xmlwriter.fullendelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::openMemory](xmlwriter.openmemory.md) | Функція тепер повертає екземпляр XMLWriter у разі успішного виконання. Раніше у разі повертався ресурс (resource). |
|  | [XMLWriter::openUri](xmlwriter.openuri.md) | Функція тепер повертає екземпляр XMLWriter у разі успішного виконання. Раніше у разі повертався ресурс (resource). |
|  | [XMLWriter::outputMemory](xmlwriter.outputmemory.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::setIndent](xmlwriter.setindent.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::setIndentString](xmlwriter.setindentstring.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startAttribute](xmlwriter.startattribute.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startAttributeNs](xmlwriter.startattributens.md) | prefix тепер припускає значення null. |
|  | [XMLWriter::startAttributeNs](xmlwriter.startattributens.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startCdata](xmlwriter.startcdata.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startComment](xmlwriter.startcomment.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startDocument](xmlwriter.startdocument.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startDtd](xmlwriter.startdtd.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startDtdAttlist](xmlwriter.startdtdattlist.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startDtdElement](xmlwriter.startdtdelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startDtdEntity](xmlwriter.startdtdentity.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startElement](xmlwriter.startelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startElementNs](xmlwriter.startelementns.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::startPi](xmlwriter.startpi.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::text](xmlwriter.text.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeAttribute](xmlwriter.writeattribute.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeAttributeNs](xmlwriter.writeattributens.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeCdata](xmlwriter.writecdata.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeComment](xmlwriter.writecomment.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeDtd](xmlwriter.writedtd.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeDtdAttlist](xmlwriter.writedtdattlist.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeDtdElement](xmlwriter.writedtdelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeDtdEntity](xmlwriter.writedtdentity.md) | publicId, systemId і notationData тепер допускають значення null. |
|  | [XMLWriter::writeDtdEntity](xmlwriter.writedtdentity.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeElement](xmlwriter.writeelement.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeElementNs](xmlwriter.writeelementns.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writePi](xmlwriter.writepi.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [XMLWriter::writeRaw](xmlwriter.writeraw.md) | У параметрі writer тепер очікується екземпляр XMLWriter; раніше очікували ресурс (resource). |
|  | [ZipArchive::setEncryptionIndex](ziparchive.setencryptionindex.md) | password тепер допускає значення null. |
|  | [ZipArchive::setEncryptionName](ziparchive.setencryptionname.md) | password тепер допускає значення null. |
|  | [procopen](function.proc-open.md) | Додана опція createnewconsole у параметр options. |
|  | [arraymerge](function.array-merge.md) | Функцію тепер можна викликати без будь-яких параметрів. Раніше був потрібний хоча б один параметр. |
|  | [arraymergerecursive](function.array-merge-recursive.md) | Функцію тепер можна викликати без будь-яких параметрів. Раніше був потрібний хоча б один параметр. |
|  | [baseconvert](function.base-convert.md) | Передача некоректних символів видаватиме повідомлення про старіння. Результат буде обчислено так, якби некоректні символи не існували. |
|  | [bindec](function.bindec.md) | Передача некоректних символів видаватиме повідомлення про старіння. Результат буде обчислено так, якби некоректні символи не існували. |
|  | [chr](function.chr.md) | Функція більше не приймає непідтримувані значення codepoint і перетворює їх на 0. |
|  | [curlversion](function.curl-version.md) | Необов'язковий параметр age оголошений застарілим; якщо передано значення, воно ігнорується. |
|  | [fgetcsv](function.fgetcsv.md) | Тепер параметр escape може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |
|  | [fputcsv](function.fputcsv.md) | Тепер параметр escape може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |
|  | [getdeclaredclasses](function.get-declared-classes.md) | Раніше getdeclaredclasses завжди повертала батьківські класи перед дочірніми класами. Це не так. Для значення, що повертається getdeclaredclasss конкретний порядок не гарантується. |
|  | [getmagicquotesgpc](function.get-magic-quotes-gpc.md) | Функцію оголошено застарілою. |
|  | [getmagicquotesruntime](function.get-magic-quotes-runtime.md) | Функцію оголошено застарілою. |
|  | [gzread](function.gzread.md) | У разі помилки повертається false; раніше, повертався 0. |
|  | [gzwrite](function.gzwrite.md) | У разі помилки функція повертає false. раніше повертався 0. |
|  | [hashalgos](function.hash-algos.md) | Додано підтримку для crc32c. |
|  | [hexdec](function.hexdec.md) | Передача некоректних символів видаватиме повідомлення про старіння. Результат буде обчислено так, якби некоректні символи не існували. |
|  | [idnтоascii](function.idn-to-ascii.md) | Тепер значення за замовчуванням variant змінено на INTLIDNAVARIANTUTS46 замість застарілої константи INTLIDNAVARIANT |
|  | [idnтоutf8](function.idn-to-utf8.md) | Тепер значення за замовчуванням variant змінено на INTLIDNAVARIANTUTS46 замість застарілої константи INTLIDNAVARIANT |
|  | [imagecropauto](function.imagecropauto.md) | Значення за умовчанням mode було змінено на IMGCROPAUTO. Раніше значення за промовчанням було -1, що відповідає IMGCROPDEFAULT, але передача -1 тепер застаріла. |
|  | [imagecropauto](function.imagecropauto.md) | Поведінка imagecropauto() у комплекті libgd синхронізована із системним libgd: IMGCROPDEFAULT більше не використовує IMGCROPSIDES і для обрізки порога тепер використовується той же алгоритм, що і системним libgd. |
|  | [imagefilter](function.imagefilter.md) | Додано підтримку розсіювання (IMGFILTERSCATTER). |
|  | [implode](function.implode.md) | Передача separator після array (тобто використання недокументованого порядку параметрів) застаріла. |
|  | [ldapcontrolpagedresult](function.ldap-control-paged-result.md) | Функцію оголошено застарілою. |
|  | [ldapcontrolpagedresultresponse](function.ldap-control-paged-result-response.md) | Функцію оголошено застарілою. |
|  | [moneyformat](function.money-format.md) | Функція застаріла. Замість неї використовуйте NumberFormatter::formatCurrency. |
|  | [octdec](function.octdec.md) | Передача некоректних символів видаватиме повідомлення про старіння. Результат буде обчислено так, якби некоректні символи не існували. |
|  | [passwordhash](function.password-hash.md) | Модуль sodium забезпечує альтернативну реалізацію паролів Argon2. |
|  | [passwordhash](function.password-hash.md) | Параметр algo зараз очікує рядок (string), але все ще приймає число (int) для зворотної сумісності. |
|  | [passwordneedsrehash](function.password-needs-rehash.md) | Параметр algo зараз очікує рядок (string), але все ще приймає число (int) для зворотної сумісності. |
|  | [pregreplacecallback](function.preg-replace-callback.md) | Додано параметр flags. |
|  | [pregreplacecallbackarray](function.preg-replace-callback-array.md) | Додано параметр flags. |
|  | [procopen](function.proc-open.md) | Додана опція createprocessgroup у параметр options. |
|  | [procopen](function.proc-open.md) | procopen тепер приймає також масив (array) в command. |
|  | [stat](function.stat.md) | У Windows номер пристрою тепер є серійним номером тома, що містить файл та номер inode - це ідентифікатор, пов'язаний із файлом. |
|  | [stat](function.stat.md) | Статистика символьних посилань size, atime, mtime та ctime завжди відповідає статистиці цільового об'єкта. Це було раніше не характерно для NTS-складання на Windows. |
|  | [strgetcsv](function.str-getcsv.md) | Тепер порожній параметр escape інтерпретуватиметься як вимога вимкнення пропрієтарного механізму екранування. Раніше порожній рядок позначав використання символу екранування за промовчанням. |
|  | [striptags](function.strip-tags.md) | allowedtags альтернативно приймає масив (array). |
|  | [Locale::lookup](locale.lookup.md) | defaultLocale тепер допускає значення null. |
|  | [SplFileObject::fgetcsv](splfileobject.fgetcsv.md) | Тепер параметр escape може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |
|  | [SplFileObject::fputcsv](splfileobject.fputcsv.md) | Тепер параметр escape може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |
|  | [SplFileObject::fwrite](splfileobject.fwrite.md) | Функція тепер повертає false замість нуля у разі виникнення помилки. |
|  | [SplFileObject::getCsvControl](splfileobject.getcsvcontrol.md) | Як символ екранування можна використовувати порожній рядок. |
|  | [SplFileObject::setCsvControl](splfileobject.setcsvcontrol.md) | Тепер параметр escape може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |
|  | [SQLite3Stmt::bindParam](sqlite3stmt.bindparam.md) | Параметр param тепер підтримує нотацію @param. |
|  | [SQLite3Stmt::bindValue](sqlite3stmt.bindvalue.md) | Параметр param тепер підтримує нотацію @param. |
|  | [jdtounix](function.jdtounix.md) | Збільшена верхня межа julianday. Раніше він був 2465342 незалежно від архітектури. |
|  | [tidyNode::isHtml](tidynode.ishtml.md) | Виправлено, тепер функція поводиться розумно. Раніше майже будь-який вузол вважався вузлом HTML. |
|  | [curlsetopt](function.curl-setopt.md) | Додано CURLOPTHTTP09ALLOWED. |
|  | [dbaopen](function.dba-open.md) | Драйвер lmdb підтримує додатковий параметр $mapsize. |
|  | [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md) | Доданий специфікатор v параметрі format. |
|  | [apacherequestheaders](function.apache-request-headers.md) | Ця функція стала доступною у SAPI FPM. |
|  | [arraypush](function.array-push.md) | Тепер ця функція може бути викликана одним параметром. Раніше потрібно було мінімум два параметри. |
|  | [arrayunshift](function.array-unshift.md) | Тепер ця функція може бути викликана одним параметром. Раніше потрібно було мінімум два параметри. |
|  | [assert](function.assert.md) | Оголошення функції з іменем assert() усередині простору імен оголошено застарілим. Таке оголошення тепер видає помилку рівня EDEPRECATED. |
|  | [bcmul](function.bcmul.md) | Тепер bcmul повертає числа із заданою точністю. Раніше завершальні нулі в дробовій частині числа відкидалися. |
|  | [bcpow](function.bcpow.md) | Тепер bcpow повертає числа із заданою точністю. Раніше завершальні нулі в дробовій частині числа відкидалися. |
|  | [bcscale](function.bcscale.md) | bcscale тепер можна використовувати для отримання поточного масштабу; при встановленні нового значення поверне старе значення масштабу. Раніше scale був обов'язковим, і bcscale завжди повертав true. |
|  | [compact](function.compact.md) | compact тепер видає помилку рівня ENOTICE, якщо заданий рядок пов'язаний із віддаленою змінною. Раніше такі рядки пропускалися без жодного повідомлення. |
|  | [curlgetinfo](function.curl-getinfo.md) | Додано CURLINFOCONTENTLENGTHDOWNLOADT, CURLINFOCONTENTLENGTHUPLOADT, CURLINFOHTTPVERSION, CURLINFOPROTOCOL, CURLINFOPROXYSSLVERIFYRESULT, CURLINFOSCHEME, CURLINFOSIZEDOWNLOADT, CURLINFOSIZEUPLOADT, CURLINFOSPEEDDOWNLOADT, CURLINFOSPEEDUPLOADT, CURLINFOAPPCONNECTTIMET, CURLINFOCONNECTTIMET, CURLINFOFILETIMET, CURLINFONAMELOOKUPTIMET, CURLINFOPRETRANSFERTIMET, CURLINFOREDIRECTTIMET, CURLINFOSTARTTRANSFERTIMET, CURLINFOTOTALTIMEТ. |
|  | [curlsetopt](function.curl-setopt.md) | Введено CURLOPTABSTRACTUNIXSOCKET, CURLOPTKEEPSENDINGВІНERROR, CURLOPTPREPROXY, CURLOPTPROXYCAINFO, CURLOPTPROXYCAPATH, CURLOPTPROXYCRLFILE, CURLOPTPROXYKEYPASSWD, CURLOPTPROXYPINNEDPUBLICKEY, CURLOPTPROXYSSLCERT, CURLOPTPROXYSSLCERTTYPE, CURLOPTPROXYSSLCIPHERLIST, CURLOPTPROXYSSLKEY, CURLOPTPROXYSSLKEYTYPE, CURLOPTPROXYSSLOPTIONS, CURLOPTPROXYSSLVERIFYHOST, CURLOPTPROXYSSLVERIFYPEER, CURLOPTPROXYSSLVERSION, CURLOPTPROXYTLSAUTHPASSWORD, CURLOPTPROXYTLSAUTHTYPE, CURLOPTPROXYTLSAUTHUSERNAME, CURLOPTSOCKS5AUTH, CURLOPTSUPPRESSCONNECTHEADERS, CURLOPTDISALLOWUSERNAMEІНURL, CURLOPTDNSSHUFFLEADDRESSES, CURLOPTHAPPYEYEBALLSTIMEOUTMS, CURLOPTHAPROXYPROTOCOL, CURLOPTPROXYTLS13CIPHERS, CURLOPTSSHCOMPRESSION, CURLOPTTIMEVALUELARGE та CURLOPTTLS13CIPHERS. |
|  | [define](function.define.md) | Параметр caseinsensitive оголошено застарілим і буде видалено у версії 8.0.0. |
|  | [ftpfget](function.ftp-fget.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpfput](function.ftp-fput.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpget](function.ftp-get.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpнбfget](function.ftp-nb-fget.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpнбfput](function.ftp-nb-fput.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpнбget](function.ftp-nb-get.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpнбput](function.ftp-nb-put.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [ftpput](function.ftp-put.md) | Тепер параметр mode є опціональним. Раніше він був обов'язковим. |
|  | [getallheaders](function.getallheaders.md) | Ця функція стала доступною у SAPI FPM. |
|  | [imagecreatefromstring](function.imagecreatefromstring.md) | Додана підтримка WEBP (якщо підтримується libgd). |
|  | [ісcountable](function.is-countable.md) | Додана функція iscountable. |
|  | [jsondecode](function.json-decode.md) | Додано константу JSONTHROWВІНERROR для параметра flags. |
|  | [jsonencode](function.json-encode.md) | Додано константу JSONTHROWВІНERROR для параметра flags. |
|  | [ldapadd](function.ldap-add.md) | Додано підтримку параметра controls |
|  | [ldapcompare](function.ldap-compare.md) | Додано підтримку параметра controls |
|  | [ldapdelete](function.ldap-delete.md) | Додано підтримку параметра controls |
|  | [ldapexop](function.ldap-exop.md) | Додано підтримку controls |
|  | [ldapexoppasswd](function.ldap-exop-passwd.md) | Додано підтримку параметра controls |
|  | [ldaplist](function.ldap-list.md) | Додано підтримку параметра controls |
|  | [ldapmodadd](function.ldap-mod-add.md) | Додано підтримку параметра controls |
|  | [ldapmoddel](function.ldap-mod-del.md) | Додано підтримку параметра controls |
|  | [ldapmodreplace](function.ldap-mod-replace.md) | Додано підтримку параметра controls |
|  | [ldapmodifybatch](function.ldap-modify-batch.md) | Додано підтримку параметра controls |
|  | [ldapmodaddext](function.ldap-mod_add-ext.md) | Додано підтримку параметра controls |
|  | [ldapmoddelext](function.ldap-mod_del-ext.md) | Додано підтримку параметра controls |
|  | [ldapmodreplaceext](function.ldap-mod_replace-ext.md) | Додано підтримку параметра controls |
|  | [ldapparseresult](function.ldap-parse-result.md) | Додано підтримку параметра controls |
|  | [ldapread](function.ldap-read.md) | Додано підтримку параметра controls |
|  | [ldaprename](function.ldap-rename.md) | Додано підтримку параметра controls |
|  | [ldaprenameext](function.ldap-rename-ext.md) | Додано підтримку параметра controls |
|  | [ldapsearch](function.ldap-search.md) | Додано підтримку параметра controls |
|  | [list](function.list.md) | Додано підтримку присвоєння за посиланнями при деструктуруванні масиву. |
|  | [мбconvertcase](function.mb-convert-case.md) | Додано підтримку MBCASEFOLD, MBCASEUPPERSIMPLE, MBCASELOWERSIMPLE, MBCASETITLESIMPLE та MBCASEFOLDSIMPLE у параметрі mode. |
|  | [passwordhash](function.password-hash.md) | Додано підтримку алгоритму хешування паролів Argon2id за допомогою PASSWORDARGON2ID. |
|  | [pregquote](function.preg-quote.md) | Символ # тепер екранується |
|  | [sessiongetcookieparams](function.session-get-cookie-params.md) | Доданий елемент "samesite" у масив, що повертається. |
|  | [sessionsetcookieparams](function.session-set-cookie-params.md) | Додано альтернативний підпис, який підтримує масив опцій lifetimeорoptions. Цей підпис також підтримує налаштування cookie-атрибута SameSite. |
|  | [setcookie](function.setcookie.md) | Додано альтернативний підпис, що підтримує масив опцій options. Цей підпис також підтримує налаштування cookie-атрибута SameSite. |
|  | [setrawcookie](function.setrawcookie.md) | Додано альтернативний підпис, що підтримує масив опцій options. Цей підпис також підтримує налаштування cookie-атрибута SameSite. |
|  | [stripos](function.stripos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [stristr](function.stristr.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strpos](function.strpos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strrchr](function.strrchr.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strripos](function.strripos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strrpos](function.strrpos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strstr](function.strstr.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [unlink](function.unlink.md) | У Windows тепер можна видалити файли функцією unlink за допомогою дескрипторів, хоча раніше це не вдавалося. Тим не менш, все ще неможливо повторно створити віддалений файл, доки всі дескриптори до нього не будуть закриті. |
|  | [varexport](function.var-export.md) | Тепер об'єкти stdClass експортуються як масиву, приведеного до об'єкта (масив (object) array( ... )), замість використання неіснуючого методу stdClass::SetState. Практичний ефект полягає в тому, що тепер stdClass можна експортувати, і отриманий код працюватиме навіть у попередніх версіях PHP. |
|  | [xmlsetexternalentityrefhandler](function.xml-set-external-entity-ref-handler.md) | Значення handler, що повертається, більше не ігнорується, якщо модуль був зібраний з бібліотекою libxml. Раніше значення, що поверталося, ігнорувалося, а розбір ніколи не зупинявся. |
|  | [DatePeriod::construct](dateperiod.construct.md) | recurrences має бути більше 0. |
|  | [SplFileObject::toString](splfileobject.tostring.md) | Змінено псевдонім з SplFileObject::current на SplFileObject::fgets. |
|  | [substrcompare](function.substr-compare.md) | offset тепер може бути рівним haystack. |
|  | [arrayunique](function.array-unique.md) | Якщо flags дорівнює SORTSTRING раніше масив array копіювався, а не унікальні елементи видалялися (зберігаючи значення цифрових індексів), але тепер створюється новий масив шляхом додавання унікальних елементів. Це може призвести до різних числових індексів. |
|  | [assert](function.assert.md) | Використання рядків у параметрі assertion оголошено застарілим і призводитиме до помилок рівня EDEPRECATED у разі, коли і assert.active і zend.assertions встановлені значення 1. |
|  | [bcmod](function.bcmod.md) | Додано параметр scale. |
|  | [bcmod](function.bcmod.md) | num1 і num2 більше не обрізаються до цілого, тому тепер поведінка bcmod відповідає fmod, а не оператору %. |
|  | [count](function.count.md) | count тепер видаватиме попередження про неприпустимі обчислювані типи, передані в параметр value. |
|  | [dateparse](function.date-parse.md) | Елемент масива, що повертається, з ключем zone тепер містить секунди, а не хвилини. Крім того, знак інвертовано. Тобто. раніше було -120, а тепер 7200. |
|  | [dateparsefromformat](function.date-parse-from-format.md) | Елемент zone масиву, що повертається, відображає тепер секунди замість хвилин, а його знак інвертується. Наприклад, -120 тепер буде 7200. |
|  | [datesuninfo](function.date-sun-info.md) | Розрахунок був виправлений з урахуванням місцевої опівночі замість місцевого полудня, що дещо змінює результати. |
|  | [exifreaddata](function.exif-read-data.md) | Параметр file перейменований на stream і може приймати як локальний шлях до файлу, так і потоковий ресурс. |
|  | [exifreaddata](function.exif-read-data.md) | Додано підтримку наступних форматів EXIF: Samsung DJI Panasonic Sony Pentax Minolta Sigma/Foveon AGFA |
|  | [exifthumbnail](function.exif-thumbnail.md) | Параметр file перейменований на stream і може приймати як локальний шлях до файлу, так і потоковий ресурс. |
|  | [getclass](function.get-class.md) | До цієї версії значенням за умовчанням для object було null з тим самим ефектом, як і відсутність передачі значення. Тепер null був видалений як значення за промовчанням для object і більше не є допустимим значенням. |
|  | [gettype](function.gettype.md) | Для закритих ресурсів повертається 'resource (closed)'. Раніше для закритих ресурсів поверталося 'unknown type'. |
|  | [hashcopy](function.hash-copy.md) | Приймає та повертає HashContext, а не ресурс. |
|  | [hashfinal](function.hash-final.md) | Приймає HashContext, а не ресурс. |
|  | [hashhmac](function.hash-hmac.md) | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat). |
|  | [hashhmacfile](function.hash-hmac-file.md) | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat). |
|  | [hashinit](function.hash-init.md) | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat) з константою HASHHMAC. |
|  | [hashinit](function.hash-init.md) | Повертає HashContext, а не ресурс. |
|  | [hashpbkdf2](function.hash-pbkdf2.md) | Заборонено використання некриптографічних функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat). |
|  | [hashupdate](function.hash-update.md) | Приймає HashContext, а не ресурс. |
|  | [hashupdatefile](function.hash-update-file.md) | Приймає HashContext, а не ресурс. |
|  | [hashupdatestream](function.hash-update-stream.md) | Приймає HashContext, а не ресурс. |
|  | [idnтоascii](function.idn-to-ascii.md) | INTLIDNAVARIANT2003 оголошено застарілою, замість неї використовуйте INTLIDNAVARIANTUTS46. |
|  | [idnтоutf8](function.idn-to-utf8.md) | INTLIDNAVARIANT2003 оголошено застарілою, замість неї використовуйте INTLIDNAVARIANTUTS46. |
|  | [imageantialias](function.imageantialias.md) | Функція imageantialias доступна без обмежень. Раніше вона була доступна тільки якщо PHP був зібраний з використанням бібліотеки GD, що йде з ним в комплекті. |
|  | [imagegd](function.imagegd.md) | Тепер imagegd дозволяє зберігати зображення "truecolor". Раніше вони неявно перетворювалися на палітру. |
|  | [imagelayereffect](function.imagelayereffect.md) | Додана IMGEFFECTMULTIPLY (вимагає системну бібліотеку libgd >= 2.1.1 або libgd, що йде в комплекті з PHP). |
|  | [imagetypes](function.imagetypes.md) | Додано константу IMGBMP. |
|  | [ісobject](function.is-object.md) | Тепер isobject повертає true для десеріалізованих об'єктів, які не мають оголошення класу (клас PHPIncompleteClass). Раніше поверталося false. |
|  | [jsondecode](function.json-decode.md) | associative тепер nullable. |
|  | [jsondecode](function.json-decode.md) | Додані константи JSONINVALIDUTF8IGNORE та JSONINVALIDUTF8SUBSTITUTE для параметра flags. |
|  | [jsonencode](function.json-encode.md) | Додані константи JSONINVALIDUTF8IGNORE та JSONINVALIDUTF8SUBSTITUTE для параметра flags. |
|  | [mail](function.mail.md) | Параметр additionalheaders може набувати значень типу масив. |
|  | [мбcheckencoding](function.mb-check-encoding.md) | Функція тепер приймає масив (array) в value. Раніше підтримувалися лише рядки (string). |
|  | [мбconvertencoding](function.mb-convert-encoding.md) | Функція тепер приймає масив (array) в string. Раніше підтримувалися лише рядки (string). |
|  | [мбparsestr](function.mb-parse-str.md) | Виклик функції mbparsestr без другого параметра оголошено застарілим. |
|  | [мбsendmail](function.mb-send-mail.md) | Тепер у параметрі additionalheaders можна передавати масив. |
|  | [мтrand](function.mt-rand.md) | Для mtrand здійснено виправлення бага зміщення за модулем. Це означає, що послідовності згенеровані з конкретним початковим значенням можуть відрізнятися від згенерованих PHP 7.1 для 64-бітних машин. |
|  | [numberformat](function.number-format.md) | numberformat була змінена, щоб не повертати -0, раніше -0 могло бути повернено у випадках коли num був -0.01. |
|  | [opensslpkcs7verify](function.openssl-pkcs7-verify.md) | Додано параметр outputfilename. |
|  | [pack](function.pack.md) | Типи float і double підтримують як зворотний, і прямий порядок передачі байтів. |
|  | [parsestr](function.parse-str.md) | Використання parsestr без другого параметра буде викликати помилку рівня EDEPRECATED. |
|  | [passwordhash](function.password-hash.md) | Додано підтримку хешуючого алгоритму Argon2i за допомогою PASSWORDARGON2I. |
|  | [pregmatch](function.preg-match.md) | Тепер константа PREGUNMATCHEDАСNULL підтримується для параметра $flags. |
|  | [pregmatchall](function.preg-match-all.md) | Тепер константа PREGUNMATCHEDАСNULL підтримується для параметра $flags. |
|  | [pregquote](function.preg-quote.md) | delimiter тепер допускає значення null. |
|  | [procnice](function.proc-nice.md) | Ця функція стала доступною у Windows. |
|  | [rand](function.rand.md) | Для rand здійснено виправлення бага зміщення модулем. Це означає, що послідовності згенеровані з конкретним початковим значенням можуть відрізнятися від згенерованих PHP 7.1 для 64-бітних машин. |
|  | [readexifdata](function.read-exif-data.md) | Цей псевдонім було оголошено застарілим. |
|  | [sessionabort](function.session-abort.md) | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |
|  | [sessionmodulename](function.session-module-name.md) | Заборонено встановлювати ім'я модуля на значення "user". Раніше це ігнорувалося. |
|  | [sessionname](function.session-name.md) | sessionname перевіряє статус сесії, раніше вона перевіряла лише статус cookie. Тому стара версія sessionname дозволяла викликати sessionname після sessionstart, що могло призвести до збою PHP та неправильної поведінки. |
|  | [sessionreset](function.session-reset.md) | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |
|  | [sessionsetcookieparams](function.session-set-cookie-params.md) | Повертає true у разі успішного виконання або false у разі виникнення помилки. Раніше повертала тип void. |
|  | [sessionunset](function.session-unset.md) | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |
|  | [sessionwriteclose](function.session-write-close.md) | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |
|  | [seterrorhandler](function.set-error-handler.md) | Параметр errcontext оголошений застарілим. Тепер при його використанні викликатиметься помилка рівня EDEPRECATED. |
|  | [unpack](function.unpack.md) | Типи float і double підтримують як зворотний, і прямий порядок передачі байтів. |
|  | [utf8decode](function.utf8-decode.md) | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |
|  | [utf8encode](function.utf8-encode.md) | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |
|  | [PDOStatement::debugDumpParams](pdostatement.debugdumpparams.md) | PDOStatement::debugDumpParams тепер повертає SQL, надісланий у базу даних, у тому числі повний необроблений запит (включаючи замінені параметри зі своїми зв'язаними значеннями). Зверніть увагу, що це буде працювати тільки при включеній емуляції запитів, що готуються. |
|  | [ReflectionClass::getMethods](reflectionclass.getmethods.md) | filter тепер припускає значення null. |
|  | [ReflectionClass::getProperties](reflectionclass.getproperties.md) | filter тепер припускає значення null. |
|  | [SQLite3::openBlob](sqlite3.openblob.md) | Додано параметр flags, що дозволяє записати BLOB; раніше підтримувалося лише читання. |
|  | [xmlparsergetoption](function.xml-parser-get-option.md) | Тепер опція підтримує XMLOPTIONSKIPTAGSTART та XMLOPTIONSKIPWHITE. |
|  | [IntlDateFormatter::format](intldateformatter.format.md) | Додано підтримку надання загальних об'єктів DateTimeInterface для параметра datetime. Раніше підтримувалися лише об'єкти DateTime. |
|  | [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md) | Додано параметр flags. |
|  | [SQLite3::createFunction](sqlite3.createfunction.md) | Додано параметр flags. |
|  | [DateInterval::format](dateinterval.format.md) | Додані форматуючі символи F та f. |
|  | [DateTime::setTime](datetime.settime.md) | Додано параметр microsecond. |
|  | [DateTimeImmutable::construct](datetimeimmutable.construct.md) | Відтепер мікросекунди заповнюються фактичним значенням. Чи не '00000'. |
|  | [DateTimeImmutable::setTime](datetimeimmutable.settime.md) | Додано параметр microsecond. |
|  | [DateTimeZone::listIdentifiers](datetimezone.listidentifiers.md) | countryCode тепер припускає значення null. |
|  | [arrayrand](function.array-rand.md) | Внутрішній алгоритм отримання випадкових чисел змінено з функції rand бібліотеки libc на генератор з урахуванням Вихря Мерсенна. |
|  | [curlmultisetopt](function.curl-multi-setopt.md) | Додано константу CURLMOPTPUSHFUNCTION. |
|  | [exifimagetype](function.exif-imagetype.md) | Додано підтримку WebP. |
|  | [filegetcontents](function.file-get-contents.md) | Додано підтримку негативних значень offset. |
|  | [getheaders](function.get-headers.md) | Додано параметр context. |
|  | [getenv](function.getenv.md) | Параметр varname тепер може бути опущений для отримання асоціативного масиву всіх змінних оточення. |
|  | [getimagesize](function.getimagesize.md) | Додано підтримку WebP. |
|  | [getopt](function.getopt.md) | Додано параметр restindex. |
|  | [graphemeextract](function.grapheme-extract.md) | Додано підтримку негативних значень offset. |
|  | [graphemestripos](function.grapheme-stripos.md) | Додано підтримку негативних значень offset. |
|  | [graphemestrpos](function.grapheme-strpos.md) | Додано підтримку негативних значень offset. |
|  | [hashalgos](function.hash-algos.md) | Додана підтримка для sha512/224, sha512/256, sha3-224, sha3-256, sha3-384 та sha3-512. |
|  | [iconvstrpos](function.iconv-strpos.md) | Підтримка негативних значень offset. |
|  | [jsondecode](function.json-decode.md) | Порожній ключ JSON ("") буде перетворено на порожню властивість об'єкта, а не на властивість зі значенням empty |
|  | [jsonencode](function.json-encode.md) | При кодуванні чисел із плаваючою точкою використовується serializeprecision замість precision. |
|  | [jsonencode](function.json-encode.md) | Додано константу JSONUNESCAPEDLINETERMINATORS для параметра flags. |
|  | [list](function.list.md) | Тепер можна задавати ключі в List. Це дозволяє розіменовувати асоціативні масиви та масиви з індексами не по порядку. |
|  | [long2ip](function.long2ip.md) | Тип параметра ip змінено з типу string тип int. |
|  | [мбereg](function.mb-ereg.md) | Тепер mbereg встановлює matches рівним порожньому масиву (array), якщо нічого не знайдено. Раніше в цьому випадку матчі залишалися незмінними. |
|  | [мбeregreplace](function.mb-ereg-replace.md) | Модифікатор e оголошено застарілим. |
|  | [мбeregreplace](function.mb-ereg-replace.md) | Функція перевіряє, чи коректна string для поточного кодування. |
|  | [мбeregreplacecallback](function.mb-ereg-replace-callback.md) | Функція перевіряє, чи коректна string для поточного кодування. |
|  | [мбeregsearchsetpos](function.mb-ereg-search-setpos.md) | Додано підтримку негативних значень offset. |
|  | [мбeregi](function.mb-eregi.md) | Функцію mberegi встановлює значення матчів рівним порожньому масиву, якщо нічого не знайдено. Раніше, в такому випадку, матчі залишалися незмінними. |
|  | [мбeregireplace](function.mb-eregi-replace.md) | Модифікатор e оголошено застарілим. |
|  | [мбeregireplace](function.mb-eregi-replace.md) | Функція перевіряє, чи є string коректним рядком для поточного кодування. |
|  | [мбstrimwidth](function.mb-strimwidth.md) | Додано підтримку негативних start і width. |
|  | [мбstripos](function.mb-stripos.md) | Додано підтримку негативних значень offset. |
|  | [мбstrpos](function.mb-strpos.md) | Додано підтримку негативних значень offset. |
|  | [мтrand](function.mt-rand.md) | Функція mtrand було оновлено і тепер використовує коректну версію генератора випадкових чисел на основі Вихря Мерсенна. Для використання старої поведінки, використовуйте mtsrand з другим параметром, встановленим у MTRANDPHP. |
|  | [мтrand](function.mt-rand.md) | rand тепер є псевдонімом для mtrand. |
|  | [мтsrand](function.mt-srand.md) | мтrand була змінена для використання фіксованої коректної версії алгоритму Вихря Мерсенна. Для відкату до старої поведінки, використовуйте mtsrand із другим параметром MTRANDPHP. |
|  | [мтsrand](function.mt-srand.md) | srand тепер є псевдонімом для mtsrand. |
|  | [opensslcsrnew](function.openssl-csr-new.md) | Параметр options тепер підтримує curvename. |
|  | [openssldecrypt](function.openssl-decrypt.md) | Додані параметри tag та aad. |
|  | [opensslencrypt](function.openssl-encrypt.md) | Додані параметри tag, aad та taglength. |
|  | [opensslpkeynew](function.openssl-pkey-new.md) | Доданий ключ curvename в option для забезпечення можливості створення ключів EC. |
|  | [outputaddrewritevar](function.output-add-rewrite-var.md) | До PHP 7.1.0 змінні перезаписи, встановлені функцією outputaddrewritevar, використовують той самий буфер модуля сесії "trans sid". Починаючи з PHP 7.1.0, використовується окремий буфер, urlrewriter.tags використовується тільки для функцій виведення, додано urlrewriter.hosts. |
|  | [outputresetrewritevars](function.output-reset-rewrite-vars.md) | До PHP 7.1.0, змінні перезаписи встановлені функцією outputaddrewritevar використовують той самий буфер модуля сесії "trans sid". З PHP 7.1.0, використовується окремий буфер та outputresetrewritevars тільки видаляє змінні перезаписи певні outputaddrewritevar. |
|  | [pcntlsignal](function.pcntl-signal.md) | Починаючи з PHP 7.1.0 обробнику callback-функції передається другий аргумент, що містить структуру siginfo певного сигналу. Ці дані будуть передані тільки в тому випадку, якщо операційна система підтримує структури siginfot. Якщо в операційній системі не реалізовано підтримку структури siginfot, то як другий аргумент буде переданий NULL. |
|  | [pcntlsignalgethandler](function.pcntl-signal-get-handler.md) | Додано функцію pcntlsignalgethandler. |
|  | [пгfetchall](function.pg-fetch-all.md) | Додано параметр mode. |
|  | [пгlastnotice](function.pg-last-notice.md) | Додано параметр mode. |
|  | [пгselect](function.pg-select.md) | Додано параметр mode. |
|  | [rand](function.rand.md) | rand стала синонімом функції mtrand. |
|  | [sessionstart](function.session-start.md) | sessionstart тепер повертає false і більше не ініціалізує $SESSION коли вона не змогла запустити сесію. |
|  | [shuffle](function.shuffle.md) | Внутрішній алгоритм отримання випадкових чисел змінено з функції rand бібліотеки libc на генератор з урахуванням Вихря Мерсена. |
|  | [srand](function.srand.md) | srand стала синонімом функції mtsrand. |
|  | [strshuffle](function.str-shuffle.md) | Внутрішній алгоритм отримання випадкових чисел змінено з функції rand бібліотеки libc на генератор з урахуванням Вихря Мерсена. |
|  | [stripos](function.stripos.md) | Додано підтримку негативних значень offset. |
|  | [strpos](function.strpos.md) | Додано підтримку негативних значень offset. |
|  | [substrcount](function.substr-count.md) | Додано підтримку негативних значень offset і length. length тепер також може бути 0. |
|  | [tempnam](function.tempnam.md) | tempnam тепер видає повідомлення при поверненні до тимчасового каталогу системи. |
|  | [unpack](function.unpack.md) | Додано необов'язковий параметр offset. |
|  | [unserialize](function.unserialize.md) | Тепер елемент allowedclasses параметра options строго типізований, тобто якщо щось передано, крім array і bool, unserialize поверне false і викличе помилку EWARNING. |
|  | [ReflectionType::toString](reflectiontype.tostring.md) | ReflectionType::доString оголошено застарілим. |
|  | [SessionHandler::gc](sessionhandler.gc.md) | До цієї версії, у разі успішного виконання, ця функція повертала true. |
|  | [SessionHandlerInterface::gc](sessionhandlerinterface.gc.md) | До цієї версії, функція повертала true у разі успішного виконання. |
|  | [dnsgetrecord](function.dns-get-record.md) | Додано підтримку записів типу CAA. |
|  | [fopen](function.fopen.md) | Додано опцію 'e'. |
|  | [getdefinedfunctions](function.get-defined-functions.md) | Доданий параметр excludedisabled. |
|  | [pack](function.pack.md) | Додані коди "e", "E", "g" та "G" для підтримки примусової вказівки порядку байт для float та double. |
|  | [iconvsubstr](function.iconv-substr.md) | Якщо string має довжину рівну offset, буде повернуто порожній рядок. Раніше у таких випадках поверталося false. |
|  | [imagetypes](function.imagetypes.md) | Додано константу IMGWEBP. |
|  | [SplFileObject::getCsvControl](splfileobject.getcsvcontrol.md) | Доданий символ екранування до результуючого масиву. |
|  | [SQLite3::construct](sqlite3.construct.md) | Параметр filename можна задавати порожнім рядком для створення на диску приватної бази даних. |
|  | [getenv](function.getenv.md) | Додано параметр localтільки. |
|  | [curlmultisetopt](function.curl-multi-setopt.md) | Додано константи CURLMOPTCHUNKLENGTHPENALTYSIZE, CURLMOPTCONTENTLENGTHPENALTYSIZE, CURLMOPTMAXHOSTCONNECTIONS, CURLMOPTMAXPIPELINELENGTH та CURLMOPTMAXTOTALCONNECTIONS. |
|  | [curlsetopt](function.curl-setopt.md) | Додано CURLHTTPVERSION2, CURLHTTPVERSIONPRIORKNOWLEDGE, CURLHTTPVERSION2TLS, CURLREDIRPOST301, CURLREDIRPOST302, CURLREDIRPOST303, CURLREDIRPOSTALL, CURLVERSIONKERBEROS5, CURLVERSIONPSL, CURLVERSIONUNIXSOCKETS, CURLAUTHNEGOTIATE, CURLAUTHNTLMWB, CURLFTPCREATEDIR, CURLFTPCREATEDIRNONE, CURLFTPCREATEDIRRETRY, CURLHEADERSEPARATE, CURLHEADERUNIFIED, CURLMOPTCHUNKLENGTHPENALTYSIZE, CURLMOPTCONTENTLENGTHPENALTYSIZE, CURLMOPTMAXHOSTCONNECTIONS, CURLMOPTMAXPIPELINELENGTH, CURLMOPTMAXTOTALCONNECTIONS, CURLOPTCONNECTTO, CURLOPTDEFAULTPROTOCOL, CURLOPTDNSINTERFACE, CURLOPTDNSLOCALIP4, CURLOPTDNSLOCALIP6, CURLOPTEXPECTTIMEOUTMS, CURLOPTHEADEROPT, CURLOPTLOGINOPTIONS, CURLOPTPATHАСIS, CURLOPTPINNEDPUBLICKEY, CURLOPTPIPEWAIT, CURLOPTPROXYSERVICENAME, CURLOPTPROXYHEADER, CURLOPTSASLIR, CURLOPTSERVICENAME, CURLOPTSSLENABLEALPN, CURLOPTSSLENABLENPN, CURLOPTSSLFALSESTART, CURLOPTSSLVERIFYSTATUS, CURLOPTSTREAMWEIGHT, CURLOPTTCPFASTOPEN, CURLOPTTFTPАЛЕOPTIONS, CURLOPTUNIXSOCKETPATH, CURLOPTXOAUTH2BEARER, CURLPROTOSMB, CURLPROTOSMBS, CURLPROXYHTTP0, CURLSSHAUTHAGENT та CURLSSLOPTАЛЕREVOKE. |
|  | [assert](function.assert.md) | assert тепер мовна конструкція, а не функція. asertion тепер може бути виразом. Другий параметр тепер інтерпретується як виняток exception (якщо передано об'єкт Throwable), або як опис description, який підтримується з версії PHP 5.4.8 і далі. |
|  | [define](function.define.md) | Допустимі значення типу array. |
|  | [dirname](function.dirname.md) | Додано необов'язковий параметр рівнів. |
|  | [getrusage](function.getrusage.md) | Додано підтримку цієї функції у Windows. |
| 5.5.0/PECL 3.0.0 | [IntlDateFormatter::create](intldateformatter.create.md) | Об'єкт IntlCalendar допускається у параметрі calendar. Об'єкти IntlTimeZone та DateTimeZone допускаються у параметрі timezone. Неприпустимі ідентифікатори часового поясу (включаючи порожні рядки) більше не допускаються у параметрі timezone. Якщо у параметрі timezone вказано значення null, ідентифікатор часового поясу, заданий datedefaulttimezoneget, використовуватиметься замість значення ICU за замовчуванням. |
|  | [IntlDateFormatter::setCalendar](intldateformatter.setcalendar.md) | Додано можливість передати об'єкт IntlCalendar. |
