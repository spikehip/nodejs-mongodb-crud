# Node.js-Express-MongoDB CRUD sample Application

[![wercker status](https://app.wercker.com/status/fab35822b24d218999e5a7a265b04ee0/m/master "wercker status")](https://app.wercker.com/project/byKey/fab35822b24d218999e5a7a265b04ee0)


This is a simple Node.js CRUD application using MongoDB.

It is based on
[https://github.com/ijason/NodeJS-Sample-App](https://github.com/ijason/NodeJS-Sample-App) and has the following features:

+ includes Wercker configuration
+ application changes to run on Oracle Container Cloud Service

### How to run

	npm install
	node app.js

### Configuration

MongoDB: `mongodb://mongodb`

Express: `app.listen(process.env.PORT || 3000);`

Wercker environment properties:

+ DOCKER\_USERNAME = username for Docker account
+ DOCKER\_PASSWORD = password for Docker account
+ DOCKER\_TAG = tag of the docker image
+ DOCKER\_REPOSITORY = name of the new repository (includes image name)

## History

### 1.0.0

- Initial version

## License

The Universal Permissive License (UPL), Version 1.0

### Notes

docker run --rm --name mongodb -d mongo
docker run -p 3000:3000 --rm --link mongodb:mongodb -d spikehip/nodejs-mongodb-crud
