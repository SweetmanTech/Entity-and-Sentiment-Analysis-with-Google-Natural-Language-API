# QwikLabs - Entity and Sentiment Analysis with the Natural Language API
Lab completed by Pat Sweetman during Google Cloud OnAir: The Journey From Big Data to AI. Sources include:
* QwikLabs
* Google

## Languages
* JSON
* curl
## Uses
This repository should be used as a reference. This does not build, and is not an application. Any attempt to build this as an application will almost certainly fail :)
## API Usage
Curl request can be used to with json payload including Image URL string or Google Storage URL
1. Be sure to `export API_KEY={your-api-key}` for this curl command to work
2. You should be located in the same directory as `request.json`
3. NLP - Analyze Entities
```
curl "https://language.googleapis.com/v1/documents:analyzeEntities?key=${API_KEY}" \
  -s -X POST -H "Content-Type: application/json" --data-binary @request.json
```
4. NLP - Analyze Sentimentd
```
curl "https://language.googleapis.com/v1/documents:analyzeSentiment?key=${API_KEY}" \
  -s -X POST -H "Content-Type: application/json" --data-binary @sentiment-request.json
```
4. NLP - Analyze Entity Sentiment
```
curl "https://language.googleapis.com/v1/documents:analyzeEntitySentiment?key=${API_KEY}" \
  -s -X POST -H "Content-Type: application/json" --data-binary @sentiment-entity-request.json
```
5. NLP - Annotate Text
```
curl "https://language.googleapis.com/v1/documents:analyzeSyntax?key=${API_KEY}" \
  -s -X POST -H "Content-Type: application/json" --data-binary @syntax-request.json
```
6. NLP - Multilingual Analysis
```
curl "https://language.googleapis.com/v1/documents:analyzeEntities?key=${API_KEY}" \
  -s -X POST -H "Content-Type: application/json" --data-binary @multilingual-request.json
```
