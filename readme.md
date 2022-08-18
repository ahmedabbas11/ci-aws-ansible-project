# configure and deploy server code

## cf cloudfront

```
aws cloudformation deploy \
--template-file ./cf/cloudfront.yml \
--stack-name production-distro \
--parameter-overrides PipelineID="${S3_BUCKET_NAME}" \ # Name of the S3 bucket you created manually.
--tags project=udapeople &
```

aws cloudformation deploy \
--template-file ./cf/cloudfront.yml \
--stack-name production-distro \
--parameter-overrides PipelineID="udacity-ci" --tags project=udapeople