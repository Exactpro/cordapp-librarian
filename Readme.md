# CordApp Samples Re-use

Select, build and publish simple (easy to reason about) CorDapps, e.g. from corda/samples,
for testing Corda releases and snapshots.

Two approaches tried: using
[flat dir resolver](https://docs.gradle.org/current/userguide/repository_types.html#sec:flat_dir_resolver),
and publishing to real repos (mavenLocal for the moment).
```
# use unmodified `corda/samples`
# clone github.com/corda/samples into lib/
#   and
# start an indepenent `gradlew jar` in lib/samples/obligation-cordapp/
gradle -q o2jars

# publish to mavenLocal (requires changes to corda/samples)
pushd obligation-cordapp && gradle clean install && popd
```

Both checked with Gradle 4.10.3, 5.4.1, 5.5.1, 5.6.2;
Caveat: Gradle 4.10.3 cannot make wrapper of 5.5.1; Gradle 5.6.2 can.
