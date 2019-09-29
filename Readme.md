# CordApp Samples Re-use

Select, build and publish simple (easy to reason about) CorDapps, e.g. from corda/samples,
for testing Corda releases and snapshots.

Two approaches tried:
```
# publish to mavenLocal (requires changes to corda/samples)
cd obligation-cordapp && ./gradlew install

# use unmodifiead `corda/samples`
# clone github.com/corda/samples into lib/
#   and
# start an indepenent `gradlew jar` in lib/samples/obligation-cordapp/
gradle -q o2jars
```

The last one was checked with Gradle 4.10.3, 5.5.1, 5.6.2;
Caveat: Gradle 4.10.3 cannot make wrapper of 5.5.1; Gradle 5.6.2 can.
