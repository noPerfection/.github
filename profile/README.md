# noPerfection

A protocol-based Go framework for writing self-managing
microservices. You write your app as an MVP, then scale it when necessary.
noPerfection is AI-friendly and helps refactor code into a concurrent
application.

# Top level modules

## [service](https://github.com/noPerfection/service) module

Primary framework entry point, make your app as a service, or use it to turn any package into a microservice.

## [showcase](https://github.com/noPerfection/showcase) module

Examples on how to use the framework

## Second layer
Second layers are additional modules that is used by `service` module.

### [protocol](https://github.com/noPerfection/protocol) module
Communication layer used by service.

- [protocol/client](https://github.com/noPerfection/protocol/client) module sends requests/submits messages to a service from a go package
- [protocol/handler](https://github.com/noPerfection/protocol/handler) module exposes
  command-based APIs and routes incoming messages to Go functions.
- [protocol/message](https://github.com/noPerfection/protocol/message) module defines
  the request and reply formats passed between clients and handlers.

### [context](https://github.com/noPerfection/context) module
Shared service configuration model that application uses. Since its a .json you can edit it to manage how framework manages its dependencies.

----

# Independent modules
These repositories are used by the framework, but they can also be used
independently in other Go applications.

## [datatype](https://github.com/noPerfection/datatype) module
Additional data types such as Queue, KeyValue. This module also provides helper functions for Go's built in data types.

## [log](https://github.com/noPerfection/log) module
Colorful, nested logging in your terminal

## [os](https://github.com/noPerfection/os) module
Operating-system helper packages:
    
- `path`             package to build or check file/directory paths
- `env`              package load environment variables or files
- `net`              package with the additional network functions such as checking port, or getting free port from OS
- `arg`              package for the app's argument parsing

