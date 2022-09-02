---
navigation:
  - extensions.state.md: '" Станом'
  - reserved.md: Список зарезервованих слів »
  - index.md: PHP Manual
  - appendices.md: Appendices
title: Список псевдонімів функцій
---
# Список псевдонімів функцій

У PHP досить багато функцій, доступних відразу за кількома іменами. У деяких випадках немає варіанта, що віддається переваги, хорошим прикладом є [ісint()](function.is-int.md) і [ісinteger()](function.is-integer.md). Однак, є функції, що змінили свої назви внаслідок чищення API або з іншої причини, а старі імена були залишені з метою зворотної сумісності. Зазвичай не рекомендується використовувати ці псевдоніми, оскільки причиною їхнього існування може бути старіння або зміна імені основної функції, що може призвести до проблем портування скрипта. Цей список надається для оновлення старих скриптів до нового синтаксису.

**Псевдоніми**

| Псевдоним | Основная функция | Модуль |
| --- | --- | --- |
|  | [gettext()](function.gettext.md) | [Gettext](ref.gettext.md) |
| chop | [rtrim()](function.rtrim.md) | Базовий синтаксис |
| close | [closedir()](function.closedir.md) | Базовий синтаксис |
| comget | **compropget()** | [COM](ref.com.md) |
| compropset | **compropput()** | [COM](ref.com.md) |
| comset | **compropput()** | [COM](ref.com.md) |
| die | [exit()](function.exit.md) | [Некласифіковані функції](ref.misc.md) |
| diskfreespace | [diskfreespace()](function.disk-free-space.md) | [Файлова система](ref.filesystem.md) |
| doubleval | [floatval()](function.floatval.md) | Базовий синтаксис |
| fputs | [fwrite()](function.fwrite.md) | Базовий синтаксис |
| gzputs | [gzwrite()](function.gzwrite.md) | [Zlib](ref.zlib.md) |
| i18nconvert | [мбconvertencoding()](function.mb-convert-encoding.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18ndiscoverencoding | [мбdetectencoding()](function.mb-detect-encoding.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18nhttpinput | [мбhttpinput()](function.mb-http-input.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18nhttpoutput | [мбhttpoutput()](function.mb-http-output.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18ninternalencoding | [мбinternalencoding()](function.mb-internal-encoding.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18nяжпhantozen | [мбconvertkana()](function.mb-convert-kana.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18nmimeheaderdecode | [мбdecodemimeheader()](function.mb-decode-mimeheader.md) | [Багатобайтові рядки](ref.mbstring.md) |
| i18nmimeheaderencode | [мбencodemimeheader()](function.mb-encode-mimeheader.md) | [Багатобайтові рядки](ref.mbstring.md) |
| imapcreate | [imapcreatemailbox()](function.imap-createmailbox.md) | [IMAP](ref.imap.md) |
| imapfetchtext | [imapbody()](function.imap-body.md) | [IMAP](ref.imap.md) |
| imapgetmailboxes | **imaplistfull()** | [IMAP](ref.imap.md) |
| imapgetsubscribed | **imaplsubfull()** | [IMAP](ref.imap.md) |
| imapheader | [imapheaderinfo()](function.imap-headerinfo.md) | [IMAP](ref.imap.md) |
| imaplistmailbox | [imaplist()](function.imap-list.md) | [IMAP](ref.imap.md) |
| imaplistsubscribed | [imaplsub()](function.imap-lsub.md) | [IMAP](ref.imap.md) |
| imaprename | [imaprenamemailbox()](function.imap-renamemailbox.md) | [IMAP](ref.imap.md) |
| imapscan | [imaplistscan()](function.imap-listscan.md) | [IMAP](ref.imap.md) |
| imapscanmailbox | [imaplistscan()](function.imap-listscan.md) | [IMAP](ref.imap.md) |
| inialter | [iniset()](function.ini-set.md) | Базовий синтаксис |
| ісdouble | [ісfloat()](function.is-float.md) | Базовий синтаксис |
| ісinteger | [ісint()](function.is-int.md) | Базовий синтаксис |
| ісlong | [ісint()](function.is-int.md) | Базовий синтаксис |
| ісreal | [ісfloat()](function.is-float.md) | Базовий синтаксис |
| ісwriteable | [ісwritable()](function.is-writable.md) | Базовий синтаксис |
| join | [implode()](function.implode.md) | Базовий синтаксис |
| keyexists | [arraykeyexists()](function.array-key-exists.md) | Базовий синтаксис |
| ldapclose | [ldapunbind()](function.ldap-unbind.md) | [LDAP](ref.ldap.md) |
| mbstrcut | [мбstrcut()](function.mb-strcut.md) | [Багатобайтові рядки](ref.mbstring.md) |
| mbstrlen | [мбstrlen()](function.mb-strlen.md) | [Багатобайтові рядки](ref.mbstring.md) |
| mbstrpos | [мбstrpos()](function.mb-strpos.md) | [Багатобайтові рядки](ref.mbstring.md) |
| mbstrrpos | [мбstrrpos()](function.mb-strrpos.md) | [Багатобайтові рядки](ref.mbstring.md) |
| mbsubstr | [мбsubstr()](function.mb-substr.md) | [Багатобайтові рядки](ref.mbstring.md) |
| mysql | [mysqlдбquery()](function.mysql-db-query.md) | [MySQL](ref.mysql.md) |
| mysqlcreatedb | [mysqlcreatedb()](function.mysql-create-db.md) | [MySQL](ref.mysql.md) |
| mysqlдбname | [mysqlresult()](function.mysql-result.md) | [MySQL](ref.mysql.md) |
| mysqldbname | [mysqlresult()](function.mysql-result.md) | [MySQL](ref.mysql.md) |
| mysqldropdb | [mysqldropdb()](function.mysql-drop-db.md) | [MySQL](ref.mysql.md) |
| mysqlfieldflags | [mysqlfieldflags()](function.mysql-field-flags.md) | [MySQL](ref.mysql.md) |
| mysqlfieldlen | [mysqlfieldlen()](function.mysql-field-len.md) | [MySQL](ref.mysql.md) |
| mysqlfieldname | [mysqlfieldname()](function.mysql-field-name.md) | [MySQL](ref.mysql.md) |
| mysqlfieldtable | [mysqlfieldtable()](function.mysql-field-table.md) | [MySQL](ref.mysql.md) |
| mysqlfieldtype | [mysqlfieldtype()](function.mysql-field-type.md) | [MySQL](ref.mysql.md) |
| mysqlfreeresult | [mysqlfreeresult()](function.mysql-free-result.md) | [MySQL](ref.mysql.md) |
| mysqllistdbs | [mysqllistdbs()](function.mysql-list-dbs.md) | [MySQL](ref.mysql.md) |
| mysqllistfields | [mysqllistfields()](function.mysql-list-fields.md) | [MySQL](ref.mysql.md) |
| mysqllisttables | [mysqllisttables()](function.mysql-list-tables.md) | [MySQL](ref.mysql.md) |
| mysqlnumfields | [mysqlnumfields()](function.mysql-num-fields.md) | [MySQL](ref.mysql.md) |
| mysqlnumrows | [mysqlnumrows()](function.mysql-num-rows.md) | [MySQL](ref.mysql.md) |
| mysqlselectdb | [mysqlselectdb()](function.mysql-select-db.md) | [MySQL](ref.mysql.md) |
| mysqltablename | [mysqlresult()](function.mysql-result.md) | [MySQL](ref.mysql.md) |
| ociassignelem | [OCICollection::assignElem](ocicollection.assignelem.md) | [OCI8](ref.oci8.md) |
| ocibindbyname | [ocibindбname()](function.oci-bind-by-name.md) | [OCI8](ref.oci8.md) |
| ocicancel | [ocicancel()](function.oci-cancel.md) | [OCI8](ref.oci8.md) |
| ocicloselob | [OCILob::close](ocilob.close.md) | [OCI8](ref.oci8.md) |
| ocicollappend | [OCICollection::append](ocicollection.append.md) | [OCI8](ref.oci8.md) |
| ocicollassign | [OCICollection::assign](ocicollection.assign.md) | [OCI8](ref.oci8.md) |
| ocicollmax | [OCICollection::max](ocicollection.max.md) | [OCI8](ref.oci8.md) |
| ocicollsize | [OCICollection::size](ocicollection.size.md) | [OCI8](ref.oci8.md) |
| ocicolltrim | [OCICollection::trim](ocicollection.trim.md) | [OCI8](ref.oci8.md) |
| ocicolumnisnull | [ocifieldісnull()](function.oci-field-is-null.md) | [OCI8](ref.oci8.md) |
| ocicolumnname | [ocifieldname()](function.oci-field-name.md) | [OCI8](ref.oci8.md) |
| ocicolumnprecision | [ocifieldprecision()](function.oci-field-precision.md) | [OCI8](ref.oci8.md) |
| ocicolumnscale | [ocifieldscale()](function.oci-field-scale.md) | [OCI8](ref.oci8.md) |
| ocicolumnsize | [ocifieldsize()](function.oci-field-size.md) | [OCI8](ref.oci8.md) |
| ocicolumntype | [ocifieldtype()](function.oci-field-type.md) | [OCI8](ref.oci8.md) |
| ocicolumntyperaw | [ocifieldtyperaw()](function.oci-field-type-raw.md) | [OCI8](ref.oci8.md) |
| ocicommit | [ocicommit()](function.oci-commit.md) | [OCI8](ref.oci8.md) |
| ocidefinebyname | [ocidefineбname()](function.oci-define-by-name.md) | [OCI8](ref.oci8.md) |
| ocierror | [ocierror()](function.oci-error.md) | [OCI8](ref.oci8.md) |
| ociexecute | [ociexecute()](function.oci-execute.md) | [OCI8](ref.oci8.md) |
| ocifetch | [ocifetch()](function.oci-fetch.md) | [OCI8](ref.oci8.md) |
| ocifetchinto | [ocifetcharray()](function.oci-fetch-array.md) [ocifetchrow()](function.oci-fetch-row.md) [ocifetchassoc()](function.oci-fetch-assoc.md) [ocifetchobject()](function.oci-fetch-object.md) | [OCI8](ref.oci8.md) |
| ocifetchstatement | [ocifetchall()](function.oci-fetch-all.md) | [OCI8](ref.oci8.md) |
| ocifreecollection | [OCICollection::free](ocicollection.free.md) | [OCI8](ref.oci8.md) |
| ocifreecursor | [ocifreestatement()](function.oci-free-statement.md) | [OCI8](ref.oci8.md) |
| ocifreedesc | [ocifreedescriptor()](function.oci-free-descriptor.md) | [OCI8](ref.oci8.md) |
| ocifreestatement | [ocifreestatement()](function.oci-free-statement.md) | [OCI8](ref.oci8.md) |
| ocigetelem | [OCICollection::getElem](ocicollection.getelem.md) | [OCI8](ref.oci8.md) |
| ociinternaldebug | [ociinternaldebug()](function.oci-internal-debug.md) | [OCI8](ref.oci8.md) |
| ociloadlob | [OCILob::load](ocilob.load.md) | [OCI8](ref.oci8.md) |
| ocilogon | [ociconnect()](function.oci-connect.md) | [OCI8](ref.oci8.md) |
| ocinewcollection | [ocinewcollection()](function.oci-new-collection.md) | [OCI8](ref.oci8.md) |
| ocinewcursor | [ocinewcursor()](function.oci-new-cursor.md) | [OCI8](ref.oci8.md) |
| ocinewdescriptor | [ocinewdescriptor()](function.oci-new-descriptor.md) | [OCI8](ref.oci8.md) |
| ocinlogon | [ocinewconnect()](function.oci-new-connect.md) | [OCI8](ref.oci8.md) |
| ocinumcols | [ocinumfields()](function.oci-num-fields.md) | [OCI8](ref.oci8.md) |
| ociparse | [ociparse()](function.oci-parse.md) | [OCI8](ref.oci8.md) |
| ocipasswordchange | [ocipasswordchange()](function.oci-password-change.md) | [OCI8](ref.oci8.md) |
| ociplogon | [ocipconnect()](function.oci-pconnect.md) | [OCI8](ref.oci8.md) |
| ociresult | [ociresult()](function.oci-result.md) | [OCI8](ref.oci8.md) |
| ocirollback | [ocirollback()](function.oci-rollback.md) | [OCI8](ref.oci8.md) |
| ocisavelob | [OCILob::save](ocilob.save.md) | [OCI8](ref.oci8.md) |
| ocisavelobfile | [OCILob::import](ocilob.import.md) | [OCI8](ref.oci8.md) |
| ociserverversion | [ociserverversion()](function.oci-server-version.md) | [OCI8](ref.oci8.md) |
| ocisetprefetch | [ocisetprefetch()](function.oci-set-prefetch.md) | [OCI8](ref.oci8.md) |
| ocistatementtype | [ocistatementtype()](function.oci-statement-type.md) | [OCI8](ref.oci8.md) |
| ociwritelobtofile | [OCILob::export](ocilob.export.md) | [OCI8](ref.oci8.md) |
| ociwritetemporarylob | [OCILob::writeTemporary](ocilob.writetemporary.md) | [OCI8](ref.oci8.md) |
| odbcдо | [odbcexec()](function.odbc-exec.md) | [ODBC](ref.uodbc.md) |
| odbcfieldprecision | [odbcfieldlen()](function.odbc-field-len.md) | [ODBC](ref.uodbc.md) |
| пгclientencoding | [пгclientencoding()](function.pg-client-encoding.md) | [PostgreSQL](ref.pgsql.md) |
| пгsetclientencoding | [пгsetclientencoding()](function.pg-set-client-encoding.md) | [PostgreSQL](ref.pgsql.md) |
| pos | [current()](function.current.md) | Базовий синтаксис |
| recode | [recodestring()](function.recode-string.md) | [Recode](ref.recode.md) |
| showsource | [highlightfile()](function.highlight-file.md) | Базовий синтаксис |
| sizeof | [count()](function.count.md) | Базовий синтаксис |
| snmpwalkoid | [snmprealwalk()](function.snmprealwalk.md) | [SNMP](ref.snmp.md) |
| strchr | [strstr()](function.strstr.md) | Базовий синтаксис |
| xptrnewcontext | **xpathnewcontext()** |  |
