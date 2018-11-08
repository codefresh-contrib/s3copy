# Codefresh s3copy plugin

This is a plugin to simplify copying from codefresh pipeline to and from Amazon S3 buckets.

## Usage

Provide the necessary AWS access credentials as the pipeline env variables and set the source and destination paths relatively to the working directory (which is by default the root of the repository). Here is an example:


```yaml
---
version: '1.0'

steps:

  ...

  Copy to S3:
    image: 'codefresh/s3copy'
    environment:
      - SOURCE="path/to/somefile"
      - DESTINATION="s3://path-to-s3-bucket"
  ...

```

## Environment variables

```text
AWS_ACCESS_KEY_ID=<id>
AWS_SECRET_ACCESS_KEY=<key>
AWS_DEFAULT_REGION=<region>
SOURCE=<sourcepath>
DESTINATION=<destinationpath>

```
