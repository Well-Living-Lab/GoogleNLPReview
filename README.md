
# [Natural Language: Node.js Samples](https://github.com/googleapis/nodejs-language)


[Cloud Natural Language API](https://cloud.google.com/natural-language/docs) provides natural
language understanding technologies to developers, including sentiment analysis, entity
analysis, and syntax analysis. This API is part of the larger Cloud Machine Learning API family.

## Table of Contents

* Before you begin
  * Install the client library
  * Use client library


## Before you begin

1.  Select or create a Cloud Platform project.
1.  Enable billing for your project.
1.  Enable the Natural Language API.
1.  Set up authentication with a service account so you can access the API from your local workstation.

### Installing the client library

```bash
npm install @google-cloud/language
```


### Using the client library

```javascript
async function quickstart() {
  // Imports the Google Cloud client library
  const language = require('@google-cloud/language');

  // Instantiates a client
  const client = new language.LanguageServiceClient();

  // The text to analyze
  const text = 'Hello, world!';

  const document = {
    content: text,
    type: 'PLAIN_TEXT',
  };

  // Detects the sentiment of the text
  const [result] = await client.analyzeSentiment({document: document});
  const sentiment = result.documentSentiment;

  console.log(`Text: ${text}`);
  console.log(`Sentiment score: ${sentiment.score}`);
  console.log(`Sentiment magnitude: ${sentiment.magnitude}`);
}

```





`cd samples`

`npm install`

`cd ..`

## Samples



### Analyze v1

View the [source code](https://github.com/googleapis/nodejs-language/blob/master/samples/analyze.v1.js).

[![Open in Cloud Shell][shell_img]](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-language&page=editor&open_in_editor=samples/analyze.v1.js,samples/README.md)

__Usage:__


`node samples/analyze.v1.js`


-----




### Quickstart

View the [source code](https://github.com/googleapis/nodejs-language/blob/master/samples/quickstart.js).

[![Open in Cloud Shell][shell_img]](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-language&page=editor&open_in_editor=samples/quickstart.js,samples/README.md)

__Usage:__


`node samples/quickstart.js`


-----




### Set Endpoint

View the [source code](https://github.com/googleapis/nodejs-language/blob/master/samples/setEndpoint.js).

[![Open in Cloud Shell][shell_img]](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-language&page=editor&open_in_editor=samples/setEndpoint.js,samples/README.md)

__Usage:__


`node samples/setEndpoint.js`






[shell_img]: https://gstatic.com/cloudssh/images/open-btn.png
[shell_link]: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-language&page=editor&open_in_editor=samples/README.md
[product-docs]: https://cloud.google.com/natural-language/docs/
