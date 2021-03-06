crypto
======

[![Build Status](https://travis-ci.org/ReconfigureIO/crypto.svg?branch=master)](https://travis-ci.org/ReconfigureIO/crypto)
[![Documentation](https://godoc.org/github.com/ReconfigureIO/crypto?status.svg)](http://godoc.org/github.com/ReconfigureIO/crypto)

A library for cryptography algorithms designed for FGPAs.

Using in your kernels
---------------------

Reconfigure.io supports including vendor packages in your kernels. You can use your favorite Go dependency manager to add it to your kernel. We use [glide](https://github.com/Masterminds/glide) for our code.

```
$ glide create --non-interactive
[INFO]  Generating a YAML configuration file and guessing the dependencies
[INFO]  Attempting to import from other package managers (use --skip-import to skip)
[INFO]  Scanning code to look for dependencies
[INFO]  Writing configuration file (glide.yaml)
[INFO]  You can now edit the glide.yaml file. Consider:
[INFO]  --> Using versions and ranges. See https://glide.sh/docs/versions/
[INFO]  --> Adding additional metadata. See https://glide.sh/docs/glide.yaml/
[INFO]  --> Running the config-wizard command to improve the versions in your configuration
$ glide get github.com/ReconfigureIO/crypto
[INFO]  Preparing to install 1 package.
[INFO]  Attempting to get package github.com/ReconfigureIO/crypto
[INFO]  --> Gathering release information for github.com/ReconfigureIO/crypto
[INFO]  --> Adding github.com/ReconfigureIO/crypto to your configuration
[INFO]  Downloading dependencies. Please wait...
[INFO]  --> Fetching updates for github.com/ReconfigureIO/crypto
[INFO]  Resolving imports
[INFO]  Downloading dependencies. Please wait...
[INFO]  Exporting resolved dependencies...
[INFO]  --> Exporting github.com/ReconfigureIO/crypto
[INFO]  Replacing existing vendor dependencies
```

You should now see it in your `vendor` directory.

```
$ tree vendor
vendor
└── github.com
    └── ReconfigureIO
        └── crypto
            └── md5
                ├── host
                │   └── md5.go
                ├── md5.go
                └── md5_test.go

```

Contributing
------------

Pull requests & issues are enthusiastically accepted!

By participating in this project you agree to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
