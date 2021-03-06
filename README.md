Log Cache CLI Plugin
====================
[![GoDoc][go-doc-badge]][go-doc] [![travis][travis-badge]][travis] [![slack.cloudfoundry.org][slack-badge]][loggregator-slack]

The Log Cache CLI Plugin is a [CF CLI](cf-cli) plugin for the [Log
Cache](log-cache) system.

### Installing Plugin

```
go get code.cloudfoundry.org/log-cache-cli
cf install-plugin $GOPATH/bin/log-cache-cli
```

### Usage

##### `log-cache`

```
$ cf tail --help
NAME:
   tail - Output logs for a source-id/app

USAGE:
   tail [options] <source-id/app>

OPTIONS:
   -envelope-type       Envelope type filter. Available filters: 'log', 'counter', 'gauge', 'timer', and 'event'.
   -follow, -f          Output appended to stdout as logs are egressed.
   -gauge-name          Gauge name filter (implies --envelope-type=gauge).
   -json                Output envelopes in JSON format.
   -lines, -n           Number of envelopes to return. Default is 10.
   -start-time          Start of query range in UNIX nanoseconds.
   -counter-name        Counter name filter (implies --envelope-type=counter).
   -end-time            End of query range in UNIX nanoseconds.
```

##### `log-cache-meta`

```
$ cf log-meta --help
NAME:
   log-meta - Show all available meta information

USAGE:
   log-meta
```

[log-cache]: https://code.cloudfoundry.org/log-cache-release
[cf-cli]: https://code.cloudfoundry.org/cli

[slack-badge]:              https://slack.cloudfoundry.org/badge.svg
[loggregator-slack]:        https://cloudfoundry.slack.com/archives/loggregator
[go-doc-badge]:             https://godoc.org/code.cloudfoundry.org/log-cache-cli?status.svg
[go-doc]:                   https://godoc.org/code.cloudfoundry.org/log-cache-cli
[travis-badge]:             https://travis-ci.org/cloudfoundry-incubator/log-cache-cli.svg?branch=master
[travis]:                   https://travis-ci.org/cloudfoundry-incubator/log-cache-cli?branch=master
