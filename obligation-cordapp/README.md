# The Obligation CorDapp

This CorDapp comprises a demo of an IOU-like agreement that can be issued, transfered and settled confidentially. The CorDapp includes:

* An obligation state definition that records an amount of any currency payable from one party to another. The obligation state
* A contract that facilitates the verification of issuance, transfer (from one lender to another) and settlement of obligations
* Three sets of flows for issuing, transferring and settling obligations. They work with both confidential and non-confidential obligations

The CorDapp allows you to issue, transfer (from old lender to new lender) and settle (with cash) obligations.

# How to use that

Please see the [cordapp-harness](https://github.com/exactpro/cordapp-harness) project
and its [README](https://github.com/exactpro/cordapp-harness/blob/4ea6605/README.md).

TODO publish an example rpc-client.

# Publishing

```
./gradlew obligation-j:bintrayUpload obligation-k:bintrayUpload
```
