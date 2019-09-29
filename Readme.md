# CordApp Samples Re-use

Select, build and publish simple (easy to reason about) CorDapps, e.g. from corda/samples,
for testing Corda releases and snapshots.

TODO: define Maven coordinates & provide instructions.

N.B. This is just a start of this work, this command works:
```
gradle -q o2jars
```
It clones github.com/corda/samples and starts an indepenent `gradlew jar` in obligations/

Checked with Gradle 4.10.3, 5.5.1, 5.6.2;
Caveat: Gradle 4.10.3 cannot make wrapper of 5.5.1; Gradle 5.6.2 can.
