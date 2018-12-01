# ClamAV Fuzz Corpus

This repository stores the seed corpora and fuzzing dictionaries for ClamAV.

This collection is a hodgepodge of samples we have either created or have borrowed from other projects.

## Seed Corpus

The corpus is a set of inputs for the fuzz target (stored as individual files). When starting the fuzzing process, one should have a "seed corpus", i.e. a set of inputs to "seed" the mutations. The quality of the seed corpus has a huge impact on fuzzing efficiency as it allows the fuzzer to discover new code paths more easily.

The ideal corpus is a minimal set of inputs that provides maximal code coverage.

https://github.com/google/oss-fuzz/blob/master/docs/ideal_integration.md#seed-corpus

## Dictionaries

For some input types, a simple dictionary of tokens used by the input language can have a dramatic positive effect on fuzzing efficiency. For example, when fuzzing an XML parser, a dictionary of XML tokens will help.
(https://github.com/google/oss-fuzz/blob/master/docs/ideal_integration.md#fuzzing-dictionary).
