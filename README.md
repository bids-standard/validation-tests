# BIDS Validation Tests

This repository contains tests to help validators ensure coverage of the BIDS Standard,
as encoded in the schema.

The BIDS Schema defines a model where a context object is populated as the validator walks
the file tree. For a given context, each rule either passes, fails or does not apply.

## Test format

A test is an object with `rules`, `does` and `contexts` fields.
A test collection is a list of tests:

```yaml
- rules:
    - rules.X
    - rules.Y
  does: pass
  contexts:
    - sidecar:
        MetadataField1: Value1
        MetadataField2: Value2
      path: /path/to/file.ext
- rules: ...
  does: ...
  contexts: ...
```
