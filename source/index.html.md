---
title: NIAGADS API v0.0.1
language_tabs:
  - python: Python
  - r: R
  - perl: Perl
  - ruby: Ruby
language_clients:
  - python: ""
  - r: ""
  - perl: ""
  - ruby: ""
toc_footers: []
includes: 
  - filters
  - schemas
search: false
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: widdershins v4.0.1

---

<h1 id="niagads-api">NIAGADS API v0.0.1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

an application programming interface (API) that provides programmatic access to Open-Access resources at the NIA Genetics of Alzheimer's Disease Data Storage Site (NIAGADS)

Base URLs:

* <a href="/api">/api</a>

<a href="http://example.com/terms/">Terms of service</a>
Email: <a href="mailto:help@niagads.org">NIAGADS Support</a> 
License: <a href="https://www.apache.org/licenses/LICENSE-2.0.html">Apache 2.0</a>

<h1 id="niagads-api-default">Default</h1>

## Read Root

<a id="opIdread_root__get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /`

> Example responses

> 200 Response

```json
null
```

<h3 id="read-root-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|

<h3 id="read-root-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="niagads-api-filer-functional-genomics-repository">FILER Functional Genomics Repository</h1>

## About

<a id="opIdabout_filer__get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /filer/`

about the FILER Functional Genomics Repository

> Example responses

> 200 Response

```json
null
```

<h3 id="about-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|

<h3 id="about-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Get Track Metadata

<a id="opIdGet_track_metadata_filer_track_record__track__get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/track/record/{track}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/track/record/{track}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /filer/track/record/{track}`

retrieve metadata for the functional genomics `track` specified in the path

<h3 id="get-track-metadata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|track|path|string|true|FILER track identifier|

> Example responses

> 200 Response

```json
null
```

<h3 id="get-track-metadata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="get-track-metadata-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Get Metadata For Multiple Tracks

<a id="opIdGet_metadata_for_multiple_tracks_filer_track_record_get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/track/record', params={
  'track': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/track/record',
  params: {
  'track' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /filer/track/record`

retrieve metadata for one or more functional genomics tracks from FILER

<h3 id="get-metadata-for-multiple-tracks-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|track|query|string|true|comma separated list of one or more FILER track identifiers|

> Example responses

> 200 Response

```json
null
```

<h3 id="get-metadata-for-multiple-tracks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="get-metadata-for-multiple-tracks-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Get Track Data

<a id="opIdGet_track_data_filer_track_data__track__get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/track/data/{track}', params={
  'loc': 'chr19:10000-40000'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/track/data/{track}',
  params: {
  'loc' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /filer/track/data/{track}`

retrieve functional genomics track data from FILER in the specified region

<h3 id="get-track-data-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|track|path|string|true|FILER track identifier|
|loc|query|string|true|genomic region to query; for a chromosome, N, please specify as chrN:start-end or N:start-end|

> Example responses

> 200 Response

```json
null
```

<h3 id="get-track-data-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="get-track-data-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Get Data From Multiple Tracks

<a id="opIdGet_data_from_multiple_tracks_filer_track_data_get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/track/data', params={
  'track': 'string',  'loc': 'chr19:10000-40000'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/track/data',
  params: {
  'track' => 'string',
'loc' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /filer/track/data`

retrieve data from one or more functional genomics tracks from FILER in the specified region

<h3 id="get-data-from-multiple-tracks-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|track|query|string|true|comma separated list of one or more FILER track identifiers|
|loc|query|string|true|genomic region to query; for a chromosome, N, please specify as chrN:start-end or N:start-end|

> Example responses

> 200 Response

```json
null
```

<h3 id="get-data-from-multiple-tracks-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="get-data-from-multiple-tracks-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Track Metadata Text Search

<a id="opIdTrack_Metadata_Text_Search_filer_query_tracks_get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/query/tracks', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/query/tracks',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /filer/query/tracks`

find functional genomics tracks using category filters or by a keyword search againts all text fields in the track metadata

<h3 id="track-metadata-text-search-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|keyword|query|any|false|search all text fields by keyword|
|assembly|query|any|false|reference genome build (assembly)|
|filter|query|string|false|filter expresssion string|
|limit|query|any|false|maximum number of results to return; please note that `pagination is not yet implemented`|
|page|query|any|false|current page; please note that `pagination is not yet implemented`|
|countOnly|query|any|false|return result size (count) only|
|idsOnly|query|any|false|return only the IDS (no annotation or metadata) for matching records|

> Example responses

> 200 Response

```json
null
```

<h3 id="track-metadata-text-search-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="track-metadata-text-search-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Get Data From Tracks Meeting Search Criteria

<a id="opIdGet_Data_from_Tracks_meeting_Search_Criteria_filer_query_region_get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/query/region', params={
  'loc': 'chr19:10000-40000'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/query/region',
  params: {
  'loc' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /filer/query/region`

retrieve data in a region of interest from all functional genomics tracks whose metadata meets the search or filter criteria

<h3 id="get-data-from-tracks-meeting-search-criteria-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|keyword|query|any|false|search all text fields by keyword|
|assembly|query|any|false|reference genome build (assembly)|
|filter|query|string|false|filter expresssion string|
|loc|query|string|true|genomic region to query; for a chromosome, N, please specify as chrN:start-end or N:start-end|
|limit|query|any|false|maximum number of results to return; please note that `pagination is not yet implemented`|
|page|query|any|false|current page; please note that `pagination is not yet implemented`|
|countOnly|query|any|false|return result size (count) only|
|idsOnly|query|any|false|return only the IDS (no annotation or metadata) for matching records|

> Example responses

> 200 Response

```json
null
```

<h3 id="get-data-from-tracks-meeting-search-criteria-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="get-data-from-tracks-meeting-search-criteria-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Helper: Allowable Filter Fields

<a id="opIdHelper__Allowable_Filter_Fields_filer_query_filter_get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/query/filter', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/query/filter',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /filer/query/filter`

get list of allowable fields for filter-based searches of FILER track metadata

> Example responses

> 200 Response

```json
null
```

<h3 id="helper:-allowable-filter-fields-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|

<h3 id="helper:-allowable-filter-fields-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Helper: Filter Field Values

<a id="opIdHelper__Filter_Field_Values_filer_query_filter__field__get"></a>

> Code samples

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/filer/query/filter/{field}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api/filer/query/filter/{field}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /filer/query/filter/{field}`

get list of values and associated FILER track counts for each allowable filter field

<h3 id="helper:-filter-field-values-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|field|path|string|true|filter field; please note that there are too many possible values for `biosample`; the returned result summarizes over broad `tissue categories` only|

#### Enumerated Values

|Parameter|Value|
|---|---|
|field|biosample|
|field|antibody|
|field|assay|
|field|feature|
|field|analysis|
|field|classification|
|field|category|
|field|data_source|

> Example responses

> 200 Response

```json
null
```

<h3 id="helper:-filter-field-values-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="helper:-filter-field-values-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>
