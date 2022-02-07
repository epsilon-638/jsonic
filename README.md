### jsonic interpreter written in Racket
#### Following along in https://beautifulracket.com/jsonic
```racket
#lang jsonic
[
  @$ 'null $@,
  @$ (* 6 7) $@,
  @$ (= 2 (+ 1 1)) $@,
  @$ (list "array" "of" "strings") $@,
  @$ (hash 'key-1 'null
           'key-2 (even? 3)
           'key-3 (hash 'subkey 21)) $@
]
```
#### Output: JSON
```json
[
  null,
  42,
  true,
  [
		"array",
		"of",
		"strings"
	],
  {
		"key-1": null,
		"key-3": {
								"subkey":21
							},
		"key-2": false
	}
]

```
#### jsonic takes s-expr and interprets it as valid json. This is another proj from the book Beautiful Racket found [here](https://beautifulracket.com/). This section shows how easily one can create a DSL.
