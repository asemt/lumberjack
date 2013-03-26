# lumberjack

A Clojure library designed to help with your log lines.  Currently creates a log entry structure for Nginx logs, and allows for some basic visualization of time series data.

## Artifacts

Lumberjack artifacts are [released to Clojars](https://clojars.org/lumberjack). If you are using Maven, add the following repository
definition to your `pom.xml`:

``` xml
<repository>
  <id>clojars.org</id>
  <url>http://clojars.org/repo</url>
</repository>
```

### The Most Recent Release

With Leiningen:

    [lumberjack "0.1.0"]


With Maven:

    <dependency>
      <groupId>lumberjack</groupId>
      <artifactId>lumberjack</artifactId>
      <version>0.1.0</version>
    </dependency>

## Usage

To view a simple time series graph of the number of hits by the minute:

(view-time-series (nginx-logs ["test/lumberjack/nginx_sample.log"]) :by timestamp-minute :grouping-name "minute")

## License

Copyright © 2013 Steven Proctor

Distributed under the Eclipse Public License, the same as Clojure.
