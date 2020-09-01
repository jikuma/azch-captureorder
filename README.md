你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。

# CaptureOrder

[![Build Status](https://dev.azure.com/theazurechallenge/Kubernetes/_apis/build/status/Code/Azure.azch-captureorder)](https://dev.azure.com/theazurechallenge/Kubernetes/_build/latest?definitionId=10)

A containerised Go swagger API to capture orders, write them to MongoDb and an AMQP message queue.

## Usage

### Swagger

Access the Swagger UI at [http://[host]/swagger]()

### Submitting an order

```
POST /v1/Order HTTP/1.1
Host: [host]:[port]
Content-Type: application/json

{
  "EmailAddress": "test@domain.com",
  "PreferredLanguage": "en"
}
```

## Environment Variables

The following environment variables need to be passed to the container:

### Logging

```
ENV TEAMNAME=[YourTeamName]
ENV CHALLENGEAPPINSIGHTS_KEY=[Challenge Application Insights Key] # Override, if given one by the proctors
```

### For MongoDB

```
ENV MONGOHOST=<mongo service name>.<namespace>
```

```
ENV MONGOUSER=admin
```

```
ENV MONGOPASSWORD=<password for MongoDB>
```

### For CosmosDB

```
ENV MONGOHOST=<cosmosdb account name>.documents.azure.com
```

```
ENV MONGOUSER=<cosmosdb username>
```

```
ENV MONGOPASSWORD=<cosmosdb primary password>
```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
