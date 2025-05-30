---
title: kuma-dp
---

Dataplane manager for Envoy-based Service Mesh

### Synopsis

Dataplane manager for Envoy-based Service Mesh.

### Options

```
  -h, --help                         help for kuma-dp
      --log-level string             log level: one of off|info|debug (default "info")
      --log-max-age int              maximum number of days to retain old log files based on the timestamp encoded in their filename (default 30)
      --log-max-retained-files int   maximum number of the old log files to retain (default 1000)
      --log-max-size int             maximum size in megabytes of a log file before it gets rotated (default 100)
      --log-output-path string       path to the file that will be filled with logs. Example: if we set it to /tmp/kuma.log then after the file is rotated we will have /tmp/kuma-2021-06-07T09-15-18.265.log
```

### SEE ALSO

* [kuma-dp run](/docs/{{ page.release }}/generated/cmd/kuma-dp/kuma-dp_run)	 - Launch Dataplane (Envoy)
* [kuma-dp version](/docs/{{ page.release }}/generated/cmd/kuma-dp/kuma-dp_version)	 - Print version

