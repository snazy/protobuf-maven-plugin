[![GitHub license](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://raw.githubusercontent.com/projectnessie/protobuf-maven-plugin/master/LICENSE)
[![Build Status](https://github.com/snazy/protobuf-maven-plugin/actions/workflows/main.yml/badge.svg)](https://github.com/snazy/protobuf-maven-plugin/actions/workflows/main.yml)
[![Maven Central](https://img.shields.io/maven-central/v/org.caffinitas.protobuf-maven/protobuf-maven-plugin)](https://search.maven.org/artifact/org.caffinitas.protobuf-maven/protobuf-maven-plugin)

# NOTE! This is a fork!

_**This is a fork of [xolstice/protobuf-maven-plugin](https://github.com/xolstice/protobuf-maven-plugin/)**_
based on [this commit](https://github.com/xolstice/protobuf-maven-plugin/commit/fe8e6448dc6a5d58019b47a6fa7d348f8acd28e5)
from August 2020 (the latest release 0.6.1 was in Oct 2018) of the forked repo with the following additions:

* Use shared repository for protobuf binaries to prevent a sporadic build failure on Linux when
  executing the `protoc` binary. The shared repository is located at the project's top level
  directory under `.mvn/protobuf-binaries`.
  This is enabled by default, can be disabled by setting the new configuration option
  `useProtocBinaryRepository` to `false`.
* https://github.com/xolstice/protobuf-maven-plugin/issues/77

In addition to version 0.6.1:

* Fix file descriptor leak [commit](https://github.com/xolstice/protobuf-maven-plugin/commit/05ad59b08160fee6c20429ddc223f89e0093afe8)
* Support passing option to Java compiler [commit](https://github.com/xolstice/protobuf-maven-plugin/commit/3ae165e5f6b33f8a6221ece11cc79a7df5eeb8df)
* Respect attach flag for descriptor set goals [commit](https://github.com/xolstice/protobuf-maven-plugin/commit/68c82a45c2fd424bb002a8dbcebf2e78304580c1)
* Use pb insead of protobin for binary descriptors [commit](https://github.com/xolstice/protobuf-maven-plugin/commit/18461bf2554dc98139e95dc4828142b939f4b45a)

Plus quite a few dependency updates.

# Maven Protocol Buffers Plugin

[![Join the chat at https://gitter.im/xolstice/protobuf-maven-plugin](https://badges.gitter.im/xolstice/protobuf-maven-plugin.svg)](https://gitter.im/xolstice/protobuf-maven-plugin?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A plugin that integrates protocol buffers compiler (`protoc`) into Maven lifecycle.
This is a continuation of `maven-protoc-plugin` that was started at Google
and later developed by GitHub community.

[Release notes](https://www.xolstice.org/protobuf-maven-plugin/changes-report.html) and detailed documentation
are available on the [web site](https://www.xolstice.org/protobuf-maven-plugin/).

Please also read [Contribution Guidelines](docs/CONTRIBUTING.md) and [Code of Conduct](docs/CODE_OF_CONDUCT.md) for this project.
