# Overview for Compiler (Conjure 4.16.1)

This distribution was manually generated from 4.16.1. from original palantir repository.
The bintray binaries are no longer publically available.

## How to use it:

Please refer to the documentation available [here](https://github.com/palantir/conjure/blob/master/docs/howto/invoke_clis_manually.md#how-to-invoke-conjure-clis-manually)

An invocation from this binary will convert any .yaml specification into the intermediate IR (.json) format.
The intermediary format can later be consumed by a language specific generator in order to auto-generate code.

## Usage sample
./conjure-4.16.1/bin/conjure compile input-yaml/input.yml output-json/output.json

# Overview for Java Generator (Conjure Generator 6.1.0)

This distribution was manually generated from tag 6.1.0 from original Palantir repository.
The bintray binaries are not longer publically available.

In order to generate, due to a deprecation on Gradle 7.0.0, the following command was required:

```
./gradlew assemble --warning-mode all
```

## How to use it

The invocation will use the intermediary format IR (the json file) and create the generated code using the specified library.
More information on what library implementations are avaiable can be found [here](https://github.com/palantir/conjure-java/tree/e1991a0a09d106ad9d5bbd13e3f010e9674d8c9a)

## Example usage:

To generate a Jersey Client/Server, use the following command line call:

```
./conjure-java-6.1.0/bin/conjure-java generate --rawSource input-json/input.json output-java-jersey --jersey
```

Bear in mind that this requires the previous creation of the output directory (output-java-jersey)
