# Filter Expressions

<code>/query</code> endpoints take an optional <code>filter</code> parameter that accepts boolean text expressions in the following format:

<code>\<<em>field</em>\> \<<em>operator</em>\> \<<em>test_condition</em>\>

<aside class="success">Keywords (operators, logical conjunctions, and field names) in text expressions are <strong>case-sensitive</strong>.</aside>

## Fields

Allowable fields may vary depending on the data type and NIAGADS Open Access resource being queried.  

Each knowledgebase provides a <em>Helper</em> <code>/query/filter</code> endpoint that generates a list of allowable filter fields for its filters; see for, example, the available fields for [FILER queries](#helper-allowable-filter-fields)

## Text Filter Expression Operators

|Operator|Description|
|---|---|
|eq|<code>equals</code>: case-sensitive, exact text match to field value|
|neq|<code>not equals</code>: case-sensitive, negative exact text match to field value|
|like|<code>ilike</code>: case-insensitive, substring matching against field value|

## Complex expressions

Filter expressions can be combind using the logical conjunction operator <code>and</code>. For example:

> data_source eq ENCODE and biosample like lung


<aside class="notice">Currently only <code>and</code> expressions are supported.  Support for logical <code>or</code> is coming soon.</aside>
