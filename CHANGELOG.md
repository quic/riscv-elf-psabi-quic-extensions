# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

- The "Extended to Compressed Address Relaxation" is now called "Extended to
  Compressed LUI Relaxation", and it now replaces the instruction with a `C.LUI`
  instruction rather than `C.LI` instruction. This should mean the relaxation
  applies more often, as relatively fewer symbols are expected to fit their
  address in a `C.LI` than a `C.LUI`.

## [v0.2]

- `QUALCOMM` relocation 192 has been renamed to `R_RISCV_QC_ABS20_U` to reflect
  that this is not part of a HI/LO pair (there is no upper bits counterpart).
  Instead, this makes it clear that this is for materialising absolute addresses
  that are 20 bits. The relocation ID, type, field, and calculation have not
  changed, only the human-readable name.

- Some relaxations now have restrictions that they only apply to adjacent
  instructions.

- More clarifying notes and examples have been added, including an appendix
  explaining the choices that have guided this ABI design.

- `QUALCOMM` Relocation 195 has been renamed from `R_RISCV_QC_E_JUMP_PLT` to
  `R_RISCV_QC_E_CALL_PLT` to more clearly show it is used for calls, which can
  clobber temporary registers.

## [v0.1]

- Initial Version of Qualcomm Extensions
