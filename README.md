# Cryptoki Rust Wrapper, sgal Edit

An edited copy of the Rust [cryptoki crate](https://crates.io/crates/cryptoki). Based on the [cd497d6 commit](https://github.com/parallaxsecond/rust-cryptoki/commit/cd497d607bd98c56e58a91da9b160322f814431d).

Adds unit test-less support for `AES_GCM`, `GENERIC_SECRET_KEY_GEN`, `SHA HMAC`, `AES_KEY_WRAP_THALES`, `AES_KEY_WRAP_PAD_THALES` mechanisms. [Thales](https://cpl.thalesgroup.com/) has their own defined Key Wrap mechanism which is compatible with PKCS11 standard mechanism `AES_KEY_WRAP`. Its mechanism code is `0x80000170` with no parameters. The padded version compatible with PKCS11 standard mechanism `AES_KEY_WRAP_PAD` has code `0x80000171` with no parameters.

Branch name is knowingly mis-named after the (current) latest [cryptoki](https://crates.io/crates/cryptoki) version (v0.4.1) so I can somewhat leverage certain automated dependency vulnerability scanners in a strict manner while also using functionality from [parallaxsecond/rust-cryptoki PR #111](https://github.com/parallaxsecond/rust-cryptoki/pull/111). This is not ideal, so I eagerly await a new version 🍽️

<br>

# Cryptoki Rust Wrapper

The `cryptoki` crate provides an idiomatic interface to the PKCS #11 API.
The `cryptoki-sys` crate provides the direct FFI bindings.

# Community

Come and ask questions or talk with the Parsec Community in our Slack channel or biweekly meetings.
See the [Community](https://github.com/parallaxsecond/community) repository for more information on how to join.

# Contributing

Please check the [**Contribution
Guidelines**](https://parallaxsecond.github.io/parsec-book/contributing/index.html) to know more
about the contribution process.

# History

This repository is based on [this original PR on rust-pkcs11](https://github.com/mheese/rust-pkcs11/pull/43).
Read the PR discussion for more information.

# License

The software is provided under Apache-2.0. Contributions to this project are accepted under the same license.

*Copyright 2021 Contributors to the Parsec project.*
