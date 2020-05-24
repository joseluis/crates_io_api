# Changelog

## 0.6.0

* Upgrade the async client to Futures 0.3
* Removed `failure` dependency
* Add HTTP proxy support through the standard `http_proxy` environment variables ( compliments of reqwest 0.10 )
* Make the default user-agent `crates-io-api {version}`, i.e. `crates-io-api/0.6.0`

## 0.5.1 - 2019-08-23

* Fix faulty condition check in SyncClient::all_crates

## 0.5.0 - 2019/06/22

* Add 7 missing type fields for:
  * Crate {recent_downloads, exact_match}
  * CrateResponse {versions, keywords, categories}
  * Version {crate_size, published_by}
* Make field optional: User {kind} 
* Fix getting the reverse dependencies.
  * Rearrange the received data for simpler manipulation.
  * Add 3 new types:
    * ReverseDependenciesAsReceived {dependencies, versions, meta}
    * ReverseDependencies {dependencies, meta}
    * ReverseDependency {crate_version, dependency}

## 0.4.1 - 2019/03/09

* Fixed errors for version information due to the `id` field being removed from the API.  [PR #11](https://github.com/theduke/crates_io_api/pull/11)

## 0.4.0 - 2019/03/01

* Added `with_user_agent` method to client
* Switch to 2018 edition, requiring rustc 1.31+

## 0.3.0 - 2018/10/09

* Upgrade reqwest to 0.9
* Upgrade to tokio instead of tokio_core

## 0.2.0 - 2018/04/29

* Add AsyncClient
* Switch from error_chain to failure
* Remove unused time dependency and loosen dependency constraints

## 0.1.0 - 2018/02/10

* Add some newly introduced fields in the API
* Fix URL for the /summary endpoint
* Upgrade dependencies
* Add a simple test
