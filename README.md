# wait - Docker mod for any container

This mod adds [wait](https://github.com/ufoscout/docker-compose-wait) to any container, to be installed/updated during container start.

In any container docker arguments, set an environment variable `DOCKER_MODS=mzramna/mods:universal-wait`

If adding multiple mods, enter them in an array separated by `|`, such as `DOCKER_MODS=linuxserver/mods:universal-wait|linuxserver/mods:universal-mod2`

Additional configuration options
The behaviour of the wait utility can be configured with the following environment variables:
WAIT_VERSION: the version that will be installed of the wait
WAIT_LOGGER_LEVEL : the output logger level. Valid values are: debug, info, error, off. the default is debug.
WAIT_HOSTS: comma-separated list of pairs host:port for which you want to wait.
WAIT_PATHS: comma-separated list of paths (i.e. files or directories) on the local filesystem for which you want to wait until they exist.
WAIT_TIMEOUT: max number of seconds to wait for all the hosts/paths to be available before failure. The default is 30 seconds.
WAIT_HOST_CONNECT_TIMEOUT: The timeout of a single TCP connection to a remote host before attempting a new connection. The default is 5 seconds.
WAIT_BEFORE: number of seconds to wait (sleep) before start checking for the hosts/paths availability
WAIT_AFTER: number of seconds to wait (sleep) once all the hosts/paths are available
WAIT_SLEEP_INTERVAL: number of seconds to sleep between retries. The default is 1 second.
