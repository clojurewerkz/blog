---
layout: post
title: "Elastisch 2.1.0-beta5 is released"
date: 2014-08-27 04:13:25 +0400
comments: false
categories:
  - elastisch
  - releases
---

## TL;DR

Elastisch is a battle tested, small but feature rich and well
documented [Clojure client for ElasticSearch](http://clojureelasticsearch.info). It supports
virtually every Elastic Search feature and has [solid documentation](http://clojureelasticsearch.info).

[2.1.0-beta5](https://clojars.org/clojurewerkz/elastisch/versions/2.1.0-beta5) is a preview
release of Elastisch 2.1.


## Changes between Elastisch 2.1.0-beta4 and 2.1.0-beta5

### ElasticSearch Native Client Upgrade

Elastisch now depends on ElasticSearch native client version `1.3.x`.

### Single-Bucket Aggregation Fix in the Native Client

Child aggregations in single-bucket aggregations (i.e. "global") are no longer silently dropped.

Contributed by Yannick Scherer (StyleFruits).


## Full Change Log

[Elastisch change log](https://github.com/clojurewerkz/elastisch/blob/master/ChangeLog.md) is available on GitHub.


## Elastisch is a ClojureWerkz Project

[Elastisch](http://clojureelasticsearch.info) is part of the [group of libraries known as ClojureWerkz](http://clojurewerkz.org), together with

 * [Langohr](http://clojurerabbitmq.info), a Clojure client for RabbitMQ that embraces the AMQP 0.9.1 model
 * [Monger](http://clojuremongodb.info), a Clojure MongoDB client for a more civilized age
 * [Cassaforte](http://clojurecassandra.info), a Clojure Cassandra client
 * [Titanium](http://titanium.clojurewerkz.org), a Clojure graph library
 * [Neocons](http://clojureneo4j.info), a client for the Neo4J REST API
 * [Welle](http://clojureriak.info), a Riak client with batteries included
 * [Quartzite](http://clojurequartz.info), a powerful scheduling library

and several others. If you like Elastisch, you may also like [our other projects](http://clojurewerkz.org).

Let us know what you think [on Twitter](http://twitter.com/clojurewerkz) or on the [Clojure mailing list](https://groups.google.com/group/clojure).


## About the Author

[Michael](http://twitter.com/michaelklishin) on behalf of the [ClojureWerkz](http://clojurewerkz.org) Team
