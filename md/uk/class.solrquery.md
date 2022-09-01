---
navigation:
  - solrmodifiableparams.destruct.md: '« SolrModifiableParams::destruct'
  - solrquery.addexpandfilterquery.md: 'SolrQuery::addExpandFilterQuery »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrQuery
---
# Клас SolrQuery

(PECL solr> = 0.9.2)

## Вступ

Надає колекцію пар ім'я-значення, відправлену на сервер Solr під час запиту.

## Огляд класів

```classsynopsis



    
     
      class SolrQuery
     

     
      extends
       SolrModifiableParams
     

     implements 
       Serializable {

    /* Константы */
    
     const
     int
      ORDER_ASC = 0;

    const
     int
      ORDER_DESC = 1;

    const
     int
      FACET_SORT_INDEX = 0;

    const
     int
      FACET_SORT_COUNT = 1;

    const
     int
      TERMS_SORT_INDEX = 0;

    const
     int
      TERMS_SORT_COUNT = 1;


    /* Свойства */


    /* Методы */
    
   public __construct(string $q = ?)

    public addExpandFilterQuery(string $fq): SolrQuery
public addExpandSortField(string $field, string $order = ?): SolrQuery
public addFacetDateField(string $dateField): SolrQuery
public addFacetDateOther(string $value, string $field_override = ?): SolrQuery
public addFacetField(string $field): SolrQuery
public addFacetQuery(string $facetQuery): SolrQuery
public addField(string $field): SolrQuery
public addFilterQuery(string $fq): SolrQuery
public addGroupField(string $value): SolrQuery
public addGroupFunction(string $value): SolrQuery
public addGroupQuery(string $value): SolrQuery
public addGroupSortField(string $field, int $order = ?): SolrQuery
public addHighlightField(string $field): SolrQuery
public addMltField(string $field): SolrQuery
public addMltQueryField(string $field, float $boost): SolrQuery
public addSortField(string $field, int $order = SolrQuery::ORDER_DESC): SolrQuery
public addStatsFacet(string $field): SolrQuery
public addStatsField(string $field): SolrQuery
public collapse(SolrCollapseFunction $collapseFunction): SolrQuery
public getExpand(): bool
public getExpandFilterQueries(): array
public getExpandQuery(): array
public getExpandRows(): int
public getExpandSortFields(): array
public getFacet(): bool
public getFacetDateEnd(string $field_override = ?): string
public getFacetDateFields(): array
public getFacetDateGap(string $field_override = ?): string
public getFacetDateHardEnd(string $field_override = ?): string
public getFacetDateOther(string $field_override = ?): array
public getFacetDateStart(string $field_override = ?): string
public getFacetFields(): array
public getFacetLimit(string $field_override = ?): int
public getFacetMethod(string $field_override = ?): string
public getFacetMinCount(string $field_override = ?): int
public getFacetMissing(string $field_override = ?): bool
public getFacetOffset(string $field_override = ?): int
public getFacetPrefix(string $field_override = ?): string
public getFacetQueries(): array
public getFacetSort(string $field_override = ?): int
public getFields(): array
public getFilterQueries(): array
public getGroup(): bool
public getGroupCachePercent(): int
public getGroupFacet(): bool
public getGroupFields(): array
public getGroupFormat(): string
public getGroupFunctions(): array
public getGroupLimit(): int
public getGroupMain(): bool
public getGroupNGroups(): bool
public getGroupOffset(): int
public getGroupQueries(): array
public getGroupSortFields(): array
public getGroupTruncate(): bool
public getHighlight(): bool
public getHighlightAlternateField(string $field_override = ?): string
public getHighlightFields(): array
public getHighlightFormatter(string $field_override = ?): string
public getHighlightFragmenter(string $field_override = ?): string
public getHighlightFragsize(string $field_override = ?): int
public getHighlightHighlightMultiTerm(): bool
public getHighlightMaxAlternateFieldLength(string $field_override = ?): int
public getHighlightMaxAnalyzedChars(): int
public getHighlightMergeContiguous(string $field_override = ?): bool
public getHighlightRegexMaxAnalyzedChars(): int
public getHighlightRegexPattern(): string
public getHighlightRegexSlop(): float
public getHighlightRequireFieldMatch(): bool
public getHighlightSimplePost(string $field_override = ?): string
public getHighlightSimplePre(string $field_override = ?): string
public getHighlightSnippets(string $field_override = ?): int
public getHighlightUsePhraseHighlighter(): bool
public getMlt(): bool
public getMltBoost(): bool
public getMltCount(): int
public getMltFields(): array
public getMltMaxNumQueryTerms(): int
public getMltMaxNumTokens(): int
public getMltMaxWordLength(): int
public getMltMinDocFrequency(): int
public getMltMinTermFrequency(): int
public getMltMinWordLength(): int
public getMltQueryFields(): array
public getQuery(): string
public getRows(): int
public getSortFields(): array
public getStart(): int
public getStats(): bool
public getStatsFacets(): array
public getStatsFields(): array
public getTerms(): bool
public getTermsField(): string
public getTermsIncludeLowerBound(): bool
public getTermsIncludeUpperBound(): bool
public getTermsLimit(): int
public getTermsLowerBound(): string
public getTermsMaxCount(): int
public getTermsMinCount(): int
public getTermsPrefix(): string
public getTermsReturnRaw(): bool
public getTermsSort(): int
public getTermsUpperBound(): string
public getTimeAllowed(): int
public removeExpandFilterQuery(string $fq): SolrQuery
public removeExpandSortField(string $field): SolrQuery
public removeFacetDateField(string $field): SolrQuery
public removeFacetDateOther(string $value, string $field_override = ?): SolrQuery
public removeFacetField(string $field): SolrQuery
public removeFacetQuery(string $value): SolrQuery
public removeField(string $field): SolrQuery
public removeFilterQuery(string $fq): SolrQuery
public removeHighlightField(string $field): SolrQuery
public removeMltField(string $field): SolrQuery
public removeMltQueryField(string $queryField): SolrQuery
public removeSortField(string $field): SolrQuery
public removeStatsFacet(string $value): SolrQuery
public removeStatsField(string $field): SolrQuery
public setEchoHandler(bool $flag): SolrQuery
public setEchoParams(string $type): SolrQuery
public setExpand(bool $value): SolrQuery
public setExpandQuery(string $q): SolrQuery
public setExpandRows(int $value): SolrQuery
public setExplainOther(string $query): SolrQuery
public setFacet(bool $flag): SolrQuery
public setFacetDateEnd(string $value, string $field_override = ?): SolrQuery
public setFacetDateGap(string $value, string $field_override = ?): SolrQuery
public setFacetDateHardEnd(bool $value, string $field_override = ?): SolrQuery
public setFacetDateStart(string $value, string $field_override = ?): SolrQuery
public setFacetEnumCacheMinDefaultFrequency(int $frequency, string $field_override = ?): SolrQuery
public setFacetLimit(int $limit, string $field_override = ?): SolrQuery
public setFacetMethod(string $method, string $field_override = ?): SolrQuery
public setFacetMinCount(int $mincount, string $field_override = ?): SolrQuery
public setFacetMissing(bool $flag, string $field_override = ?): SolrQuery
public setFacetOffset(int $offset, string $field_override = ?): SolrQuery
public setFacetPrefix(string $prefix, string $field_override = ?): SolrQuery
public setFacetSort(int $facetSort, string $field_override = ?): SolrQuery
public setGroup(bool $value): SolrQuery
public setGroupCachePercent(int $percent): SolrQuery
public setGroupFacet(bool $value): SolrQuery
public setGroupFormat(string $value): SolrQuery
public setGroupLimit(int $value): SolrQuery
public setGroupMain(string $value): SolrQuery
public setGroupNGroups(bool $value): SolrQuery
public setGroupOffset(int $value): SolrQuery
public setGroupTruncate(bool $value): SolrQuery
public setHighlight(bool $flag): SolrQuery
public setHighlightAlternateField(string $field, string $field_override = ?): SolrQuery
public setHighlightFormatter(string $formatter, string $field_override = ?): SolrQuery
public setHighlightFragmenter(string $fragmenter, string $field_override = ?): SolrQuery
public setHighlightFragsize(int $size, string $field_override = ?): SolrQuery
public setHighlightHighlightMultiTerm(bool $flag): SolrQuery
public setHighlightMaxAlternateFieldLength(int $fieldLength, string $field_override = ?): SolrQuery
public setHighlightMaxAnalyzedChars(int $value): SolrQuery
public setHighlightMergeContiguous(bool $flag, string $field_override = ?): SolrQuery
public setHighlightRegexMaxAnalyzedChars(int $maxAnalyzedChars): SolrQuery
public setHighlightRegexPattern(string $value): SolrQuery
public setHighlightRegexSlop(float $factor): SolrQuery
public setHighlightRequireFieldMatch(bool $flag): SolrQuery
public setHighlightSimplePost(string $simplePost, string $field_override = ?): SolrQuery
public setHighlightSimplePre(string $simplePre, string $field_override = ?): SolrQuery
public setHighlightSnippets(int $value, string $field_override = ?): SolrQuery
public setHighlightUsePhraseHighlighter(bool $flag): SolrQuery
public setMlt(bool $flag): SolrQuery
public setMltBoost(bool $flag): SolrQuery
public setMltCount(int $count): SolrQuery
public setMltMaxNumQueryTerms(int $value): SolrQuery
public setMltMaxNumTokens(int $value): SolrQuery
public setMltMaxWordLength(int $maxWordLength): SolrQuery
public setMltMinDocFrequency(int $minDocFrequency): SolrQuery
public setMltMinTermFrequency(int $minTermFrequency): SolrQuery
public setMltMinWordLength(int $minWordLength): SolrQuery
public setOmitHeader(bool $flag): SolrQuery
public setQuery(string $query): SolrQuery
public setRows(int $rows): SolrQuery
public setShowDebugInfo(bool $flag): SolrQuery
public setStart(int $start): SolrQuery
public setStats(bool $flag): SolrQuery
public setTerms(bool $flag): SolrQuery
public setTermsField(string $fieldname): SolrQuery
public setTermsIncludeLowerBound(bool $flag): SolrQuery
public setTermsIncludeUpperBound(bool $flag): SolrQuery
public setTermsLimit(int $limit): SolrQuery
public setTermsLowerBound(string $lowerBound): SolrQuery
public setTermsMaxCount(int $frequency): SolrQuery
public setTermsMinCount(int $frequency): SolrQuery
public setTermsPrefix(string $prefix): SolrQuery
public setTermsReturnRaw(bool $flag): SolrQuery
public setTermsSort(int $sortType): SolrQuery
public setTermsUpperBound(string $upperBound): SolrQuery
public setTimeAllowed(int $timeAllowed): SolrQuery

    public __destruct()


    /* Наследуемые методы */
    public SolrModifiableParams::__construct()

    public SolrModifiableParams::__destruct()


   }
```

