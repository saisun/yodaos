YodaOS
=============================

![https://img.shields.io/badge/base-linux-green.svg](https://img.shields.io/badge/base-linux-green.svg)
![https://img.shields.io/badge/build-openwrt-blue.svg](https://img.shields.io/badge/build-openwrt-blue.svg)

This is a modern operating system for next generation interactive device, and it embraces Web community,
uses JavaScript as the application language.

The project is a group of sub projects open sourced which are:

**Framework**

- [YodaRT][]: the JavaScript/Web layer for the OS, it provides the application development model.
- [ShadowNode][]: the [Node.js][] runtime that implements most of core APIs and N-API-compatible.

**Core**

- [yoda-flora][]: the IPC library for [YodaOS][]

**Service**

- [yoda-speech-service][]: the speech service that talks to [Rokid][] ASR/NLP cloud.
- [yoda-flora-dispatcher][]: the IPC centered service.

## Releases

This section describes how do [YodaOS][] release and its lifecycle.

#### versions

[YodaOS][] uses [Semver 2.0][] for versioning management, and we have lifecycles for `major` and `minor`.

- `major`: one release per 6 month, and all releases are stable.
- `minor`: one release per 1 month, and only the even ones are __stable__, namely `1.0.x`, `1.2.x`, `1.4.x`.

We assume the 3rd Thursday at every month as [YodaOS][] release date.

#### release requirements

Every release must contain the following parts:

- Repo manifest commit with specific version, for downloading the source code.
- Multiple platform images, includes:
  - Rokid Kamino18 soc.
  - AmLogic A113.
- Changelog describes what changes this updated.

#### stable and pre-versions

Stable version requires the complete tests on:

- Compatibility test suite
- Unit tests of modules and services
- Functional tests
- Integration tests

The above workload is in usual 2 weeks for the team, therefore we introduce pre-version, namely release
candidates(RC) to track the stable releasing progress.

For stable version, we preserve 2 weeks at least to take the workload of full tests, and create a pre-version 
branch `v1.2.x-rc`. Once all the full tests are passed, then create a stable branch(`v1.2.x`) from release
candidate branch(`v1.2.x-rc`).

## Community

- [YouTube](https://www.youtube.com/channel/UCRvBWIaBcsfvCTC_4EKW4lw)

#### Yoda Dev Day

Yoda Dev Day is the meetup we hold officially every 2 weeks, and it's publicly live or video available.
The agenda of [Yoda Dev Day](#yoda-dev-day) contains:

- Summary
- Topic presentation
- Free talks

## Contributing

[YodaOS][] is a community-driven project that we accepts any improved proposals, pull requests and issues.

- For JavaScript development, go [YodaRT][] for details.
- For proposal, [yoda-evolution][] is the place where someone can submit pull request to propose something.

## Documentation

- [Yoda Book](https://github.com/Rokid/yoda-book)
- [API reference](https://yodaos.rokid.com/docs/0.6/)

## License

Apeach 2.0

[YodaOS]: https://github.com/Rokid/YodaOS
[YodaRT]: https://github.com/Rokid/YodaRT
[yoda-flora]: https://github.com/Rokid/yoda-flora
[yoda-flora-dispatcher]: https://github.com/Rokid/yoda-flora-dispatcher
[yoda-speech-service]: https://github.com/Rokid/yoda-speech-service
[yoda-evolution]: https://github.com/Rokid/yoda-evolution
[Semver 2.0]: https://semver.org/
[ShadowNode]: https://github.com/Rokid/ShadowNode
[Rokid]: https://github.com/Rokid
[Node.js]: https://github.com/nodejs/node

