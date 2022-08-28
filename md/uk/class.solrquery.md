Клас SolrQuery

-   [« SolrModifiableParams::\_\_destruct](solrmodifiableparams.destruct.html)
    
-   [SolrQuery::addExpandFilterQuery »](solrquery.addexpandfilterquery.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrQuery
    

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

-   [SolrQuery::addExpandFilterQuery](solrquery.addexpandfilterquery.html) — Перевизначає запит основного фільтра, визначає, які документи включити до основної групи
-   [SolrQuery::addExpandSortField](solrquery.addexpandsortfield.html) — Упорядковує документи у розширених групах (параметр expand.sort)
-   [SolrQuery::addFacetDateField](solrquery.addfacetdatefield.html) - Карти для facet.date
-   [SolrQuery::addFacetDateOther](solrquery.addfacetdateother.html) — Додає ще один параметр facet.date.other
-   [SolrQuery::addFacetField](solrquery.addfacetfield.html) — Додає інше поле до фасету
-   [SolrQuery::addFacetQuery](solrquery.addfacetquery.html) — Додає фасетний запит
-   [SolrQuery::addField](solrquery.addfield.html) — Вказує, які поля повертатиме в результаті
-   [SolrQuery::addFilterQuery](solrquery.addfilterquery.html) — Визначає запит фільтру
-   [SolrQuery::addGroupField](solrquery.addgroupfield.html) — Додає поле, яке використовуватиметься для угруповання результатів
-   [SolrQuery::addGroupFunction](solrquery.addgroupfunction.html) — Дозволяє групувати результати з урахуванням унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery](solrquery.addgroupquery.html) — Дозволяє групувати документи, що відповідають цьому запиту.
-   [SolrQuery::addGroupSortField](solrquery.addgroupsortfield.html) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::addHighlightField](solrquery.addhighlightfield.html) - Відповідає hl.fl
-   [SolrQuery::addMltField](solrquery.addmltfield.html) — Встановлює поле для використання для подібності
-   [SolrQuery::addMltQueryField](solrquery.addmltqueryfield.html) - Відповідає mlt.qf
-   [SolrQuery::addSortField](solrquery.addsortfield.html) — Використовується для керування сортуванням результатів
-   [SolrQuery::addStatsFacet](solrquery.addstatsfacet.html) — Запитує повернення допоміжних результатів для значень у цьому фасеті
-   [SolrQuery::addStatsField](solrquery.addstatsfield.html) - Відповідає параметру stats.field
-   [SolrQuery::collapse](solrquery.collapse.html) — Згортає набір результатів до одного документа на групу
-   [SolrQuery::\_\_construct](solrquery.construct.html) - Конструктор
-   [SolrQuery::\_\_destruct](solrquery.destruct.html) - Деструктор
-   [SolrQuery::getExpand](solrquery.getexpand.html) — Повертає true, якщо увімкнено розширення групи
-   [SolrQuery::getExpandFilterQueries](solrquery.getexpandfilterqueries.html) — Повертає запити на розширений фільтр
-   [SolrQuery::getExpandQuery](solrquery.getexpandquery.html) — Повертає параметр розширеного запиту expand.q
-   [SolrQuery::getExpandRows](solrquery.getexpandrows.html) — Повертає кількість рядків, які відображаються в кожній групі (expand.rows)
-   [SolrQuery::getExpandSortFields](solrquery.getexpandsortfields.html) - Повертає масив полів
-   [SolrQuery::getFacet](solrquery.getfacet.html) — Повертає значення параметра фасету
-   [SolrQuery::getFacetDateEnd](solrquery.getfacetdateend.html) — Повертає значення параметра facet.date.end
-   [SolrQuery::getFacetDateFields](solrquery.getfacetdatefields.html) - Повертає всі поля facet.date
-   [SolrQuery::getFacetDateGap](solrquery.getfacetdategap.html) — Повертає значення параметра facet.date.gap
-   [SolrQuery::getFacetDateHardEnd](solrquery.getfacetdatehardend.html) — Повертає значення параметра facet.date.hardend
-   [SolrQuery::getFacetDateOther](solrquery.getfacetdateother.html) — Повертає значення параметра facet.date.other
-   [SolrQuery::getFacetDateStart](solrquery.getfacetdatestart.html) — Повертає нижню межу першого діапазону дат для всіх аспектів дати у цьому полі
-   [SolrQuery::getFacetFields](solrquery.getfacetfields.html) — Повертає всі поля фасетів
-   [SolrQuery::getFacetLimit](solrquery.getfacetlimit.html) — Повертає максимальну кількість лічильників обмежень, яка має бути повернена для полів фасету
-   [SolrQuery::getFacetMethod](solrquery.getfacetmethod.html) — Повертає значення параметра facet.method
-   [SolrQuery::getFacetMinCount](solrquery.getfacetmincount.html) — Повертає мінімальну кількість полів аспектів, які мають бути включені у відповідь
-   [SolrQuery::getFacetMissing](solrquery.getfacetmissing.html) — Повертає поточний стан facet.missing
-   [SolrQuery::getFacetOffset](solrquery.getfacetoffset.html) — Повертає усунення у списку обмежень, які будуть використовуватися для посторінкової навігації
-   [SolrQuery::getFacetPrefix](solrquery.getfacetprefix.html) — Повертає префікс фасету
-   [SolrQuery::getFacetQueries](solrquery.getfacetqueries.html) — Повертає всі фасетні запити
-   [SolrQuery::getFacetSort](solrquery.getfacetsort.html) — Повертає тип сортування фасету
-   [SolrQuery::getFields](solrquery.getfields.html) — Повертає список полів, які будуть повернені у відповіді
-   [SolrQuery::getFilterQueries](solrquery.getfilterqueries.html) - Повертає масив запитів фільтра
-   [SolrQuery::getGroup](solrquery.getgroup.html) — Повертає true, якщо угруповання увімкнено
-   [SolrQuery::getGroupCachePercent](solrquery.getgroupcachepercent.html) — Повертає відсоткове значення групового кешу
-   [SolrQuery::getGroupFacet](solrquery.getgroupfacet.html) — Повертає значення параметра group.facet
-   [SolrQuery::getGroupFields](solrquery.getgroupfields.html) — Повертає групові поля (значення параметра group.field)
-   [SolrQuery::getGroupFormat](solrquery.getgroupformat.html) - Повертає значення group.format
-   [SolrQuery::getGroupFunctions](solrquery.getgroupfunctions.html) — Повертає групові функції (значення параметрів group.func)
-   [SolrQuery::getGroupLimit](solrquery.getgrouplimit.html) — Повертає значення group.limit
-   [SolrQuery::getGroupMain](solrquery.getgroupmain.html) — Повертає значення group.main
-   [SolrQuery::getGroupNGroups](solrquery.getgroupngroups.html) — Повертає значення group.ngroups
-   [SolrQuery::getGroupOffset](solrquery.getgroupoffset.html) — Повертає значення group.offset
-   [SolrQuery::getGroupQueries](solrquery.getgroupqueries.html) — Повертає всі параметри group.query
-   [SolrQuery::getGroupSortFields](solrquery.getgroupsortfields.html) — Повертає значення group.sort
-   [SolrQuery::getGroupTruncate](solrquery.getgrouptruncate.html) — Повертає значення group.truncate
-   [SolrQuery::getHighlight](solrquery.gethighlight.html) — Повертає стан параметра hl
-   [SolrQuery::getHighlightAlternateField](solrquery.gethighlightalternatefield.html) — Повертає виділене поле для використання як резервну копію або за замовчуванням
-   [SolrQuery::getHighlightFields](solrquery.gethighlightfields.html) — Повертає всі поля, для яких Solr має генерувати виділені фрагменти
-   [SolrQuery::getHighlightFormatter](solrquery.gethighlightformatter.html) — Повертає засіб форматування для виділеного висновку
-   [SolrQuery::getHighlightFragmenter](solrquery.gethighlightfragmenter.html) — Повертає генератор фрагментів тексту для виділеного тексту
-   [SolrQuery::getHighlightFragsize](solrquery.gethighlightfragsize.html) — Повертає кількість символів фрагментів для виділення
-   [SolrQuery::getHighlightHighlightMultiTerm](solrquery.gethighlighthighlightmultiterm.html) — Повертає, чи потрібно включати виділення для запитів діапазону/підстановочних знаків/нечітких/префіксів
-   [SolrQuery::getHighlightMaxAlternateFieldLength](solrquery.gethighlightmaxalternatefieldlength.html) — Повертає максимальну кількість символів поля для повернення
-   [SolrQuery::getHighlightMaxAnalyzedChars](solrquery.gethighlightmaxanalyzedchars.html) — Повертає максимальну кількість символів у документі для пошуку відповідних фрагментів
-   [SolrQuery::getHighlightMergeContiguous](solrquery.gethighlightmergecontiguous.html) — Повертає, чи повернути суміжні фрагменти в один фрагмент
-   [SolrQuery::getHighlightRegexMaxAnalyzedChars](solrquery.gethighlightregexmaxanalyzedchars.html) — Повертає максимальну кількість символів із поля при використанні фрагментатора регулярного виразу
-   [SolrQuery::getHighlightRegexPattern](solrquery.gethighlightregexpattern.html) — Повертає регулярний вираз для фрагментації
-   [SolrQuery::getHighlightRegexSlop](solrquery.gethighlightregexslop.html) — Повертає коефіцієнт відхилення від ідеального розміру фрагмента
-   [SolrQuery::getHighlightRequireFieldMatch](solrquery.gethighlightrequirefieldmatch.html) — Повертає, якщо поле буде виділено лише у тому випадку, якщо запит відповідає цьому конкретному полю
-   [SolrQuery::getHighlightSimplePost](solrquery.gethighlightsimplepost.html) — Повертає текст, який з'являється після виділення.
-   [SolrQuery::getHighlightSimplePre](solrquery.gethighlightsimplepre.html) — Повертає текст, який з'являється перед виділеним виразом
-   [SolrQuery::getHighlightSnippets](solrquery.gethighlightsnippets.html) — Повертає максимальну кількість виділених фрагментів для створення кожного поля
-   [SolrQuery::getHighlightUsePhraseHighlighter](solrquery.gethighlightusephrasehighlighter.html) — Повертає стан параметра hl.usePhraseHighlighter
-   [SolrQuery::getMlt](solrquery.getmlt.html) — Повертає, чи мають бути включені результати MoreLikeThis
-   [SolrQuery::getMltBoost](solrquery.getmltboost.html) — Повертає, чи буде запит посилений релевантністю виразу, що цікавить.
-   [SolrQuery::getMltCount](solrquery.getmltcount.html) — Повертає кількість схожих документів, які повертаються для кожного результату
-   [SolrQuery::getMltFields](solrquery.getmltfields.html) — Повертає всі поля, які потрібно використати для порівняння
-   [SolrQuery::getMltMaxNumQueryTerms](solrquery.getmltmaxnumqueryterms.html) — Повертає максимальну кількість умов запиту, які будуть включені до будь-якого згенерованого запиту
-   [SolrQuery::getMltMaxNumTokens](solrquery.getmltmaxnumtokens.html) — Повертає максимальну кількість токенів для аналізу у кожному полі документа, яке не зберігається за допомогою TermVector
-   [SolrQuery::getMltMaxWordLength](solrquery.getmltmaxwordlength.html) — Повертає максимальну довжину слова, вище якої слова ігноруватимуться.
-   [SolrQuery::getMltMinDocFrequency](solrquery.getmltmindocfrequency.html) — Повертає граничну частоту, з якої ігноруватимуться слова, яких немає, принаймні, у такій кількості документів
-   [SolrQuery::getMltMinTermFrequency](solrquery.getmltmintermfrequency.html) — Повертає частоту, нижче за яку вирази ігноруватимуться у вихідному документі
-   [SolrQuery::getMltMinWordLength](solrquery.getmltminwordlength.html) — Повертає мінімальну довжину слова, нижче за яку слова ігноруватимуться
-   [SolrQuery::getMltQueryFields](solrquery.getmltqueryfields.html) — Повертає поля запиту та їх підвищення
-   [SolrQuery::getQuery](solrquery.getquery.html) - Повертає основний запит
-   [SolrQuery::getRows](solrquery.getrows.html) — Повертає максимальну кількість документів
-   [SolrQuery::getSortFields](solrquery.getsortfields.html) - Повертає всі поля сортування
-   [SolrQuery::getStart](solrquery.getstart.html) — Повертає усунення у повному наборі результатів
-   [SolrQuery::getStats](solrquery.getstats.html) — Повертає, чи включено статистику
-   [SolrQuery::getStatsFacets](solrquery.getstatsfacets.html) — Повертає всі фасети статистики, які було встановлено
-   [SolrQuery::getStatsFields](solrquery.getstatsfields.html) — Повертає усі поля статистики
-   [SolrQuery::getTerms](solrquery.getterms.html) — Повертає, чи увімкнено Terms Component
-   [SolrQuery::getTermsField](solrquery.gettermsfield.html) — Повертає поле, з якого витягуються вирази
-   [SolrQuery::getTermsIncludeLowerBound](solrquery.gettermsincludelowerbound.html) — Повертає, чи потрібно включати вираз нижньої межі до набору результатів
-   [SolrQuery::getTermsIncludeUpperBound](solrquery.gettermsincludeupperbound.html) — Повертає, чи потрібно включати вираз верхньої межі до набору результатів
-   [SolrQuery::getTermsLimit](solrquery.gettermslimit.html) — Повертає максимальну кількість виразів, які має повернути Solr
-   [SolrQuery::getTermsLowerBound](solrquery.gettermslowerbound.html) — Повертає вираз для початку
-   [SolrQuery::getTermsMaxCount](solrquery.gettermsmaxcount.html) — Повертає максимальну частоту документа
-   [SolrQuery::getTermsMinCount](solrquery.gettermsmincount.html) — Повертає мінімальну частоту повернення документів для увімкнення
-   [SolrQuery::getTermsPrefix](solrquery.gettermsprefix.html) — Повертає префікс виразу
-   [SolrQuery::getTermsReturnRaw](solrquery.gettermsreturnraw.html) — Чи слід повертати необроблені символи
-   [SolrQuery::getTermsSort](solrquery.gettermssort.html) — Повертає ціле число, яке вказує, як сортуються вирази
-   [SolrQuery::getTermsUpperBound](solrquery.gettermsupperbound.html) — Повертає вираз для зупинки
-   [SolrQuery::getTimeAllowed](solrquery.gettimeallowed.html) — Повертає час у мілісекундах, дозволений для завершення запиту
-   [SolrQuery::removeExpandFilterQuery](solrquery.removeexpandfilterquery.html) — Видаляє запит розширеного фільтра
-   [SolrQuery::removeExpandSortField](solrquery.removeexpandsortfield.html) — Видаляє розширене поле сортування за допомогою параметра expand.sort
-   [SolrQuery::removeFacetDateField](solrquery.removefacetdatefield.html) — Видаляє одне з полів дати фасету
-   [SolrQuery::removeFacetDateOther](solrquery.removefacetdateother.html) — Видаляє один із параметрів facet.date.other
-   [SolrQuery::removeFacetField](solrquery.removefacetfield.html) — Видаляє один із параметрів facet.date
-   [SolrQuery::removeFacetQuery](solrquery.removefacetquery.html) — Видаляє один із параметрів facet.query
-   [SolrQuery::removeField](solrquery.removefield.html) — Видаляє поле зі списку полів
-   [SolrQuery::removeFilterQuery](solrquery.removefilterquery.html) — Видаляє запит фільтра
-   [SolrQuery::removeHighlightField](solrquery.removehighlightfield.html) — Видаляє одне з полів, що використовуються для виділення
-   [SolrQuery::removeMltField](solrquery.removemltfield.html) — Видаляє одне з полів.
-   [SolrQuery::removeMltQueryField](solrquery.removemltqueryfield.html) — Видаляє одне з полів запиту moreLikeThis
-   [SolrQuery::removeSortField](solrquery.removesortfield.html) - Видаляє одне з полів сортування
-   [SolrQuery::removeStatsFacet](solrquery.removestatsfacet.html) — Видаляє один із параметрів stats.facet
-   [SolrQuery::removeStatsField](solrquery.removestatsfield.html) — Видаляє один із параметрів stats.field
-   [SolrQuery::setEchoHandler](solrquery.setechohandler.html) — Перемикає параметр echoHandler
-   [SolrQuery::setEchoParams](solrquery.setechoparams.html) — Визначає, які параметри включати у відповідь
-   [SolrQuery::setExpand](solrquery.setexpand.html) — Вмикає/вимикає компонент Expand
-   [SolrQuery::setExpandQuery](solrquery.setexpandquery.html) — Встановлює параметр expand.q
-   [SolrQuery::setExpandRows](solrquery.setexpandrows.html) — Встановлює кількість рядків для відображення кожної групи (expand.rows). Типово 5
-   [SolrQuery::setExplainOther](solrquery.setexplainother.html) — Встановлює загальний параметр запиту explainOther
-   [SolrQuery::setFacet](solrquery.setfacet.html) — Відповідає параметру фасету. Включає або вимикає фасетування
-   [SolrQuery::setFacetDateEnd](solrquery.setfacetdateend.html) - Відповідає facet.date.end
-   [SolrQuery::setFacetDateGap](solrquery.setfacetdategap.html) - Відповідає facet.date.gap
-   [SolrQuery::setFacetDateHardEnd](solrquery.setfacetdatehardend.html) - Відповідає facet.date.hardend
-   [SolrQuery::setFacetDateStart](solrquery.setfacetdatestart.html) - Відповідає facet.date.start
-   [SolrQuery::setFacetEnumCacheMinDefaultFrequency](solrquery.setfacetenumcachemindefaultfrequency.html) — Встановлює мінімальну частоту документа, яка використовується для визначення кількості виразів
-   [SolrQuery::setFacetLimit](solrquery.setfacetlimit.html) - Відповідає facet.limit
-   [SolrQuery::setFacetMethod](solrquery.setfacetmethod.html) — Задає тип алгоритму, який слід використовувати під час фасетування поля
-   [SolrQuery::setFacetMinCount](solrquery.setfacetmincount.html) - Відповідає facet.mincount
-   [SolrQuery::setFacetMissing](solrquery.setfacetmissing.html) - Відповідає facet.missing
-   [SolrQuery::setFacetOffset](solrquery.setfacetoffset.html) — Встановлює переміщення до списку обмежень для розбивки на сторінки
-   [SolrQuery::setFacetPrefix](solrquery.setfacetprefix.html) — Визначає рядковий префікс, за допомогою якого обмежуються вирази, на яких виконується фасет
-   [SolrQuery::setFacetSort](solrquery.setfacetsort.html) — Визначає порядок обмежень поля фасету
-   [SolrQuery::setGroup](solrquery.setgroup.html) — Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::setGroupCachePercent](solrquery.setgroupcachepercent.html) — Включає кешування для угруповання результатів
-   [SolrQuery::setGroupFacet](solrquery.setgroupfacet.html) - Встановлює параметр group.facet
-   [SolrQuery::setGroupFormat](solrquery.setgroupformat.html) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupLimit](solrquery.setgrouplimit.html) — Задає кількість результатів, які повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain](solrquery.setgroupmain.html) — Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups](solrquery.setgroupngroups.html) — Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupOffset](solrquery.setgroupoffset.html) - Встановлює параметр group.offset
-   [SolrQuery::setGroupTruncate](solrquery.setgrouptruncate.html) — Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setHighlight](solrquery.sethighlight.html) — Вмикає або вимикає виділення
-   [SolrQuery::setHighlightAlternateField](solrquery.sethighlightalternatefield.html) — Задає поле резервного копіювання для використання
-   [SolrQuery::setHighlightFormatter](solrquery.sethighlightformatter.html) — Задає засіб форматування для виділення виділення
-   [SolrQuery::setHighlightFragmenter](solrquery.sethighlightfragmenter.html) — Встановлює генератор текстових фрагментів для виділеного тексту
-   [SolrQuery::setHighlightFragsize](solrquery.sethighlightfragsize.html) — Розмір фрагментів, які слід враховувати під час виділення
-   [SolrQuery::setHighlightHighlightMultiTerm](solrquery.sethighlighthighlightmultiterm.html) — Використовувати SpanScorer для виділення виразів
-   [SolrQuery::setHighlightMaxAlternateFieldLength](solrquery.sethighlightmaxalternatefieldlength.html) — Встановлює максимальну кількість символів поля для повернення
-   [SolrQuery::setHighlightMaxAnalyzedChars](solrquery.sethighlightmaxanalyzedchars.html) — Задає кількість символів у документі для пошуку відповідних фрагментів
-   [SolrQuery::setHighlightMergeContiguous](solrquery.sethighlightmergecontiguous.html) — Чи згортати суміжні фрагменти в один фрагмент
-   [SolrQuery::setHighlightRegexMaxAnalyzedChars](solrquery.sethighlightregexmaxanalyzedchars.html) — Задає максимальну кількість символів для аналізу
-   [SolrQuery::setHighlightRegexPattern](solrquery.sethighlightregexpattern.html) — Задає регулярний вираз для фрагментації
-   [SolrQuery::setHighlightRegexSlop](solrquery.sethighlightregexslop.html) — Встановлює коефіцієнт, на який фрагментатор регулярного виразу може відхилитися від ідеального розміру фрагмента
-   [SolrQuery::setHighlightRequireFieldMatch](solrquery.sethighlightrequirefieldmatch.html) - Вимагати зіставлення полів при виділенні
-   [SolrQuery::setHighlightSimplePost](solrquery.sethighlightsimplepost.html) — Встановлює текст, який з'являється після виділення.
-   [SolrQuery::setHighlightSimplePre](solrquery.sethighlightsimplepre.html) — Встановлює текст, який з'являється перед виділеним виразом
-   [SolrQuery::setHighlightSnippets](solrquery.sethighlightsnippets.html) — Встановлює максимальну кількість виділених фрагментів для створення кожного поля
-   [SolrQuery::setHighlightUsePhraseHighlighter](solrquery.sethighlightusephrasehighlighter.html) — Чи слід виділяти вирази лише тоді, коли вони з'являються у фразі запиту
-   [SolrQuery::setMlt](solrquery.setmlt.html) — Включає або вимикає moreLikeThis
-   [SolrQuery::setMltBoost](solrquery.setmltboost.html) — Встановлює, чи буде запит посилено релевантністю цікавого виразу.
-   [SolrQuery::setMltCount](solrquery.setmltcount.html) — Встановлює кількість схожих документів, які повертаються для кожного результату.
-   [SolrQuery::setMltMaxNumQueryTerms](solrquery.setmltmaxnumqueryterms.html) — Встановлює максимальну кількість запитів, що включаються.
-   [SolrQuery::setMltMaxNumTokens](solrquery.setmltmaxnumtokens.html) — Задає максимальну кількість токенів для аналізу
-   [SolrQuery::setMltMaxWordLength](solrquery.setmltmaxwordlength.html) - Встановлює максимальну довжину слова
-   [SolrQuery::setMltMinDocFrequency](solrquery.setmltmindocfrequency.html) - Встановлює частоту mltMinDoc
-   [SolrQuery::setMltMinTermFrequency](solrquery.setmltmintermfrequency.html) — Встановлює частоту, нижче за яку вирази ігноруватимуться у вихідній документації
-   [SolrQuery::setMltMinWordLength](solrquery.setmltminwordlength.html) - Встановлює мінімальну довжину слова
-   [SolrQuery::setOmitHeader](solrquery.setomitheader.html) — Виключає заголовок з результатів, що повертаються.
-   [SolrQuery::setQuery](solrquery.setquery.html) — Встановлює пошуковий запит
-   [SolrQuery::setRows](solrquery.setrows.html) — Задає максимальну кількість рядків, які повертаються в результаті
-   [SolrQuery::setShowDebugInfo](solrquery.setshowdebuginfo.html) — Прапор для відображення налагоджувальної інформації
-   [SolrQuery::setStart](solrquery.setstart.html) — Визначає кількість рядків, що пропускаються.
-   [SolrQuery::setStats](solrquery.setstats.html) — Вмикає або вимикає компонент Stats
-   [SolrQuery::setTerms](solrquery.setterms.html) — Вмикає або вимикає TermsComponent
-   [SolrQuery::setTermsField](solrquery.settermsfield.html) — Встановлює ім'я поля, з якого потрібно одержати вираз
-   [SolrQuery::setTermsIncludeLowerBound](solrquery.settermsincludelowerbound.html) — Включає нижню межу вираження у набір результатів
-   [SolrQuery::setTermsIncludeUpperBound](solrquery.settermsincludeupperbound.html) — Включає верхню межу виразу до набору результатів
-   [SolrQuery::setTermsLimit](solrquery.settermslimit.html) — Встановлює максимальну кількість виразів, що повертаються.
-   [SolrQuery::setTermsLowerBound](solrquery.settermslowerbound.html) - Визначає вираз, з якого треба починати
-   [SolrQuery::setTermsMaxCount](solrquery.settermsmaxcount.html) — Встановлює максимальну частоту документів
-   [SolrQuery::setTermsMinCount](solrquery.settermsmincount.html) — Встановлює мінімальну частоту документів
-   [SolrQuery::setTermsPrefix](solrquery.settermsprefix.html) — Обмежує збіги виразами, що починаються з префіксу
-   [SolrQuery::setTermsReturnRaw](solrquery.settermsreturnraw.html) — Повернути необроблені символи проіндексованого виразу
-   [SolrQuery::setTermsSort](solrquery.settermssort.html) — Визначає, як сортувати повернені умови
-   [SolrQuery::setTermsUpperBound](solrquery.settermsupperbound.html) - Встановлює умову для зупинки
-   [SolrQuery::setTimeAllowed](solrquery.settimeallowed.html) - Час, відведений на пошук