## Обумовлені константи

**`SolrQuery::ORDER_ASC`**

Використовується для вказівки того, що сортування має бути в порядку зростання

**`SolrQuery::ORDER_DESC`**

Використовується для вказівки, що сортування має бути в порядку зменшення

**`SolrQuery::FACET_SORT_INDEX`**

Використовується для вказівки сортування фасету за індексом

**`SolrQuery::FACET_SORT_COUNT`**

Використовується для вказівки того, що фасет має сортувати за кількістю

**`SolrQuery::TERMS_SORT_INDEX`**

Використовується в TermsComponent

**`SolrQuery::TERMS_SORT_COUNT`**

Використовується в TermsComponent

## Зміст

-   [SolrQuery::addExpandFilterQuery](solrquery.addexpandfilterquery.md) — Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::addExpandSortField](solrquery.addexpandsortfield.md) — Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::addFacetDateField](solrquery.addfacetdatefield.md) - Карти для facet.date
-   [SolrQuery::addFacetDateOther](solrquery.addfacetdateother.md) — Додає ще один параметр facet.date.other
-   [SolrQuery::addFacetField](solrquery.addfacetfield.md) — Додає інше поле до фасету
-   [SolrQuery::addFacetQuery](solrquery.addfacetquery.md) — Додає фасетний запит
-   [SolrQuery::addField](solrquery.addfield.md) — Вказує, які поля повертатиме в результаті
-   [SolrQuery::addFilterQuery](solrquery.addfilterquery.md) — Визначає запит фільтру
-   [SolrQuery::addGroupField](solrquery.addgroupfield.md) — Додає поле, яке використовуватиметься для угруповання результатів
-   [SolrQuery::addGroupFunction](solrquery.addgroupfunction.md) — Дозволяє групувати результати з урахуванням унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery](solrquery.addgroupquery.md) — Дозволяє групувати документи, що відповідають цьому запиту.
-   [SolrQuery::addGroupSortField](solrquery.addgroupsortfield.md) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::addHighlightField](solrquery.addhighlightfield.md) - Відповідає hl.fl
-   [SolrQuery::addMltField](solrquery.addmltfield.md) — Встановлює поле для використання для подібності
-   [SolrQuery::addMltQueryField](solrquery.addmltqueryfield.md) - Відповідає mlt.qf
-   [SolrQuery::addSortField](solrquery.addsortfield.md) — Використовується для керування сортуванням результатів
-   [SolrQuery::addStatsFacet](solrquery.addstatsfacet.md) — Запитує повернення допоміжних результатів для значень у цьому фасеті
-   [SolrQuery::addStatsField](solrquery.addstatsfield.md) - Відповідає параметру stats.field
-   [SolrQuery::collapse](solrquery.collapse.md) — Згортає набір результатів до одного документа на групу
-   [SolrQuery::construct](solrquery.construct.md) - Конструктор
-   [SolrQuery::destruct](solrquery.destruct.md) - Деструктор
-   [SolrQuery::getExpand](solrquery.getexpand.md) — Повертає true, якщо увімкнено розширення групи
-   [SolrQuery::getExpandFilterQueries](solrquery.getexpandfilterqueries.md) — Повертає запити на розширений фільтр
-   [SolrQuery::getExpandQuery](solrquery.getexpandquery.md) — Повертає параметр розширеного запиту expand.q
-   [SolrQuery::getExpandRows](solrquery.getexpandrows.md) — Повертає кількість рядків, які відображаються в кожній групі (expand.rows)
-   [SolrQuery::getExpandSortFields](solrquery.getexpandsortfields.md) - Повертає масив полів
-   [SolrQuery::getFacet](solrquery.getfacet.md) — Повертає значення параметра фасету
-   [SolrQuery::getFacetDateEnd](solrquery.getfacetdateend.md) — Повертає значення параметра facet.date.end
-   [SolrQuery::getFacetDateFields](solrquery.getfacetdatefields.md) - Повертає всі поля facet.date
-   [SolrQuery::getFacetDateGap](solrquery.getfacetdategap.md) — Повертає значення параметра facet.date.gap
-   [SolrQuery::getFacetDateHardEnd](solrquery.getfacetdatehardend.md) — Повертає значення параметра facet.date.hardend
-   [SolrQuery::getFacetDateOther](solrquery.getfacetdateother.md) — Повертає значення параметра facet.date.other
-   [SolrQuery::getFacetDateStart](solrquery.getfacetdatestart.md) — Повертає нижню межу першого діапазону дат для всіх аспектів дати у цьому полі
-   [SolrQuery::getFacetFields](solrquery.getfacetfields.md) — Повертає всі поля фасетів
-   [SolrQuery::getFacetLimit](solrquery.getfacetlimit.md) — Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету
-   [SolrQuery::getFacetMethod](solrquery.getfacetmethod.md) — Повертає значення параметра facet.method
-   [SolrQuery::getFacetMinCount](solrquery.getfacetmincount.md) — Повертає мінімальну кількість полів аспектів, які мають бути включені у відповідь
-   [SolrQuery::getFacetMissing](solrquery.getfacetmissing.md) — Повертає поточний стан facet.missing
-   [SolrQuery::getFacetOffset](solrquery.getfacetoffset.md) — Повертає усунення у списку обмежень, які будуть використовуватися для посторінкової навігації
-   [SolrQuery::getFacetPrefix](solrquery.getfacetprefix.md) — Повертає префікс фасету
-   [SolrQuery::getFacetQueries](solrquery.getfacetqueries.md) — Повертає всі фасетні запити
-   [SolrQuery::getFacetSort](solrquery.getfacetsort.md) — Повертає тип сортування фасету
-   [SolrQuery::getFields](solrquery.getfields.md) — Повертає список полів, які будуть повернені у відповіді
-   [SolrQuery::getFilterQueries](solrquery.getfilterqueries.md) - Повертає масив запитів фільтра
-   [SolrQuery::getGroup](solrquery.getgroup.md) — Повертає true, якщо угруповання увімкнено
-   [SolrQuery::getGroupCachePercent](solrquery.getgroupcachepercent.md) — Повертає відсоткове значення групового кешу
-   [SolrQuery::getGroupFacet](solrquery.getgroupfacet.md) — Повертає значення параметра group.facet
-   [SolrQuery::getGroupFields](solrquery.getgroupfields.md) — Повертає групові поля (значення параметра group.field)
-   [SolrQuery::getGroupFormat](solrquery.getgroupformat.md) - Повертає значення group.format
-   [SolrQuery::getGroupFunctions](solrquery.getgroupfunctions.md) — Повертає групові функції (значення параметрів group.func)
-   [SolrQuery::getGroupLimit](solrquery.getgrouplimit.md) — Повертає значення group.limit
-   [SolrQuery::getGroupMain](solrquery.getgroupmain.md) — Повертає значення group.main
-   [SolrQuery::getGroupNGroups](solrquery.getgroupngroups.md) — Повертає значення group.ngroups
-   [SolrQuery::getGroupOffset](solrquery.getgroupoffset.md) — Повертає значення group.offset
-   [SolrQuery::getGroupQueries](solrquery.getgroupqueries.md) — Повертає всі параметри group.query
-   [SolrQuery::getGroupSortFields](solrquery.getgroupsortfields.md) — Повертає значення group.sort
-   [SolrQuery::getGroupTruncate](solrquery.getgrouptruncate.md) — Повертає значення group.truncate
-   [SolrQuery::getHighlight](solrquery.gethighlight.md) — Повертає стан параметра hl
-   [SolrQuery::getHighlightAlternateField](solrquery.gethighlightalternatefield.md) — Повертає виділене поле для використання як резервну копію або за замовчуванням
-   [SolrQuery::getHighlightFields](solrquery.gethighlightfields.md) — Повертає всі поля, для яких Solr має генерувати виділені фрагменти
-   [SolrQuery::getHighlightFormatter](solrquery.gethighlightformatter.md) — Повертає засіб форматування для виділеного висновку
-   [SolrQuery::getHighlightFragmenter](solrquery.gethighlightfragmenter.md) — Повертає генератор фрагментів тексту для виділеного тексту
-   [SolrQuery::getHighlightFragsize](solrquery.gethighlightfragsize.md) — Повертає кількість символів фрагментів для виділення
-   [SolrQuery::getHighlightHighlightMultiTerm](solrquery.gethighlighthighlightmultiterm.md) — Повертає, чи потрібно включати виділення для запитів діапазону/підстановочних знаків/нечітких/префіксів
-   [SolrQuery::getHighlightMaxAlternateFieldLength](solrquery.gethighlightmaxalternatefieldlength.md) — Повертає максимальну кількість символів поля для повернення
-   [SolrQuery::getHighlightMaxAnalyzedChars](solrquery.gethighlightmaxanalyzedchars.md) — Повертає максимальну кількість символів у документі для пошуку відповідних фрагментів
-   [SolrQuery::getHighlightMergeContiguous](solrquery.gethighlightmergecontiguous.md) — Повертає, чи повернути суміжні фрагменти в один фрагмент
-   [SolrQuery::getHighlightRegexMaxAnalyzedChars](solrquery.gethighlightregexmaxanalyzedchars.md) — Повертає максимальну кількість символів із поля при використанні фрагментатора регулярного виразу
-   [SolrQuery::getHighlightRegexPattern](solrquery.gethighlightregexpattern.md) — Повертає регулярний вираз для фрагментації
-   [SolrQuery::getHighlightRegexSlop](solrquery.gethighlightregexslop.md) — Повертає коефіцієнт відхилення від ідеального розміру фрагмента
-   [SolrQuery::getHighlightRequireFieldMatch](solrquery.gethighlightrequirefieldmatch.md) — Повертає, якщо поле буде виділено лише у тому випадку, якщо запит відповідає цьому конкретному полю
-   [SolrQuery::getHighlightSimplePost](solrquery.gethighlightsimplepost.md) — Повертає текст, який з'являється після виділення.
-   [SolrQuery::getHighlightSimplePre](solrquery.gethighlightsimplepre.md) — Повертає текст, який з'являється перед виділеним виразом
-   [SolrQuery::getHighlightSnippets](solrquery.gethighlightsnippets.md) — Повертає максимальну кількість виділених фрагментів для створення кожного поля
-   [SolrQuery::getHighlightUsePhraseHighlighter](solrquery.gethighlightusephrasehighlighter.md) — Повертає стан параметра hl.usePhraseHighlighter
-   [SolrQuery::getMlt](solrquery.getmlt.md) — Повертає, чи мають бути включені результати MoreLikeThis
-   [SolrQuery::getMltBoost](solrquery.getmltboost.md) — Повертає, чи буде запит посилений релевантністю виразу, що цікавить.
-   [SolrQuery::getMltCount](solrquery.getmltcount.md) — Повертає кількість схожих документів, які повертаються для кожного результату
-   [SolrQuery::getMltFields](solrquery.getmltfields.md) — Повертає всі поля, які потрібно використати для порівняння
-   [SolrQuery::getMltMaxNumQueryTerms](solrquery.getmltmaxnumqueryterms.md) — Повертає максимальну кількість умов запиту, які будуть включені до будь-якого згенерованого запиту
-   [SolrQuery::getMltMaxNumTokens](solrquery.getmltmaxnumtokens.md) — Повертає максимальну кількість токенів для аналізу у кожному полі документа, яке не зберігається за допомогою TermVector
-   [SolrQuery::getMltMaxWordLength](solrquery.getmltmaxwordlength.md) — Повертає максимальну довжину слова, вище якої слова ігноруватимуться.
-   [SolrQuery::getMltMinDocFrequency](solrquery.getmltmindocfrequency.md) — Повертає граничну частоту, з якої ігноруватимуться слова, яких немає, принаймні, у такій кількості документів
-   [SolrQuery::getMltMinTermFrequency](solrquery.getmltmintermfrequency.md) — Повертає частоту, нижче за яку вирази ігноруватимуться у вихідному документі
-   [SolrQuery::getMltMinWordLength](solrquery.getmltminwordlength.md) — Повертає мінімальну довжину слова, нижче за яку слова ігноруватимуться
-   [SolrQuery::getMltQueryFields](solrquery.getmltqueryfields.md) — Повертає поля запиту та їх підвищення
-   [SolrQuery::getQuery](solrquery.getquery.md) - Повертає основний запит
-   [SolrQuery::getRows](solrquery.getrows.md) — Повертає максимальну кількість документів
-   [SolrQuery::getSortFields](solrquery.getsortfields.md) - Повертає всі поля сортування
-   [SolrQuery::getStart](solrquery.getstart.md) — Повертає усунення у повному наборі результатів
-   [SolrQuery::getStats](solrquery.getstats.md) — Повертає, чи включено статистику
-   [SolrQuery::getStatsFacets](solrquery.getstatsfacets.md) — Повертає всі фасети статистики, які було встановлено
-   [SolrQuery::getStatsFields](solrquery.getstatsfields.md) — Повертає усі поля статистики
-   [SolrQuery::getTerms](solrquery.getterms.md) — Повертає, чи увімкнено Terms Component
-   [SolrQuery::getTermsField](solrquery.gettermsfield.md) — Повертає поле, з якого витягуються вирази
-   [SolrQuery::getTermsIncludeLowerBound](solrquery.gettermsincludelowerbound.md) — Повертає, чи потрібно включати вираз нижньої межі до набору результатів
-   [SolrQuery::getTermsIncludeUpperBound](solrquery.gettermsincludeupperbound.md) — Повертає, чи потрібно включати вираз верхньої межі до набору результатів
-   [SolrQuery::getTermsLimit](solrquery.gettermslimit.md) — Повертає максимальну кількість виразів, які має повернути Solr
-   [SolrQuery::getTermsLowerBound](solrquery.gettermslowerbound.md) — Повертає вираз для початку
-   [SolrQuery::getTermsMaxCount](solrquery.gettermsmaxcount.md) — Повертає максимальну частоту документа
-   [SolrQuery::getTermsMinCount](solrquery.gettermsmincount.md) — Повертає мінімальну частоту повернення документів для увімкнення
-   [SolrQuery::getTermsPrefix](solrquery.gettermsprefix.md) — Повертає префікс виразу
-   [SolrQuery::getTermsReturnRaw](solrquery.gettermsreturnraw.md) — Чи слід повертати необроблені символи
-   [SolrQuery::getTermsSort](solrquery.gettermssort.md) — Повертає ціле число, яке вказує, як сортуються вирази
-   [SolrQuery::getTermsUpperBound](solrquery.gettermsupperbound.md) — Повертає вираз для зупинки
-   [SolrQuery::getTimeAllowed](solrquery.gettimeallowed.md) — Повертає час у мілісекундах, дозволений для завершення запиту
-   [SolrQuery::removeExpandFilterQuery](solrquery.removeexpandfilterquery.md) — Видаляє запит розширеного фільтра
-   [SolrQuery::removeExpandSortField](solrquery.removeexpandsortfield.md) — Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::removeFacetDateField](solrquery.removefacetdatefield.md) — Видаляє одне з полів дати фасету
-   [SolrQuery::removeFacetDateOther](solrquery.removefacetdateother.md) — Видаляє один із параметрів facet.date.other
-   [SolrQuery::removeFacetField](solrquery.removefacetfield.md) — Видаляє один із параметрів facet.date
-   [SolrQuery::removeFacetQuery](solrquery.removefacetquery.md) — Видаляє один із параметрів facet.query
-   [SolrQuery::removeField](solrquery.removefield.md) — Видаляє поле зі списку полів
-   [SolrQuery::removeFilterQuery](solrquery.removefilterquery.md) — Видаляє запит фільтра
-   [SolrQuery::removeHighlightField](solrquery.removehighlightfield.md) — Видаляє одне з полів, що використовуються для виділення
-   [SolrQuery::removeMltField](solrquery.removemltfield.md) — Видаляє одне з полів.
-   [SolrQuery::removeMltQueryField](solrquery.removemltqueryfield.md) — Видаляє одне з полів запиту moreLikeThis
-   [SolrQuery::removeSortField](solrquery.removesortfield.md) - Видаляє одне з полів сортування
-   [SolrQuery::removeStatsFacet](solrquery.removestatsfacet.md) — Видаляє один із параметрів stats.facet
-   [SolrQuery::removeStatsField](solrquery.removestatsfield.md) — Видаляє один із параметрів stats.field
-   [SolrQuery::setEchoHandler](solrquery.setechohandler.md) — Перемикає параметр echoHandler
-   [SolrQuery::setEchoParams](solrquery.setechoparams.md) — Визначає, які параметри включати у відповідь
-   [SolrQuery::setExpand](solrquery.setexpand.md) — Вмикає/вимикає компонент Expand
-   [SolrQuery::setExpandQuery](solrquery.setexpandquery.md) — Встановлює параметр expand.q
-   [SolrQuery::setExpandRows](solrquery.setexpandrows.md) — Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExplainOther](solrquery.setexplainother.md) — Встановлює загальний параметр запиту explainOther
-   [SolrQuery::setFacet](solrquery.setfacet.md) — Відповідає параметру фасету. Включає або вимикає фасетування
-   [SolrQuery::setFacetDateEnd](solrquery.setfacetdateend.md) - Відповідає facet.date.end
-   [SolrQuery::setFacetDateGap](solrquery.setfacetdategap.md) - Відповідає facet.date.gap
-   [SolrQuery::setFacetDateHardEnd](solrquery.setfacetdatehardend.md) - Відповідає facet.date.hardend
-   [SolrQuery::setFacetDateStart](solrquery.setfacetdatestart.md) - Відповідає facet.date.start
-   [SolrQuery::setFacetEnumCacheMinDefaultFrequency](solrquery.setfacetenumcachemindefaultfrequency.md) — Встановлює мінімальну частоту документа, яка використовується для визначення кількості виразів
-   [SolrQuery::setFacetLimit](solrquery.setfacetlimit.md) - Відповідає facet.limit
-   [SolrQuery::setFacetMethod](solrquery.setfacetmethod.md) — Задає тип алгоритму, який слід використовувати під час фасетування поля
-   [SolrQuery::setFacetMinCount](solrquery.setfacetmincount.md) - Відповідає facet.mincount
-   [SolrQuery::setFacetMissing](solrquery.setfacetmissing.md) - Відповідає facet.missing
-   [SolrQuery::setFacetOffset](solrquery.setfacetoffset.md) — Встановлює переміщення до списку обмежень для розбивки на сторінки
-   [SolrQuery::setFacetPrefix](solrquery.setfacetprefix.md) — Визначає рядковий префікс, за допомогою якого обмежуються вирази, на яких виконується фасет
-   [SolrQuery::setFacetSort](solrquery.setfacetsort.md) — Визначає порядок обмежень поля фасету
-   [SolrQuery::setGroup](solrquery.setgroup.md) — Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::setGroupCachePercent](solrquery.setgroupcachepercent.md) — Включає кешування для угруповання результатів
-   [SolrQuery::setGroupFacet](solrquery.setgroupfacet.md) - Встановлює параметр group.facet
-   [SolrQuery::setGroupFormat](solrquery.setgroupformat.md) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupLimit](solrquery.setgrouplimit.md) — Задає кількість результатів, які повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain](solrquery.setgroupmain.md) — Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups](solrquery.setgroupngroups.md) — Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupOffset](solrquery.setgroupoffset.md) - Встановлює параметр group.offset
-   [SolrQuery::setGroupTruncate](solrquery.setgrouptruncate.md) — Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setHighlight](solrquery.sethighlight.md) — Вмикає або вимикає виділення
-   [SolrQuery::setHighlightAlternateField](solrquery.sethighlightalternatefield.md) — Задає поле резервного копіювання для використання
-   [SolrQuery::setHighlightFormatter](solrquery.sethighlightformatter.md) — Задає засіб форматування для виділення виділення
-   [SolrQuery::setHighlightFragmenter](solrquery.sethighlightfragmenter.md) — Встановлює генератор текстових фрагментів для виділеного тексту
-   [SolrQuery::setHighlightFragsize](solrquery.sethighlightfragsize.md) — Розмір фрагментів, які слід враховувати під час виділення
-   [SolrQuery::setHighlightHighlightMultiTerm](solrquery.sethighlighthighlightmultiterm.md) — Використовувати SpanScorer для виділення виразів
-   [SolrQuery::setHighlightMaxAlternateFieldLength](solrquery.sethighlightmaxalternatefieldlength.md) — Встановлює максимальну кількість символів поля для повернення
-   [SolrQuery::setHighlightMaxAnalyzedChars](solrquery.sethighlightmaxanalyzedchars.md) — Задає кількість символів у документі для пошуку відповідних фрагментів
-   [SolrQuery::setHighlightMergeContiguous](solrquery.sethighlightmergecontiguous.md) — Чи згортати суміжні фрагменти в один фрагмент
-   [SolrQuery::setHighlightRegexMaxAnalyzedChars](solrquery.sethighlightregexmaxanalyzedchars.md) — Задає максимальну кількість символів для аналізу
-   [SolrQuery::setHighlightRegexPattern](solrquery.sethighlightregexpattern.md) — Задає регулярний вираз для фрагментації
-   [SolrQuery::setHighlightRegexSlop](solrquery.sethighlightregexslop.md) — Встановлює коефіцієнт, на який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента
-   [SolrQuery::setHighlightRequireFieldMatch](solrquery.sethighlightrequirefieldmatch.md) - Вимагати зіставлення полів при виділенні
-   [SolrQuery::setHighlightSimplePost](solrquery.sethighlightsimplepost.md) — Встановлює текст, який з'являється після виділення.
-   [SolrQuery::setHighlightSimplePre](solrquery.sethighlightsimplepre.md) — Встановлює текст, який з'являється перед виділеним виразом
-   [SolrQuery::setHighlightSnippets](solrquery.sethighlightsnippets.md) — Встановлює максимальну кількість виділених фрагментів для створення кожного поля
-   [SolrQuery::setHighlightUsePhraseHighlighter](solrquery.sethighlightusephrasehighlighter.md) — Чи слід виділяти вирази лише тоді, коли вони з'являються у фразі запиту
-   [SolrQuery::setMlt](solrquery.setmlt.md) — Включає або вимикає moreLikeThis
-   [SolrQuery::setMltBoost](solrquery.setmltboost.md) — Встановлює, чи буде запит посилено релевантністю цікавого виразу.
-   [SolrQuery::setMltCount](solrquery.setmltcount.md) — Встановлює кількість схожих документів, які повертаються для кожного результату.
-   [SolrQuery::setMltMaxNumQueryTerms](solrquery.setmltmaxnumqueryterms.md) — Встановлює максимальну кількість запитів, що включаються.
-   [SolrQuery::setMltMaxNumTokens](solrquery.setmltmaxnumtokens.md) — Задає максимальну кількість токенів для аналізу
-   [SolrQuery::setMltMaxWordLength](solrquery.setmltmaxwordlength.md) - Встановлює максимальну довжину слова
-   [SolrQuery::setMltMinDocFrequency](solrquery.setmltmindocfrequency.md) - Встановлює частоту mltMinDoc
-   [SolrQuery::setMltMinTermFrequency](solrquery.setmltmintermfrequency.md) — Встановлює частоту, нижче за яку вирази ігноруватимуться у вихідній документації
-   [SolrQuery::setMltMinWordLength](solrquery.setmltminwordlength.md) - Встановлює мінімальну довжину слова
-   [SolrQuery::setOmitHeader](solrquery.setomitheader.md) — Виключає заголовок з результатів, що повертаються.
-   [SolrQuery::setQuery](solrquery.setquery.md) — Встановлює пошуковий запит
-   [SolrQuery::setRows](solrquery.setrows.md) — Задає максимальну кількість рядків, які повертаються в результаті
-   [SolrQuery::setShowDebugInfo](solrquery.setshowdebuginfo.md) — Прапор для відображення налагоджувальної інформації
-   [SolrQuery::setStart](solrquery.setstart.md) — Визначає кількість рядків, що пропускаються.
-   [SolrQuery::setStats](solrquery.setstats.md) — Вмикає або вимикає компонент Stats
-   [SolrQuery::setTerms](solrquery.setterms.md) — Вмикає або вимикає TermsComponent
-   [SolrQuery::setTermsField](solrquery.settermsfield.md) — Встановлює ім'я поля, з якого потрібно одержати вираз
-   [SolrQuery::setTermsIncludeLowerBound](solrquery.settermsincludelowerbound.md) — Включає нижню межу вираження у набір результатів
-   [SolrQuery::setTermsIncludeUpperBound](solrquery.settermsincludeupperbound.md) — Включає верхню межу виразу до набору результатів
-   [SolrQuery::setTermsLimit](solrquery.settermslimit.md) — Встановлює максимальну кількість виразів, що повертаються.
-   [SolrQuery::setTermsLowerBound](solrquery.settermslowerbound.md) - Визначає вираз, з якого треба починати
-   [SolrQuery::setTermsMaxCount](solrquery.settermsmaxcount.md) — Встановлює максимальну частоту документів
-   [SolrQuery::setTermsMinCount](solrquery.settermsmincount.md) — Встановлює мінімальну частоту документів
-   [SolrQuery::setTermsPrefix](solrquery.settermsprefix.md) — Обмежує збіги виразами, що починаються з префіксу
-   [SolrQuery::setTermsReturnRaw](solrquery.settermsreturnraw.md) — Повернути необроблені символи проіндексованого виразу
-   [SolrQuery::setTermsSort](solrquery.settermssort.md) — Визначає, як сортувати повернені умови
-   [SolrQuery::setTermsUpperBound](solrquery.settermsupperbound.md) - Встановлює умову для зупинки
-   [SolrQuery::setTimeAllowed](solrquery.settimeallowed.md) - Час, відведений на пошук
