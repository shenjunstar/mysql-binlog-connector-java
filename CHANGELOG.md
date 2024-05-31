# Changelog
## [0.29.2](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.29.2...0.29.1) - 2024-04-22

- avoid SSL deadlocks using opt-in SO_LINGER with value of 0

## [0.29.1] - 2024-03-24

- bug fixes for VERY long transactions

## [0.29.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.29.0...0.28.3) - 2023-11-29

- add support for mysql8 specific metadata

## [0.28.3](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.28.3...0.28.1) - 2023-10-19

- around patch around pulling column signed-ness
- make mariadb_slave_compat field configurable

## [0.28.1](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.28.1...0.28.0) - 2023-07-07

- Fix a signedness bug, see #108

## [0.28.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.28.0...0.27.6) - 2023-02-14

- GTID performance improvements, thanks Janick Reynders

## [0.27.6](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.27.6...0.27.5) - 2023-01-19

- minor performance improvements
- fix isContainedWithin for mariadb events

## [0.27.5](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.27.5...0.27.4) - 2022-11-01

- add mariadb BINLOG_CHECKPOINT event 

## [0.27.4](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.27.4...0.27.3) - 2022-11-01

- move mariadb_slave_capability back to 4

## [0.27.3](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.27.3...0.27.2) - 2022-09-25

- pass use-annotate-rows through non-gtid mariadb connections

# Changelog
## [0.27.2](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.27.2...0.27.1) - 2022-09-16

- Fix the maria gtid detection regex to avoid erroneously detecting mysql gtids as maria

## [0.27.1](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.27.0...0.27.1) - 2022-08-28

- fix a bug around the capability that we send maria

## [0.27.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.26.1...0.27.0) - 2022-08-27

- Add "official" MariaDB support.  @wingerx started this worked and @ivapiv bugged me until it was
  done, thanks all.  This includes:
- MariaDB GTID support
- support for the ANNOTATE_ROWS_EVENTS
- MariaDB detection in getMariaDB()

## [0.26.1](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.26.0...0.26.1) - 2022-07-18

- fix deadlock with disconnect and keepalive thread.

## [0.26.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.6...0.26.0) - 2022-07-15

- Compressed binlogs, thank you Somesh Malviya
- fix crash on unknown field type

# Changelog

## [0.25.6](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.5...0.25.6) - 2022-04-14

- stop crashing in an inopportune place

## [0.25.5](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.4...0.25.5) - 2022-01-28

- mysql 8 also puts JSON keys in any damn place it likes

## [0.25.4](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.3...0.25.4) - 2021-10-13

- add debugging info to eof exception

## [0.25.3](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.2...0.25.3) - 2021-07-29

- support mysql 8's invisible columns

## [0.25.2](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.1...0.25.2) - 2021-06-25

- allow `setupConnection()` to be overridden
- upgrade to TLS v1.2

## [0.25.1](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.25.0...0.25.1) - 2021-04-20

- performance improves in ByteArrayInputStream#read

## [0.25.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.24.1...0.25.0) - 2021-03-04

- bring back jdk 8 support, this caused... ahem.  Issues.

## [0.24.1](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.24.0...0.24.1) - 2021-03-03

- Fix for performance issues read JSON columns

## [0.24.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.23.3...0.24.0) - 2021-02-04

- Move up to JDK 11, drop support for JDK 8

## [0.23.4](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.23.3...0.23.4) - 2021-01-17

- correct authentication error that was causing a problem with Azure

## [0.23.3](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.23.2...0.23.3) - 2020-10-29

- add EventDeserializer.CompatibilityMode.INTEGER_AS_BYTE_ARRAY if you want raw integer data
- don't crash on AWS Aurora's unknown event types

## [0.23.2](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.23.1...0.23.2) - 2020-07-25

- `connect` now throws `IllegalStateException` when already connected

## [0.23.1](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.22.2...0.23.1) - 2020-05-25

- this releases adds support for mysql 8's `caching_sha2_password` authentication method

## [0.22.2](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.22.0...0.22.2) - 2020-04-29

- Fix bugs in 0.22.0 involving nested JSON objects.

## [0.22.0](https://github.com/osheroff/mysql-binlog-connector-java/compare/0.20.1...0.22.0) - 2020-04-24

- *THIS RELEASE IS BUGGY.  DO NOT USE.*
- master server id is exposed in the library https://github.com/shyiko/mysql-binlog-connector-java/pull/319
- Fixes for JSON data in mysql 8.0.16+ https://github.com/shyiko/mysql-binlog-connector-java/pull/288
- more fixes for the bizarre azure platform https://github.com/shyiko/mysql-binlog-connector-java/pull/275

## [0.20.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.20.0...0.20.1) - 2019-05-12

