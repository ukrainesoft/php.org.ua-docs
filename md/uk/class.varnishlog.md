---
navigation:
  - varnishstat.getsnapshot.md: '« VarnishStat::getSnapshot'
  - varnishlog.construct.md: 'VarnishLog::construct »'
  - index.md: PHP Manual
  - book.varnish.md: Varnish
title: Клас VarnishLog
---
# Клас VarnishLog

(PECL varnish >= 0.6)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class VarnishLog
     
     {

    /* Constants */
    
     const
     int
      TAG_Debug = 0;

    const
     int
      TAG_Error = 1;

    const
     int
      TAG_CLI = 2;

    const
     int
      TAG_StatSess = 3;

    const
     int
      TAG_ReqEnd = 4;

    const
     int
      TAG_SessionOpen = 5;

    const
     int
      TAG_SessionClose = 6;

    const
     int
      TAG_BackendOpen = 7;

    const
     int
      TAG_BackendXID = 8;

    const
     int
      TAG_BackendReuse = 9;

    const
     int
      TAG_BackendClose = 10;

    const
     int
      TAG_HttpGarbage = 11;

    const
     int
      TAG_Backend = 12;

    const
     int
      TAG_Length = 13;

    const
     int
      TAG_FetchError = 14;

    const
     int
      TAG_RxRequest = 15;

    const
     int
      TAG_RxResponse = 16;

    const
     int
      TAG_RxStatus = 17;

    const
     int
      TAG_RxURL = 18;

    const
     int
      TAG_RxProtocol = 19;

    const
     int
      TAG_RxHeader = 20;

    const
     int
      TAG_TxRequest = 21;

    const
     int
      TAG_TxResponse = 22;

    const
     int
      TAG_TxStatus = 23;

    const
     int
      TAG_TxURL = 24;

    const
     int
      TAG_TxProtocol = 25;

    const
     int
      TAG_TxHeader = 26;

    const
     int
      TAG_ObjRequest = 27;

    const
     int
      TAG_ObjResponse = 28;

    const
     int
      TAG_ObjStatus = 29;

    const
     int
      TAG_ObjURL = 30;

    const
     int
      TAG_ObjProtocol = 31;

    const
     int
      TAG_ObjHeader = 32;

    const
     int
      TAG_LostHeader = 33;

    const
     int
      TAG_TTL = 34;

    const
     int
      TAG_Fetch_Body = 35;

    const
     int
      TAG_VCL_acl = 36;

    const
     int
      TAG_VCL_call = 37;

    const
     int
      TAG_VCL_trace = 38;

    const
     int
      TAG_VCL_return = 39;

    const
     int
      TAG_VCL_error = 40;

    const
     int
      TAG_ReqStart = 41;

    const
     int
      TAG_Hit = 42;

    const
     int
      TAG_HitPass = 43;

    const
     int
      TAG_ExpBan = 44;

    const
     int
      TAG_ExpKill = 45;

    const
     int
      TAG_WorkThread = 46;

    const
     int
      TAG_ESI_xmlerror = 47;

    const
     int
      TAG_Hash = 48;

    const
     int
      TAG_Backend_health = 49;

    const
     int
      TAG_VCL_Log = 50;

    const
     int
      TAG_Gzip = 51;


    /* Методы */
    
   public __construct(array $args = ?)
public getLine(): array
public static getTagName(int $index): string

   }
```

## Обумовлені константи

**`VarnishLog::TAG_Debug`**

**`VarnishLog::TAG_Error`**

**`VarnishLog::TAG_CLI`**

**`VarnishLog::TAG_StatSess`**

**`VarnishLog::TAG_ReqEnd`**

**`VarnishLog::TAG_SessionOpen`**

**`VarnishLog::TAG_SessionClose`**

**`VarnishLog::TAG_BackendOpen`**

**`VarnishLog::TAG_BackendXID`**

**`VarnishLog::TAG_BackendReuse`**

**`VarnishLog::TAG_BackendClose`**

**`VarnishLog::TAG_HttpGarbage`**

**`VarnishLog::TAG_Backend`**

**`VarnishLog::TAG_Length`**

**`VarnishLog::TAG_FetchError`**

**`VarnishLog::TAG_RxRequest`**

**`VarnishLog::TAG_RxResponse`**

**`VarnishLog::TAG_RxStatus`**

**`VarnishLog::TAG_RxURL`**

**`VarnishLog::TAG_RxProtocol`**

**`VarnishLog::TAG_RxHeader`**

**`VarnishLog::TAG_TxRequest`**

**`VarnishLog::TAG_TxResponse`**

**`VarnishLog::TAG_TxStatus`**

**`VarnishLog::TAG_TxURL`**

**`VarnishLog::TAG_TxProtocol`**

**`VarnishLog::TAG_TxHeader`**

**`VarnishLog::TAG_ObjRequest`**

**`VarnishLog::TAG_ObjResponse`**

**`VarnishLog::TAG_ObjStatus`**

**`VarnishLog::TAG_ObjURL`**

**`VarnishLog::TAG_ObjProtocol`**

**`VarnishLog::TAG_ObjHeader`**

**`VarnishLog::TAG_LostHeader`**

**`VarnishLog::TAG_TTL`**

**`VarnishLog::TAG_Fetch_Body`**

**`VarnishLog::TAG_VCL_acl`**

**`VarnishLog::TAG_VCL_call`**

**`VarnishLog::TAG_VCL_trace`**

**`VarnishLog::TAG_VCL_return`**

**`VarnishLog::TAG_VCL_error`**

**`VarnishLog::TAG_ReqStart`**

**`VarnishLog::TAG_Hit`**

**`VarnishLog::TAG_HitPass`**

**`VarnishLog::TAG_ExpBan`**

**`VarnishLog::TAG_ExpKill`**

**`VarnishLog::TAG_WorkThread`**

**`VarnishLog::TAG_ESI_xmlerror`**

**`VarnishLog::TAG_Hash`**

**`VarnishLog::TAG_Backend_health`**

**`VarnishLog::TAG_VCL_Log`**

**`VarnishLog::TAG_Gzip`**

## Зміст

-   [VarnishLog::construct](varnishlog.construct.md) - Конструктор Varnishlog
-   [VarnishLog::getLine](varnishlog.getline.md) — Отримати наступний рядок журналу
-   [VarnishLog::getTagName](varnishlog.gettagname.md) — Отримати строкове подання тега журналу за його індексом
