---
layout: post
title: "Monger 3.1.0 is released"
date: 2016-09-18 14:30:05 +0300
comments: false
categories:
  - monger
  - releases
---

## TL;DR

Monger is an idiomatic [Clojure MongoDB driver](http://clojuremongodb.info) for a more civilized age.
`3.1.0` is a maintenance release.


## Changes between 3.0.2 and 3.1.0

### MongoDB Java Driver Update

MongoDB Java driver dependency has been updated to `3.3.0`.

### Cursor Hinting Option Fix

Contributed by Stijn Opheide.

### Improved DBObject to Clojure Map conversion performance

New `from-db-object` implementation for `DBObject` avoids creation of an unnecessary
sequence and instead directly accesses `DBObject` instance in reduce. This should
offer performance improvement of about 20%. A performance test can be found
at [monger.test.stress-test](https://github.com/michaelklishin/monger/blob/master/test/monger/test/stress_test.clj).

Contributed by Juho Teperi.

### Authencation Function No Longer Ignores Credentials

In some cases Monger ignored provided credentials.

Contributed by Artem Chistyakov.

### Macro Type Hint Fixes

Contributed by Andre Ambrosio Boechat.


## Change Log

[Monger change log](https://github.com/michaelklishin/monger/blob/master/ChangeLog.md) is available on GitHub.



## Monger is a ClojureWerkz Project

[Monger](http://clojuremongodb.info) is part of the [group of libraries known as ClojureWerkz](http://clojurewerkz.org), together with

 * [Langohr](http://clojurerabbitmq.info), a Clojure client for RabbitMQ that embraces the AMQP 0.9.1 model
 * [Cassaforte](http://clojurecassandra.info), a Clojure Cassandra client built around CQL
 * [Elastisch](http://clojureelasticsearch.info), a minimalistic Clojure client for ElasticSearch
 * [Neocons](http://clojureneo4j.info), a client for the Neo4J REST API
 * [Quartzite](http://clojurequartz.info), a powerful scheduling library

and several others. If you like Monger, you may also like [our other projects](http://clojurewerkz.org).

Let us know what you think [on Twitter](http://twitter.com/clojurewerkz) or on the [Clojure mailing list](https://groups.google.com/group/clojure).


## About the Author

[@michaelklishin](http://twitter.com/michaelklishin) on behalf of the [ClojureWerkz](http://clojurewerkz.org) Team
