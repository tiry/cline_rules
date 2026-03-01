
## Write Unit tests as part of the main development flow

Unit tests should be written at the same time of the code.
Every code improvement should be designed to be easily unit testable.

When the implenentation is completed, we need to ensure proper coverage, but we should not wait that step to write unit tests.

## Test data over mock

When possible, prefer using data files integrated in the tests folder : this is easier to maintain than complex mock objects

## Bug : create unit test to reproduce before fixing

Everytime I report a but or a problem, unless this is something trival like a typo or a missing import, we should:

 - reproduce the bug in a unit test
 - fix the code
 - verify that the test passes
