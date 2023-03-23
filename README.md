# C++ REST SDK for RACE

This repo provides scripts to custom-build the
[C++ REST SDK library](https://github.com/microsoft/cpprestsdk) for RACE.

## License

The C++ REST SDK library is licensed under the MIT license.

Only the build scripts in this repo are licensed under Apache 2.0.

## Dependencies

C++ REST SDK has dependencies on the following custom-built libraries:

* Boost
* OpenSSL (for Android)

## How To Build

The [ext-builder](https://github.com/tst-race/ext-builder) image is used to
build C++ REST SDK.

```
git clone https://github.com/tst-race/ext-builder.git
git clone https://github.com/tst-race/ext-cpprest.git
./ext-builder/build.py \
    --target linux-x86_64 \
    ./ext-cpprest
```

## Platforms

C++ REST SDK is built for the following platforms:

* `linux-x86_64`
* `linux-arm64-v8a`
* `android-x86_64`
* `android-arm64-v8a`

## How It Is Used

C++ REST SDK is used by the exemplar bootstrap direct channel.
