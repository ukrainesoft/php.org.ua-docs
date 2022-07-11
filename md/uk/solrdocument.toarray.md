- [«SolrDocument::sort](solrdocument.sort.md)
- [SolrDocument::unserialize »](solrdocument.unserialize.md)

- [PHP Manual](index.md)
- [SolrDocument](class.solrdocument.md)
- Повертає подання масиву документа

# SolrDocument::toArray

(PECL solr \> = 0.9.2)

SolrDocument::toArray — Повертає представлення масиву документа

### Опис

public **SolrDocument::toArray**(): array

Повертає представлення масиву документа.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає представлення масиву документа.

### Приклади

**Приклад #1 Приклад використання **SolrDocument::toArray()****

` <?php$doc = new SolrDocument();$doc->addField('id', 1123);$doc->features = "PHP Client Side";$doc->features = "Fast development cycles" doc['cat'] = 'Software';$doc['cat'] = 'Custom Search';$doc->cat   = 'Information Technology';print_r($doc->toArray());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[document_boost] => 0
[field_count] => 3
[fields] => Array
(
[0] => SolrDocumentField Object
(
[name] => id
[boost] => 0
[values] => Array
(
[0] => 1123
)

)

[1] => SolrDocumentField Object
(
[name] => features
[boost] => 0
[values] => Array
(
[0] => PHP Client Side
[1] => Fast development cycles
)

)

[2] => SolrDocumentField Object
(
[name] => cat
[boost] => 0
[values] => Array
(
[0] => Software
[1] => Custom Search
[2] => Information Technology
)

)

)

)
