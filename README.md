# Omega-super-public-chain-OMG-code
Omega super public chain (OMG) code
System information
Geth version: Geth/v1.9.14-stable-6d74d1e5/linux-amd64/go1.14.2
OS & Version: Linux

Expected behaviour
Transaction is broadcasted to the network and confirms

Actual behaviour
I get a tx hash in return, the tx is also added to the eth.pendingTransactions list, but never shows up in any ETH explorers and never confirms.

Steps to reproduce the behaviour
Try sending a transaction using personal.sendTransaction()

This is the output from eth.pendingTransactions if it helps:

}, {
    blockHash: null,
    blockNumber: null,
    from: "0x66ec231d3d50fd2c5a9a5242c76d91ca39a79c35",
    gas: 21000,
    gasPrice: 18010524411,
    hash: "0x9367ca24e37184f328a5b9edd67a776f98f2195803a6237d452de2e8f4fb2083",
    input: "0x",
    nonce: 5,
    r: "0x7f0e5d712072782ecb5ac39072044229d6283166a182749b0e50adce1224601f",
    s: "0x63c276600b15e7db1543fcb115c30cf94ee0948bbf7ead1200925602428ec54f",
    to: "0x4408f69a5a7ef19c5cf61309a046e735e2e38ea3",
    transactionIndex: null,
    v: "0x25",
    value: 1000000000000000
}]
Help would be really appreciated!

Update:
I've now tried this on both a light client and a fast sync. Both return a valid tx hash but it doesn't look like it's been broadcasted.

Update 2:
This issue occurs on both v1.9.9 and v1.9.14.
