# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

- `QUALCOMM` relocation 192 has been renamed to `R_RISCV_QC_ABS20_U` to reflect
  that this is not part of a HI/LO pair (there is no upper bits counterpart).
  Instead, this makes it clear that this is for materialising absolute addresses
  that are 20 bits. The relocation ID, type, field, and calculation have not
  changed, only the human-readable name.

## [v0.1]

- Initial Version of Qualcomm Extensions
