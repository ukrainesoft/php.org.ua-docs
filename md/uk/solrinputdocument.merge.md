Об'єднує один вхідний документ в інший

-   [« SolrInputDocument::hasChildDocuments](solrinputdocument.haschilddocuments.md)
    
-   [SolrInputDocument::reset »](solrinputdocument.reset.md)
    
-   [PHP Manual](index.md)
    
-   [SolrInputDocument](class.solrinputdocument.md)
    
-   Об'єднує один вхідний документ в інший
    

# SolrInputDocument::merge

(PECL solr> = 0.9.2)

SolrInputDocument::merge — Об'єднує один вхідний документ до іншого

### Опис

```methodsynopsis
public SolrInputDocument::merge(SolrInputDocument $sourceDoc, bool $overwrite = true): bool
```

Об'єднує один вхідний документ до іншого.

### Список параметрів

`sourceDoc`

Початковий документ.

`overwrite`

Якщо вказано **`true`**, відповідні поля у цільовому документі будуть перезаписані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. У майбутньому це буде змінено, щоб повертати кількість полів у новому документі.