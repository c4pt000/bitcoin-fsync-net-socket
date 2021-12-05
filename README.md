# Easier to send and receive 
https://github.com/c4pt000/qr-code-kiosk-cash-register

scripts on a website frontend using BTC should be updated to display mBTC by cast typing decimal output
```
:::install bitcoin.conf to datadir e.g /root/.bitcoin

bitcoind or bitcoin-qt

bitcoin-cli getinfo
bitcoin-cli getbalance
::: show command line actual physical amount in wallet
bitcoin-cli listtransactions | grep amount
```
# instead of 0.00077 BTC ---- 772 BTC $40 18 BTC -> $1 (in this example)
# (taking Bitcoin to $100,000 on the world market easier send and receive)
12-05-2021 (*REBUILDING*)
![s1](https://raw.githubusercontent.com/c4pt000/bitcoin/main/MILI_BTC.png)

# amount displayed in mBTC
![s1](https://raw.githubusercontent.com/c4pt000/bitcoin/main/easier-to-send-and-receive.png)

![s1](https://github.com/c4pt000/bitcoin/releases/download/s_fast/vokoscreen-2021-11-24_12-11-52.gif)

# changes live in net.cpp, net.h, net_processing.cpp net_processing.h ^^^^^ of src/

# on a 2gb prune instead of 3 days down to 15 hours or less

debian/fedora packages
https://github.com/c4pt000/bitcoin/releases/tag/pkg-fedora-34-debian10-boost-175

Bitcoin Core integration/staging tree
=====================================

https://bitcoincore.org

For an immediately usable, binary version of the Bitcoin Core software, see
https://bitcoincore.org/en/download/.

Further information about Bitcoin Core is available in the [doc folder](/doc).

What is Bitcoin?
----------------

Bitcoin is an experimental digital currency that enables instant payments to
anyone, anywhere in the world. Bitcoin uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Bitcoin Core is the name of open source
software which enables the use of this currency.

For more information read the original Bitcoin whitepaper.

License
-------

Bitcoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built (see `doc/build-*.md` for instructions) and tested, but it is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly from release branches to indicate new official, stable release versions of Bitcoin Core.

The https://github.com/bitcoin-core/gui repository is used exclusively for the
development of the GUI. Its master branch is identical in all monotree
repositories. Release branches and tags do not exist, so please do not fork
that repository unless it is for development reasons.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The CI (Continuous Integration) systems make sure that every pull request is built for Windows, Linux, and macOS,
and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://www.transifex.com/bitcoin/bitcoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.
