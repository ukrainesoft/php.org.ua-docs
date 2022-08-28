Клас SolrDisMaxQuery

-   [« SolrQuery::setTimeAllowed](solrquery.settimeallowed.html)
    
-   [SolrDisMaxQuery::addBigramPhraseField »](solrdismaxquery.addbigramphrasefield.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrDisMaxQuery
    

# Клас SolrDisMaxQuery

(No version information available, might only be in Git)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class SolrDisMaxQuery
     

     
      extends
       SolrQuery
     

     implements 
       Serializable {


    /* Наследуемые свойства */
    
     const
     int
      SolrQuery::ORDER_ASC = 0;
const
     int
      SolrQuery::ORDER_DESC = 1;
const
     int
      SolrQuery::FACET_SORT_INDEX = 0;
const
     int
      SolrQuery::FACET_SORT_COUNT = 1;
const
     int
      SolrQuery::TERMS_SORT_INDEX = 0;
const
     int
      SolrQuery::TERMS_SORT_COUNT = 1;



    /* Методы */
    
   public __construct(string $q = ?)

    public addBigramPhraseField(string $field, string $boost, string $slop = ?): SolrDisMaxQuery
public addBoostQuery(string $field, string $value, string $boost = ?): SolrDisMaxQuery
public addPhraseField(string $field, string $boost, string $slop = ?): SolrDisMaxQuery
public addQueryField(string $field, string $boost = ?): SolrDisMaxQuery
public addTrigramPhraseField(string $field, string $boost, string $slop = ?): SolrDisMaxQuery
public addUserField(string $field): SolrDisMaxQuery
public removeBigramPhraseField(string $field): SolrDisMaxQuery
public removeBoostQuery(string $field): SolrDisMaxQuery
public removePhraseField(string $field): SolrDisMaxQuery
public removeQueryField(string $field): SolrDisMaxQuery
public removeTrigramPhraseField(string $field): SolrDisMaxQuery
public removeUserField(string $field): SolrDisMaxQuery
public setBigramPhraseFields(string $fields): SolrDisMaxQuery
public setBigramPhraseSlop(string $slop): SolrDisMaxQuery
public setBoostFunction(string $function): SolrDisMaxQuery
public setBoostQuery(string $q): SolrDisMaxQuery
public setMinimumMatch(string $value): SolrDisMaxQuery
public setPhraseFields(string $fields): SolrDisMaxQuery
public setPhraseSlop(string $slop): SolrDisMaxQuery
public setQueryAlt(string $q): SolrDisMaxQuery
public setQueryPhraseSlop(string $slop): SolrDisMaxQuery
public setTieBreaker(string $tieBreaker): SolrDisMaxQuery
public setTrigramPhraseFields(string $fields): SolrDisMaxQuery
public setTrigramPhraseSlop(string $slop): SolrDisMaxQuery
public setUserFields(string $fields): SolrDisMaxQuery
public useDisMaxQueryParser(): SolrDisMaxQuery
public useEDisMaxQueryParser(): SolrDisMaxQuery


    /* Наследуемые методы */
    public SolrQuery::addExpandFilterQuery(string $fq): SolrQuery
public SolrQuery::addExpandSortField(string $field, string $order = ?): SolrQuery
public SolrQuery::addFacetDateField(string $dateField): SolrQuery
public SolrQuery::addFacetDateOther(string $value, string $field_override = ?): SolrQuery
public SolrQuery::addFacetField(string $field): SolrQuery
public SolrQuery::addFacetQuery(string $facetQuery): SolrQuery
public SolrQuery::addField(string $field): SolrQuery
public SolrQuery::addFilterQuery(string $fq): SolrQuery
public SolrQuery::addGroupField(string $value): SolrQuery
public SolrQuery::addGroupFunction(string $value): SolrQuery
public SolrQuery::addGroupQuery(string $value): SolrQuery
public SolrQuery::addGroupSortField(string $field, int $order = ?): SolrQuery
public SolrQuery::addHighlightField(string $field): SolrQuery
public SolrQuery::addMltField(string $field): SolrQuery
public SolrQuery::addMltQueryField(string $field, float $boost): SolrQuery
public SolrQuery::addSortField(string $field, int $order = SolrQuery::ORDER_DESC): SolrQuery
public SolrQuery::addStatsFacet(string $field): SolrQuery
public SolrQuery::addStatsField(string $field): SolrQuery
public SolrQuery::collapse(SolrCollapseFunction $collapseFunction): SolrQuery
public SolrQuery::getExpand(): bool
public SolrQuery::getExpandFilterQueries(): array
public SolrQuery::getExpandQuery(): array
public SolrQuery::getExpandRows(): int
public SolrQuery::getExpandSortFields(): array
public SolrQuery::getFacet(): bool
public SolrQuery::getFacetDateEnd(string $field_override = ?): string
public SolrQuery::getFacetDateFields(): array
public SolrQuery::getFacetDateGap(string $field_override = ?): string
public SolrQuery::getFacetDateHardEnd(string $field_override = ?): string
public SolrQuery::getFacetDateOther(string $field_override = ?): array
public SolrQuery::getFacetDateStart(string $field_override = ?): string
public SolrQuery::getFacetFields(): array
public SolrQuery::getFacetLimit(string $field_override = ?): int
public SolrQuery::getFacetMethod(string $field_override = ?): string
public SolrQuery::getFacetMinCount(string $field_override = ?): int
public SolrQuery::getFacetMissing(string $field_override = ?): bool
public SolrQuery::getFacetOffset(string $field_override = ?): int
public SolrQuery::getFacetPrefix(string $field_override = ?): string
public SolrQuery::getFacetQueries(): array
public SolrQuery::getFacetSort(string $field_override = ?): int
public SolrQuery::getFields(): array
public SolrQuery::getFilterQueries(): array
public SolrQuery::getGroup(): bool
public SolrQuery::getGroupCachePercent(): int
public SolrQuery::getGroupFacet(): bool
public SolrQuery::getGroupFields(): array
public SolrQuery::getGroupFormat(): string
public SolrQuery::getGroupFunctions(): array
public SolrQuery::getGroupLimit(): int
public SolrQuery::getGroupMain(): bool
public SolrQuery::getGroupNGroups(): bool
public SolrQuery::getGroupOffset(): int
public SolrQuery::getGroupQueries(): array
public SolrQuery::getGroupSortFields(): array
public SolrQuery::getGroupTruncate(): bool
public SolrQuery::getHighlight(): bool
public SolrQuery::getHighlightAlternateField(string $field_override = ?): string
public SolrQuery::getHighlightFields(): array
public SolrQuery::getHighlightFormatter(string $field_override = ?): string
public SolrQuery::getHighlightFragmenter(string $field_override = ?): string
public SolrQuery::getHighlightFragsize(string $field_override = ?): int
public SolrQuery::getHighlightHighlightMultiTerm(): bool
public SolrQuery::getHighlightMaxAlternateFieldLength(string $field_override = ?): int
public SolrQuery::getHighlightMaxAnalyzedChars(): int
public SolrQuery::getHighlightMergeContiguous(string $field_override = ?): bool
public SolrQuery::getHighlightRegexMaxAnalyzedChars(): int
public SolrQuery::getHighlightRegexPattern(): string
public SolrQuery::getHighlightRegexSlop(): float
public SolrQuery::getHighlightRequireFieldMatch(): bool
public SolrQuery::getHighlightSimplePost(string $field_override = ?): string
public SolrQuery::getHighlightSimplePre(string $field_override = ?): string
public SolrQuery::getHighlightSnippets(string $field_override = ?): int
public SolrQuery::getHighlightUsePhraseHighlighter(): bool
public SolrQuery::getMlt(): bool
public SolrQuery::getMltBoost(): bool
public SolrQuery::getMltCount(): int
public SolrQuery::getMltFields(): array
public SolrQuery::getMltMaxNumQueryTerms(): int
public SolrQuery::getMltMaxNumTokens(): int
public SolrQuery::getMltMaxWordLength(): int
public SolrQuery::getMltMinDocFrequency(): int
public SolrQuery::getMltMinTermFrequency(): int
public SolrQuery::getMltMinWordLength(): int
public SolrQuery::getMltQueryFields(): array
public SolrQuery::getQuery(): string
public SolrQuery::getRows(): int
public SolrQuery::getSortFields(): array
public SolrQuery::getStart(): int
public SolrQuery::getStats(): bool
public SolrQuery::getStatsFacets(): array
public SolrQuery::getStatsFields(): array
public SolrQuery::getTerms(): bool
public SolrQuery::getTermsField(): string
public SolrQuery::getTermsIncludeLowerBound(): bool
public SolrQuery::getTermsIncludeUpperBound(): bool
public SolrQuery::getTermsLimit(): int
public SolrQuery::getTermsLowerBound(): string
public SolrQuery::getTermsMaxCount(): int
public SolrQuery::getTermsMinCount(): int
public SolrQuery::getTermsPrefix(): string
public SolrQuery::getTermsReturnRaw(): bool
public SolrQuery::getTermsSort(): int
public SolrQuery::getTermsUpperBound(): string
public SolrQuery::getTimeAllowed(): int
public SolrQuery::removeExpandFilterQuery(string $fq): SolrQuery
public SolrQuery::removeExpandSortField(string $field): SolrQuery
public SolrQuery::removeFacetDateField(string $field): SolrQuery
public SolrQuery::removeFacetDateOther(string $value, string $field_override = ?): SolrQuery
public SolrQuery::removeFacetField(string $field): SolrQuery
public SolrQuery::removeFacetQuery(string $value): SolrQuery
public SolrQuery::removeField(string $field): SolrQuery
public SolrQuery::removeFilterQuery(string $fq): SolrQuery
public SolrQuery::removeHighlightField(string $field): SolrQuery
public SolrQuery::removeMltField(string $field): SolrQuery
public SolrQuery::removeMltQueryField(string $queryField): SolrQuery
public SolrQuery::removeSortField(string $field): SolrQuery
public SolrQuery::removeStatsFacet(string $value): SolrQuery
public SolrQuery::removeStatsField(string $field): SolrQuery
public SolrQuery::setEchoHandler(bool $flag): SolrQuery
public SolrQuery::setEchoParams(string $type): SolrQuery
public SolrQuery::setExpand(bool $value): SolrQuery
public SolrQuery::setExpandQuery(string $q): SolrQuery
public SolrQuery::setExpandRows(int $value): SolrQuery
public SolrQuery::setExplainOther(string $query): SolrQuery
public SolrQuery::setFacet(bool $flag): SolrQuery
public SolrQuery::setFacetDateEnd(string $value, string $field_override = ?): SolrQuery
public SolrQuery::setFacetDateGap(string $value, string $field_override = ?): SolrQuery
public SolrQuery::setFacetDateHardEnd(bool $value, string $field_override = ?): SolrQuery
public SolrQuery::setFacetDateStart(string $value, string $field_override = ?): SolrQuery
public SolrQuery::setFacetEnumCacheMinDefaultFrequency(int $frequency, string $field_override = ?): SolrQuery
public SolrQuery::setFacetLimit(int $limit, string $field_override = ?): SolrQuery
public SolrQuery::setFacetMethod(string $method, string $field_override = ?): SolrQuery
public SolrQuery::setFacetMinCount(int $mincount, string $field_override = ?): SolrQuery
public SolrQuery::setFacetMissing(bool $flag, string $field_override = ?): SolrQuery
public SolrQuery::setFacetOffset(int $offset, string $field_override = ?): SolrQuery
public SolrQuery::setFacetPrefix(string $prefix, string $field_override = ?): SolrQuery
public SolrQuery::setFacetSort(int $facetSort, string $field_override = ?): SolrQuery
public SolrQuery::setGroup(bool $value): SolrQuery
public SolrQuery::setGroupCachePercent(int $percent): SolrQuery
public SolrQuery::setGroupFacet(bool $value): SolrQuery
public SolrQuery::setGroupFormat(string $value): SolrQuery
public SolrQuery::setGroupLimit(int $value): SolrQuery
public SolrQuery::setGroupMain(string $value): SolrQuery
public SolrQuery::setGroupNGroups(bool $value): SolrQuery
public SolrQuery::setGroupOffset(int $value): SolrQuery
public SolrQuery::setGroupTruncate(bool $value): SolrQuery
public SolrQuery::setHighlight(bool $flag): SolrQuery
public SolrQuery::setHighlightAlternateField(string $field, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightFormatter(string $formatter, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightFragmenter(string $fragmenter, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightFragsize(int $size, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightHighlightMultiTerm(bool $flag): SolrQuery
public SolrQuery::setHighlightMaxAlternateFieldLength(int $fieldLength, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightMaxAnalyzedChars(int $value): SolrQuery
public SolrQuery::setHighlightMergeContiguous(bool $flag, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightRegexMaxAnalyzedChars(int $maxAnalyzedChars): SolrQuery
public SolrQuery::setHighlightRegexPattern(string $value): SolrQuery
public SolrQuery::setHighlightRegexSlop(float $factor): SolrQuery
public SolrQuery::setHighlightRequireFieldMatch(bool $flag): SolrQuery
public SolrQuery::setHighlightSimplePost(string $simplePost, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightSimplePre(string $simplePre, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightSnippets(int $value, string $field_override = ?): SolrQuery
public SolrQuery::setHighlightUsePhraseHighlighter(bool $flag): SolrQuery
public SolrQuery::setMlt(bool $flag): SolrQuery
public SolrQuery::setMltBoost(bool $flag): SolrQuery
public SolrQuery::setMltCount(int $count): SolrQuery
public SolrQuery::setMltMaxNumQueryTerms(int $value): SolrQuery
public SolrQuery::setMltMaxNumTokens(int $value): SolrQuery
public SolrQuery::setMltMaxWordLength(int $maxWordLength): SolrQuery
public SolrQuery::setMltMinDocFrequency(int $minDocFrequency): SolrQuery
public SolrQuery::setMltMinTermFrequency(int $minTermFrequency): SolrQuery
public SolrQuery::setMltMinWordLength(int $minWordLength): SolrQuery
public SolrQuery::setOmitHeader(bool $flag): SolrQuery
public SolrQuery::setQuery(string $query): SolrQuery
public SolrQuery::setRows(int $rows): SolrQuery
public SolrQuery::setShowDebugInfo(bool $flag): SolrQuery
public SolrQuery::setStart(int $start): SolrQuery
public SolrQuery::setStats(bool $flag): SolrQuery
public SolrQuery::setTerms(bool $flag): SolrQuery
public SolrQuery::setTermsField(string $fieldname): SolrQuery
public SolrQuery::setTermsIncludeLowerBound(bool $flag): SolrQuery
public SolrQuery::setTermsIncludeUpperBound(bool $flag): SolrQuery
public SolrQuery::setTermsLimit(int $limit): SolrQuery
public SolrQuery::setTermsLowerBound(string $lowerBound): SolrQuery
public SolrQuery::setTermsMaxCount(int $frequency): SolrQuery
public SolrQuery::setTermsMinCount(int $frequency): SolrQuery
public SolrQuery::setTermsPrefix(string $prefix): SolrQuery
public SolrQuery::setTermsReturnRaw(bool $flag): SolrQuery
public SolrQuery::setTermsSort(int $sortType): SolrQuery
public SolrQuery::setTermsUpperBound(string $upperBound): SolrQuery
public SolrQuery::setTimeAllowed(int $timeAllowed): SolrQuery


   }
```

## Обумовлені константи

**`SolrDisMaxQuery::ORDER_ASC`**

Використовується для вказівки того, що сортування має бути в порядку зростаючому (дублювати для спрощення міграції)

**`SolrDisMaxQuery::ORDER_DESC`**

Використовується для вказівки, що сортування має бути в порядку зменшення (дублюється для спрощення міграції)

**`SolrDisMaxQuery::FACET_SORT_INDEX`**

Використовується для вказівки сортування фасету за індексом (дублюється для спрощення міграції)

**`SolrDisMaxQuery::FACET_SORT_COUNT`**

Використовується для сортування фасету за кількістю (дублюється для спрощення міграції)

**`SolrDisMaxQuery::TERMS_SORT_INDEX`**

Використовується в TermsComponent (дублюється для спрощення міграції)

**`SolrDisMaxQuery::TERMS_SORT_COUNT`**

Використовується в TermsComponent (дублюється для спрощення міграції)

## Зміст

-   [SolrDisMaxQuery::addBigramPhraseField](solrdismaxquery.addbigramphrasefield.html) - Додає поле фразової біграми (параметр pf2)
-   [SolrDisMaxQuery::addBoostQuery](solrdismaxquery.addboostquery.html) — Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
-   [SolrDisMaxQuery::addPhraseField](solrdismaxquery.addphrasefield.html) - Додає поле фрази (параметр pf)
-   [SolrDisMaxQuery::addQueryField](solrdismaxquery.addqueryfield.html) — Додає поле запиту із необов'язковим підвищенням (параметр qf)
-   [SolrDisMaxQuery::addTrigramPhraseField](solrdismaxquery.addtrigramphrasefield.html) - Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::addUserField](solrdismaxquery.adduserfield.html) — Додає поле до параметра поля користувача (uf)
-   [SolrDisMaxQuery::\_\_construct](solrdismaxquery.construct.html) - Конструктор класу
-   [SolrDisMaxQuery::removeBigramPhraseField](solrdismaxquery.removebigramphrasefield.html) - Видаляє поле біграми фрази (параметр pf2)
-   [SolrDisMaxQuery::removeBoostQuery](solrdismaxquery.removeboostquery.html) — Видаляє часткове підвищення запиту на ім'я поля (bq)
-   [SolrDisMaxQuery::removePhraseField](solrdismaxquery.removephrasefield.html) - Видаляє поле фрази (параметра)
-   [SolrDisMaxQuery::removeQueryField](solrdismaxquery.removequeryfield.html) — Видаляє поле запиту (параметр qf)
-   [SolrDisMaxQuery::removeTrigramPhraseField](solrdismaxquery.removetrigramphrasefield.html) - Видаляє поле триграми (параметр pf3)
-   [SolrDisMaxQuery::removeUserField](solrdismaxquery.removeuserfield.html) — Видаляє поле з параметра поля користувача (uf)
-   [SolrDisMaxQuery::setBigramPhraseFields](solrdismaxquery.setbigramphrasefields.html) - Встановлює поля біграми фрази та їх посилення (і відхилення) за допомогою параметра pf2
-   [SolrDisMaxQuery::setBigramPhraseSlop](solrdismaxquery.setbigramphraseslop.html) - Встановлює коефіцієнт відхилення біграми фрази (параметр ps2)
-   [SolrDisMaxQuery::setBoostFunction](solrdismaxquery.setboostfunction.html) - Встановлює функцію посилення (параметр bf)
-   [SolrDisMaxQuery::setBoostQuery](solrdismaxquery.setboostquery.html) - Безпосередньо встановлює параметр запиту посилення (bq)
-   [SolrDisMaxQuery::setMinimumMatch](solrdismaxquery.setminimummatch.html) - Встановлює мінімальну відповідність "Should" (mm)
-   [SolrDisMaxQuery::setPhraseFields](solrdismaxquery.setphrasefields.html) — Встановлює поля фрази та їх посилення (і відхилення) за допомогою pf2
-   [SolrDisMaxQuery::setPhraseSlop](solrdismaxquery.setphraseslop.html) — Встановлює коефіцієнт відхилення за промовчанням для запитів фраз (параметр ps)
-   [SolrDisMaxQuery::setQueryAlt](solrdismaxquery.setqueryalt.html) - Встановлює альтернативний запит (параметр q.alt)
-   [SolrDisMaxQuery::setQueryPhraseSlop](solrdismaxquery.setqueryphraseslop.html) — Визначає коефіцієнт відхилення, дозволений для фразових запитів, які явно включені в рядок запиту користувача (параметр qf)
-   [SolrDisMaxQuery::setTieBreaker](solrdismaxquery.settiebreaker.html) - Встановлює параметр Tie Breaker (параметр tie)
-   [SolrDisMaxQuery::setTrigramPhraseFields](solrdismaxquery.settrigramphrasefields.html) - Безпосередньо встановлює поля триграми фрази (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseSlop](solrdismaxquery.settrigramphraseslop.html) - Встановлює коефіцієнт відхилення триграми фрази (параметр ps3)
-   [SolrDisMaxQuery::setUserFields](solrdismaxquery.setuserfields.html) — Встановлює параметр полів користувача (uf)
-   [SolrDisMaxQuery::useDisMaxQueryParser](solrdismaxquery.usedismaxqueryparser.html) - Перемикає QueryParser на DisMax Query Parser
-   [SolrDisMaxQuery::useEDisMaxQueryParser](solrdismaxquery.useedismaxqueryparser.html) - Перемикає QueryParser на EDisMax