
# [Natural Language: Node.js Samples](https://github.com/googleapis/nodejs-language)


[Cloud Natural Language API](https://cloud.google.com/natural-language/docs) provides natural
language understanding technologies to developers, including sentiment analysis, entity
analysis, and syntax analysis. This API is part of the larger Cloud Machine Learning API family.


## Before you begin

1.  [Select or create a Cloud Platform project.](https://console.cloud.google.com/project)
1.  [Enable billing for your project.](https://cloud.google.com/billing/docs/how-to/modify-project?visit_id=637438212173208447-2574262482&rd=1#enable-billing)
1.  [Enable the Natural Language API.](https://console.cloud.google.com/flows/enableapi?apiid=language.googleapis.com)
1.  [Set up authentication with a service account so you can access the API from your local workstation.](https://cloud.google.com/docs/authentication/getting-started)

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


## Sample



### Analyze v1

View the original from Google's Sample repository [source code](https://github.com/googleapis/nodejs-language/blob/master/samples/analyze.v1.js).

__Usage:__

`cd GoogleNLPReview`

`npm install`

`node analyze.v1.js`

Usage Commands include:

analyze.v1.js sentiment-text <text>     => Detects sentiment of a string.

analyze.v1.js sentiment-file <bucketName> <fileName> => Detects sentiment in a file in Google Cloud Storage.

analyze.v1.js entities-text <text>  =>   Detects entities in a string.

analyze.v1.js entities-file <bucketName> <fileName>  =>  Detects entities in a file in Google Cloud Storage.

analyze.v1.js syntax-text <text>         =>                    Detects syntax of a string.

analyze.v1.js syntax-file <bucketName> <fileName>  =>         Detects syntax in a file in Google Cloud Storage.

analyze.v1.js entity-sentiment-text <text>                   Detects sentiment of the entities in a string.

analyze.v1.js entity-sentiment-file <bucketName> <fileName>  Detects sentiment of the entities in a file in Google Cloud Storage.

analyze.v1.js classify-text <text>                           Classifies text of a string.

analyze.v1.js classify-file <bucketName> <fileName>          Classifies text in a file in Google Cloud Storage.






[shell_img]: https://gstatic.com/cloudssh/images/open-btn.png
[shell_link]: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-language&page=editor&open_in_editor=samples/README.md
[product-docs]: https://cloud.google.com/natural-language/docs/
