[![Build Status](https://travis-ci.org/amardeshbd/feedly-cloud-api-specification.svg)](https://travis-ci.org/amardeshbd/feedly-cloud-api-specification) [![https://img.shields.io/badge/OpenAPI--Spec-valid-green.svg](https://img.shields.io/badge/OpenAPI-valid-brightgreen.svg)](http://online.swagger.io/validator?url=https://raw.githubusercontent.com/amardeshbd/feedly-cloud-api-specification/master/feedly-api-specification.yaml)

# Unofficial Feedly Cloud API Specification

API spec for the feedly Cloud API using OpenAPI Specification (fka Swagger 2.0). Generates PHP, Java, Python, Go, Android, Objective-C and many more client SDK.

> **DISCLAIMER:** The API specification only includes **search** API to serve my need to searching RSS/Atom feeds. See official website for list of APIs supported.

 * **Official API Spec** can be found at [developer.feedly.com](http://developer.feedly.com/).

## Preview API Spec
You can preview the [spec](https://raw.githubusercontent.com/amardeshbd/feedly-cloud-api-specification/master/feedly-api-specification.yaml) file in **[ReDoc browser](http://rebilly.github.io/ReDoc/?url=https://raw.githubusercontent.com/amardeshbd/feedly-cloud-api-specification/master/feedly-api-specification.yaml)**


## Generating Client Library

Here is an example of generating `java` library using _Retrofit_ and _RxJava_

```
java -jar swagger-codegen-cli-2.2.1.jar generate \
	--input-spec feedly-api-specification.yaml \
	--lang java \
	--library retrofit2 \
	-DuseRxJava=true \
	--model-package com.feedly.cloud \
	--api-package com.feedly.cloud \
	--output feedly-api-client
```

> NOTE: Download the CLI binary jar file from [swagger-codegen](https://github.com/swagger-api/swagger-codegen).
