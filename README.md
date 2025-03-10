# Project abac migration

Should be used before enabling `abacProject` feature flag to add abac rules with project permissions for default team.

## ENV variables
```
MONGO_URI (required) - mongo URI. Please don't forget to pass DB name or you can use same URI as for cf-api.
ACCOUNT_NAME (optional) - name of target account. Migration will be performed for all accounts if not passed.
```

## Examples

1. Run script with codefresh pipeline - see [codefresh-clone.yaml](./codefresh-clone.yaml)
2. Run docker image with codefresh pipeline - see [codefresh-image.yaml](./codefresh-image.yaml)
3. Run locally
```
yarn install
MONGO_URI={value} ACCOUNT_NAME={value} node index.js
```
4. Run docker image
```
docker run -it --rm -e MONGO_URI={value} --name codefresh-project-abac-migration quay.io/codefresh/project-abac-migration:latest
```