### Added
- `mysql_native_password` auth support + SSL (Azure) ([#274](https://github.com/shyiko/mysql-binlog-connector-java/pull/274)).

## [0.20.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.19.1...0.20.0) - 2019-04-20

### Added
- `mysql_native_password` auth support (Azure) ([#272](https://github.com/shyiko/mysql-binlog-connector-java/issues/272)).

## [0.19.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.19.0...0.19.1) - 2019-03-28

### Fixed
- `TABLE_MAP` event data deserialization on MySQL 8 ([#264](https://github.com/shyiko/mysql-binlog-connector-java/issues/264)).

## [0.19.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.18.1...0.19.0) - 2019-02-13

### Added
- [MySQL 8.0.1+ table metadata](https://mysqlhighavailability.com/more-metadata-is-written-into-binary-log/) support ([#251](https://github.com/shyiko/mysql-binlog-connector-java/issues/251)).

### Fixed
- `connect`/`disconnect` keepalive thread race condition ([#260](https://github.com/shyiko/mysql-binlog-connector-java/issues/260)).

## [0.18.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.18.0...0.18.1) - 2019-02-04

### Fixed
- Checksum detection when custom FORMAT_DESCRIPTION deserializer is set ([#258](https://github.com/shyiko/mysql-binlog-connector-java/issues/258)).

## [0.18.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.17.0...0.18.0) - 2019-01-21

### Added
- `BinaryLogClient` flag (`useBinlogFilenamePositionInGtidMode`) to control initial (requested on `connect()`) binlog position when GtidSet is set ([#254](https://github.com/shyiko/mysql-binlog-connector-java/issues/254)).

### Fixed
- Checksum detection ([#256](https://github.com/shyiko/mysql-binlog-connector-java/issues/256)).

## [0.17.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.16.1...0.17.0) - 2019-01-07

### Added
- CRC32 checksum auto-detection (BinaryLogFileReader) ([#160](https://github.com/shyiko/mysql-binlog-connector-java/issues/160)).

### Changed
- GtidSet tracking (GtidSet update is delayed until XID/QUERY(COMMIT)/QUERY(ROLLBACK)) ([#250](https://github.com/shyiko/mysql-binlog-connector-java/issues/250)).

### Fixed
- (potential) deadlock when calling disconnect() inside onDisconnect() ([250](https://github.com/shyiko/mysql-binlog-connector-java/issues/230)).

## [0.16.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.16.0...0.16.1) - 2018-04-12

### Fixed
- `DATE_AND_TIME_AS_LONG_MICRO` handling regression ([introduced in 0.15.0](https://github.com/shyiko/mysql-binlog-connector-java/commit/2530a83283ac681ae9ab8a99acfa6aa6b4e9d288#r28556787)).

## [0.16.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.15.0...0.16.0) - 2018-04-12

### Added
- `EventDeserializer.CompatibilityMode.INVALID_DATE_AND_TIME_AS_MIN_VALUE` ([#210](https://github.com/shyiko/mysql-binlog-connector-java/issues/210)).

## [0.15.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.14.0...0.15.0) - 2018-04-07

### Added
- `EventDeserializer.CompatibilityMode.INVALID_DATE_AND_TIME_AS_NEGATIVE_ONE` ([#210](https://github.com/shyiko/mysql-binlog-connector-java/issues/210)).

## [0.14.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.13.0...0.14.0) - 2018-04-04

### Added
- `EventDeserializer.CompatibilityMode.INVALID_DATE_AND_TIME_AS_ZERO` ([#210](https://github.com/shyiko/mysql-binlog-connector-java/issues/210)).

## [0.13.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.12.2...0.13.0) - 2017-06-04

### Changed
- GtidSet to be more flexible when it comes down to UUIDSet|s manipulations ([171](https://github.com/shyiko/mysql-binlog-connector-java/issues/171)).

## [0.12.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.12.1...0.12.2) - 2017-05-18

### Fixed
- Deserialization of JSON objects that contain empty keys ([170](https://github.com/shyiko/mysql-binlog-connector-java/issues/170)).

## [0.12.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.12.0...0.12.1) - 2017-05-10

### Fixed
- List of event types (TRANSACTION_CONTEXT was missing) ([167](https://github.com/shyiko/mysql-binlog-connector-java/issues/167)).

## [0.12.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.11.0...0.12.0) - 2017-03-31

### Added
- PREVIOUS_GTIDS deserializer ([159](https://github.com/shyiko/mysql-binlog-connector-java/pull/159)).

## [0.11.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.10.1...0.11.0) - 2017-03-02

### Added
- `BinaryLogClient::gtidSetFallbackToPurged` ([156](https://github.com/shyiko/mysql-binlog-connector-java/issues/156)).

## [0.10.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.10.0...0.10.1) - 2017-02-28

### Fixed
- HEARTBEAT tracking ([118](https://github.com/shyiko/mysql-binlog-connector-java/issues/118#issuecomment-283138143)).

## [0.10.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.9.2...0.10.0) - 2017-02-28

### Added
- `BinaryLogClient::heartbeatInterval` ([118](https://github.com/shyiko/mysql-binlog-connector-java/issues/118)).
  NOTE: While it's 0 (disabled) by default it's RECOMMENDED that you turn it on (regardless whether you use built-in
  keepAlive mechanism or not).

### Changed
- `BinaryLogClient::connectTimeout` scope (connection will now be forcefully terminated if `LifecycleListener::onConnect`
isn't reached within `BinaryLogClient::connectTimeout` from `BinaryLogClient::connect`).

## [0.9.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.9.1...0.9.2) - 2017-02-25

### Fixed
- `BinaryLogClient` hangs while trying to connect ([154](https://github.com/shyiko/mysql-binlog-connector-java/issues/154)).

## [0.9.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.9.0...0.9.1) - 2017-02-21

### Fixed

 - NPE in case of EOF (BinaryLogClient) ([153](https://github.com/shyiko/mysql-binlog-connector-java/pull/153)).

## [0.9.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.8.1...0.9.0) - 2017-02-07

### Added

 - `BinaryLogClient::connectTimeout` (3 seconds by default).
   NOTE: `BinaryLogClient::keepAliveConnectTimeout` has been deprecated and is going to be removed in 1.0.0.

## [0.8.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.8.0...0.8.1) - 2016-01-10

### Fixed

 - `ArrayIndexOutOfBoundsException` while parsing JSON ([145](https://github.com/shyiko/mysql-binlog-connector-java/issues/145)).

## [0.8.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.7.4...0.8.0) - 2016-01-04

### Added

 - VIEW_CHANGE and XA_PREPARE `EventType`s.

## [0.7.4](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.7.3...0.7.4) - 2016-01-02

### Fixed

 - `SSLMode.PREFERRED` handling (verification against the CA is no longer enforced) ([#142](https://github.com/shyiko/mysql-binlog-connector-java/pull/142)).
 NOTE: This change does NOT affect `SSLMode.VERIFY_CA` / `SSLMode.VERIFY_IDENTITY`.

## [0.7.3](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.7.2...0.7.3) - 2016-12-26

### Fixed

 - Handling of DATE/DATETIME/TIMESTAMP "zero" value (e.g. '0000-00-00') when
 `CompatibilityMode.DATE_AND_TIME_AS_LONG_MICRO` is set (false by default).

## [0.7.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.7.1...0.7.2) - 2016-12-26

### Fixed

 - Inconsistent microseconds deserialization ([#138](https://github.com/shyiko/mysql-binlog-connector-java/pull/138)).

## [0.7.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.7.0...0.7.1) - 2016-12-25

### Fixed

 - TIMESTAMP fsp deserialization regression introduced in 0.7.0.

## [0.7.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.6.0...0.7.0) - 2016-12-24

### Added
 - TIME/DATETIME/TIMESTAMP microseconds precision support ([#136](https://github.com/shyiko/mysql-binlog-connector-java/issues/136)).

## [0.6.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.5.2...0.6.0) - 2016-11-27

### Added
 - `EventDeserializer` compatibility modes to mimic upcoming 1.0.0 event deserialization behavior ([#131](https://github.com/shyiko/mysql-binlog-connector-java/pull/131)).

## [0.5.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.5.1...0.5.2) - 2016-11-19

### Fixed
 - (JSON) deserialization of null/true/false/(u)int(16|32)/variable-length data types ([#129](https://github.com/shyiko/mysql-binlog-connector-java/issues/129)).

## [0.5.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.5.0...0.5.1) - 2016-10-18

### Fixed
 - ROWS_QUERY event deserialization ([#124](https://github.com/shyiko/mysql-binlog-connector-java/issues/124)).
 - JSON length determination.
 - GTID sync (`GtidSet` is now updated before `BinaryLogClient.EventListener`|s are notified).

## [0.5.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.4.2...0.5.0) - 2016-10-06

### Added
 - JSON support ([#119](https://github.com/shyiko/mysql-binlog-connector-java/pull/119)) (thanks to [@rhauch](https://github.com/rhauch)).

## [0.4.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.4.1...0.4.2) - 2016-09-20

### Fixed
 - A race condition that could result in duplicate events to be emitted on reconnect ([#113](https://github.com/shyiko/mysql-binlog-connector-java/issues/113)).

## [0.4.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.4.0...0.4.1) - 2016-08-31

### Fixed
 - GTID "rollover".
 - binlog position tracking (`binaryLogClient.binlogPosition` is no longer updated on TABLE_MAP so that in case of
 reconnect (using a different instance of client) table mapping (used by *RowsEventDataDeserializer|s) could be
 reconstructed before hitting *RowsEvent.

## [0.4.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.3.3...0.4.0) - 2016-08-15

### Added
 - TLS support ([#70](https://github.com/shyiko/mysql-binlog-connector-java/issues/70)).

## [0.3.3](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.3.2...0.3.3) - 2016-08-08

### Added
 - INTVAR deserializer.
 - Rudimentary support for GEOMETRY.

### Fixed
 - Handling of DATE/DATETIME/TIMESTAMP's "zero" value (e.g. '0000-00-00').

## [0.3.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.3.1...0.3.2) - 2016-07-19

### Fixed
- Fractional seconds deserialization on MySQL 5.6.4+ ([#103](https://github.com/shyiko/mysql-binlog-connector-java/issues/103)).

## [0.3.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.3.0...0.3.1) - 2016-01-15

### Fixed
- Broken "non blocking" mode backport from master.

## [0.3.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.2.4...0.3.0) - 2016-01-15

### Added
 - Support for "non blocking" mode (equivalent to running `mysqlbinlog` without --stop-never)

### Fixed
 - NPE if user attempts to read binary log 'within the logical event group' ([#60](https://github.com/shyiko/mysql-binlog-connector-java/issues/60)).

## [0.2.4](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.2.3...0.2.4) - 2015-09-09

### Fixed
 - Possible infinite loop in case of EOF in the middle of `ByteArrayInputStream::fill`.

## [0.2.3](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.2.2...0.2.3) - 2015-08-31

### Fixed
 - Handling of packets exceeding 16mb in size.

## [0.2.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.2.1...0.2.2) - 2015-07-10

### Fixed
 - TIMESTAMP_V2 deserialization ([#46](https://github.com/shyiko/mysql-binlog-connector-java/pull/46)).
 - Freeze during `BinaryLogClient.connect` in case of missing `REPLICATION CLIENT` permission ([#55](https://github.com/shyiko/mysql-binlog-connector-java/pull/55)).

## [0.2.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.2.0...0.2.1) - 2015-05-19

### Changed
- `SocketFactory.createSocket` method signature by adding `throws SocketException`.

### Fixed
- Initial handshake error reporting (so that actual message received from the server wouldn't be lost).
- Risk of `BinaryLogClient` getting stuck while in "pre-close" state.

## [0.2.0](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.1.3...0.2.0) - 2015-05-01
### Added
- Support for COM_BINLOG_DUMP_GTID (`BinaryLogClient`::[gtidSet](https://github.com/shyiko/mysql-binlog-connector-java/commit/3f30768791ef61ab0a83bd2bdb98af80bc799abd#diff-7addc4e3eed6e9254e088abc015ac8adR229)) ([#41](https://github.com/shyiko/mysql-binlog-connector-java/issues/41)).
- Support for authentication via empty password ([#39](https://github.com/shyiko/mysql-binlog-connector-java/issues/39)).

### Changed
- Server error reporting ([#37](https://github.com/shyiko/mysql-binlog-connector-java/issues/37)).
  WARNING: If you are using exception message to identify specific server errors - you'll need to switch to
  `ServerException`::[errorCode](https://github.com/shyiko/mysql-binlog-connector-java/commit/1817d0ff709c65c31af9236dcc4e50cc3ad1023b#diff-0dff747d57cb3f5f0548be89a81e29f8R37) (as message no longer includes error code).

### Fixed
- `EventHeaderV4Deserializer` eventLength handling ([#35](https://github.com/shyiko/mysql-binlog-connector-java/issues/35)).

## [0.1.3](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.1.2...0.1.3) - 2015-03-30
### Fixed
- Deserialization of `BitSet`s in little-endian ([#34](https://github.com/shyiko/mysql-binlog-connector-java/issues/34)).

## [0.1.2](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.1.1...0.1.2) - 2015-02-17
### Fixed
- TABLE_MAP/ROTATE `EventDataDeserializer`s handling ([#29](https://github.com/shyiko/mysql-binlog-connector-java/issues/29)).

## [0.1.1](https://github.com/shyiko/mysql-binlog-connector-java/compare/0.1.0...0.1.1) - 2014-12-08
### Fixed
- EXT_WRITE_ROWS event data deserialization when binlog_row_image is set to 'minimal' (default is 'full') ([#26](https://github.com/shyiko/mysql-binlog-connector-java/issues/26)).

## 0.1.0 - 2014-06-03
