# beer-crawler

> Uses [bolaget.io](https://bolaget.io/) to check for beer news

This project consists of a AWS Lambda function which uses bolaget.io API
to check for beer news and posts them to a Slack channel.

## Install

Install Go and follow the post-install instructions:

```sh
brew install go
```

Clone this repository:

```sh
git clone git@github.com:jnsstnbrg/beer-crawler.git $GOPATH/src/beer-crawler
```

Install the `dep` Go package management tool:

```sh
brew install dep
```

Install dependencies:

```sh
dep ensure
```

## Usage

To build the crawler run the following command:

```sh
GOOS=linux go build -o main
```

Create a zip file:

```
zip main main
```

Create a new Lambda on AWS and upload main.zip.

Add `SLACK_URL` environment variable with a Slack webhook URL.

## License

The MIT License (MIT)
