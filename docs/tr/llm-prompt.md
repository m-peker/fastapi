### Target language

Translate to Turkish (Türkçe).

Language code: tr.

### Core principle

Don't translate word-by-word. Rewrite naturally in Turkish as if writing the doc from scratch. Preserve meaning, but prioritize fluency over literal accuracy.

### Grammar and tone

- Use instructional Turkish, consistent with existing Turkish docs.
- Use imperative/guide language (e.g. "açalım", "gidin", "kopyalayalım", "bir bakalım").
- Avoid filler words and overly long sentences.
- Ensure sentences make sense in Turkish context — adjust structure, conjunctions, and verb forms as needed for natural flow (e.g. use "Ancak" instead of "Ve" when connecting contrasting sentences, use "-maktadır/-mektedir" for formal statements).

### Headings

- Follow existing Turkish heading style (Title Case where used; no trailing period).

### Quotes

- Keep quote style consistent with existing Turkish docs (typically ASCII quotes in text).
- Never modify quotes inside inline code, code blocks, URLs, or file paths.

### Ellipsis

- Keep ellipsis style (`...`) consistent with existing Turkish docs.
- Never modify `...` in code, URLs, or CLI examples.

### Consistency

- Use the same translation for the same term throughout the document.
- If you translate a concept one way, keep it consistent across all occurrences.

### Links and references

- Never modify link syntax like `{.internal-link target=_blank}`.
- Keep markdown link structure intact: `[text](url){.internal-link}`.

### Suffixes on English terms

English technical terms keep their English spelling, but they still take Turkish suffixes. Attach the suffix with an apostrophe, and pick it from how the word is *pronounced*, not from how it is spelled.

- Vowel harmony follows the last spoken vowel of the word.

Example – `Starlette` is pronounced "starlet", so its last spoken vowel is a front vowel:

```
Starlette'in, Starlette'i, Starlette'te
```

Do NOT write (Turkish) – these use back vowels:

```
Starlette'ın, Starlette'a, Starlette'tan
```

- If the word ends in a vowel sound and the suffix starts with a vowel, insert a buffer consonant: `y` for the dative and accusative, `n` for the genitive and for suffixes added to a possessive.

Example:

Source (English):

```
Let's focus on the dependency first.
```

Translate with (Turkish):

```
Önce dependency'ye odaklanalım.
```

Do NOT translate with (Turkish) – notice the missing `y`:

```
Önce dependency'e odaklanalım.
```

The same word takes `n` in the genitive:

```
dependency'nin, body'nin, query'nin, cookie'nin
```

- The suffixes `-de`/`-da` and `-den`/`-dan` become `-te`/`-ta` and `-ten`/`-tan` after a voiceless consonant sound (`p`, `ç`, `t`, `k`, `f`, `h`, `s`, `ş`).

Example – `response` ends in a voiceless `s`, `request` and `path` end in a voiceless `t`:

```
response'ta, response'tan, request'ten, path'te
```

Do NOT write (Turkish):

```
response'da, response'dan, request'den, path'de
```

- Suffix the same term the same way throughout the document. Use these canonical forms for the most frequent terms:

```
request'i, request'in, request'e, request'te, request'ten, request'ler
response'u, response'un, response'a, response'ta, response'tan, response'lar
path'i, path'in, path'e, path'te, path'ten, path'ler
query'yi, query'nin, query'ye, query'de, query'den, query'ler
body'yi, body'nin, body'ye, body'de, body'den, body'ler
cookie'yi, cookie'nin, cookie'ye, cookie'de, cookie'den, cookie'ler
header'ı, header'ın, header'a, header'da, header'dan, header'lar
dependency'yi, dependency'nin, dependency'ye, dependency'de, dependency'den, dependency'ler
decorator'ı, decorator'ın, decorator'a, decorator'da, decorator'dan, decorator'lar
middleware'i, middleware'in, middleware'e, middleware'de, middleware'den, middleware'ler
endpoint'i, endpoint'in, endpoint'e, endpoint'te, endpoint'ten, endpoint'ler
instance'ı, instance'ın, instance'a, instance'ta, instance'tan, instance'lar
route'u, route'un, route'a, route'ta, route'tan, route'lar
worker'ı, worker'ın, worker'a, worker'dan, worker'lar
Starlette'i, Starlette'in, Starlette'e, Starlette'te, Starlette'ten
```

- After the plural `'lar`/`'ler`, any further suffix follows that plural, not the English word.

```
response'larda, header'lardan, dependency'lerin
```

Do NOT write (Turkish):

```
response'larta, header'lartan
```

### Preferred translations / glossary

Do not translate technical terms like path, route, request, response, query, body, cookie, and header, keep them as is.

- You can use a more instructional style, that is consistent with the document, you can add the Turkish version of the term in parenthesis if it is not something very obvious, or an advanced concept, but do not over do it, do it only the first time it is mentioned, but keep the English term as the primary word.

Below is a list of English terms and their preferred Turkish handling, separated by a colon (:). Use these, do not use your own. If an existing translation does not use them, update it to use them.

* decorator: decorator (do not translate to "dekoratör")
* deploy: deploy (do not translate to "dağıtım" or "yayına alma")
* endpoint: endpoint (do not translate to "uç nokta")
* instance: instance (do not translate to "örnek", which is already used for "example")
* middleware: middleware (do not translate to "ara katman")
* worker: worker (do not translate to "işçi" or "çalışan")
* request body: request body (do not translate to "istek gövdesi")
* response body: response body (do not translate to "yanıt gövdesi")
* type hint: type hint (do not translate to "tip ipucu" or "tip belirteci")
* dependency: dependency (keep the English term as the primary word, the Turkish gloss "bağımlılık" in parentheses only the first time it appears in a page)
* package: paket (keep the English "package" only when it names the Python concept, as in "Python package" or "subpackage")
* validation: doğrulama (do not keep the English "validation" in prose, but never change it inside URLs, code, or heading anchors like `{ #validation }`)
* to validate: doğrulamak
* type (as in a Python type): tip (do not translate to "tür")
* data type: veri tipi (do not translate to "veri türü")

### `///` admonitions

- Keep the admonition keyword in English (do not translate `note`, `tip`, etc.).
- If a title is present, prefer these canonical titles:

- `/// note | Not`
- `/// note | Teknik Detaylar`
- `/// tip | İpucu`
- `/// warning | Uyarı`
- `/// info | Bilgi`
- `/// check | Ek bilgi`

Prefer `İpucu` over `Ipucu`.
