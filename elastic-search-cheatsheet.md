# Elastic Search

## Search

By FIELD [match is for text, term is used for keywords]

```
GET product/_search
{
	"query": {
		"match": {
			"productName": "Spiderman"
		}
	}
}
```

By multiple Fields bool -> [must, must_not, should]
```
GET product/_search
{
	"query": {
		"bool": {
			"must": [
				{
					"match": {
						"productName": "Spiderman"
					}
				},
				{
					"match": {
						"productType": "Feature"
					}
				}
			]
		}
	}
}
```


By FIELD In

```
GET product/_search
{
	"query": {
		"terms": {
			"productId": [316, 420]
		}
	}
}
```