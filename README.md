# spicedb-poc
Contains spicedb instance and mysql datastore implementation. Implements a test schema for users, groups, policies, resources.

## Install instruction

Run docker containers
```
docker-compose --env-file .env up -d
```

Install Zed CLI | [Link](https://github.com/authzed/zed)
```
brew install authzed/tap/zed
```

Set zed cli conext
```
zed context set dev :50051 "secrettoken" --insecure
```

Import schema
```
# from root dir
zed import schema.yaml
```

## Authzed SpiceDB Playground
You can edit the schema yaml in a playground env found [here](https://play.authzed.com/schema). You can import and export the schema.yaml file.