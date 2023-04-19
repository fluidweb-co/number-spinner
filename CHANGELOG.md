# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.3] - 2023-04-19

### Fixed

- Fix: Add decimal places to float quantity calculations to avoid precision errors. Decimal places defaults to `0`, and should be specified as an input attribute when decimals are expected.

## [1.0.2] - 2023-03-08

### Fixed

- Fix: Use `float` instead of `int` when converting min, max and step values.

## [1.0.1] - 2022-11-25

### Fixed

- Fix: Change `tabindex` for number spinner buttons so that is does not get the focus. Users should use the keyboard arrow keys on the number field to change the values.

## [1.0.0] - 2022-11-23

### Added

- Initial commit.
