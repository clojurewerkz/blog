---
layout: post
title: "Meltdown 1.0.0-beta5 is released"
date: 2014-02-26 02:21:58 +0400
comments: false
categories:
  - meltdown
  - releases
---

## TL;DR

Meltdown is a Clojure interface to [Reactor](https://github.com/reactor), an asynchronous
programming, event passing and stream processing [toolkit for the JVM](http://spring.io/blog/2013/11/12/it-can-t-just-be-big-data-it-has-to-be-fast-data-reactor-1-0-goes-ga).

`1.0.0-beta5` is a development milestone release that updates
[Reactor](https://github.com/reactor/reactor) to `1.1.0.M1` and includes
a few bug fixes and minor API refinements.



## Changes between 1.0.0-beta4 and 1.0.0-beta5

### Environment Reuse

Previously Meltdown instantiated a new `Environment` per
`clojurewerkz.meltdown.reactor/create` invocation without
a provided environment. This lead to excessive thread creation
which could eventually exhaust system resources.

Meltdown `1.0.0-beta5` will reuse the same environment for
all created reactors unless its asked to use a specific
`Environment` instance.


### Environment Functions

`clojurewerkz.meltdown.env/environment` is a function that returns
a shared environment. To create a completely new environment from
scratch, use `clojurewerkz.meltdown.env/create`.

`clojurewerkz.meltdown.env/shutdown` shuts down environments and
all associated dispatchers.


### `clojurewerkz.meltdown.fn/->filter`

`clojurewerkz.meltdown.fn/->filter` is a new function that reifies
Reactor filters from Clojure functions.


## Changes between 1.0.0-beta3 and 1.0.0-beta4

### Moved Functions

`clojurewerkz.meltdown.streams/fn->function` and
`clojurewerkz.meltdown.streams/fn->predicate` are removed, use
`clojurewerkz.meltdown.fn/->function` and
`clojurewerkz.meltdown.fn/->predicate` instead.

### Streams Flushing

Stream operations are now lazier in Reactor. To enforce stream
sources to be drained, use `clojurewerkz.meltdown.streams/flush`
which accepts a stream or deferred.

### Reactor Update

Reactor is updated to `1.1.0.M1` which has multiple breaking API
changes.



## Change log

[Meltodwn change log](https://github.com/clojurewerkz/meltdown/blob/master/ChangeLog.md) is available on GitHub.


## Meltdown is a ClojureWerkz Project

[Meltdown](https://github.com/clojurewerkz/meltdown) is part of the [group of libraries known as ClojureWerkz](http://clojurewerkz.org), together with

 * [Langohr](http://clojurerabbitmq.info), a Clojure client for RabbitMQ that embraces the AMQP 0.9.1 model
 * [Elastisch](http://clojureelasticsearch.info), a Clojure client for ElasticSearch
 * [Monger](http://clojuremongodb.info), a Clojure MongoDB client for a more civilized age
 * [Cassaforte](http://clojurecassandra.info), a Clojure Cassandra client
 * [Titanium](http://titanium.clojurewerkz.org), a Clojure graph library
 * [Neocons](http://clojureneo4j.info), a client for the Neo4J REST API
 * [Quartzite](http://clojurequartz.info), a powerful scheduling library

and several others. If you like Meltdown, you may also like [our other projects](http://clojurewerkz.org).

Let us know what you think [on Twitter](http://twitter.com/clojurewerkz) or on the [Clojure mailing list](https://groups.google.com/group/clojure).


## About the Author

[Michael](http://twitter.com/michaelklishin) on behalf of the [ClojureWerkz](http://clojurewerkz.org) Team
