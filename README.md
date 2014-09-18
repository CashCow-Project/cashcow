CashCow integration/staging tree
================================

http://www.proofofsteak.org/

Copyright (c) 2009-2014 Bitcoin Developers

Copyright (c) 2011-2014 Litecoin Developers

Copyright (c) 2014 Reddcoin Developers

Copyright (c) 2014 CashCow Developers


What is CashCow?
------------------

CashCow is a PoS-based cryptocurrency and is derived from the Reddcoin code base, which
is in turn derived from Litecoin and Bitcoin.  To initially reach a widespread
distribution, 1 billion coins were generated and a disbursed for free to reddit users.
This free distribution put minimum account age and activity criteria on eligible parties
to try to prevent individuals from claiming extraordinarily large shares of the initial
distribution.  

CashCow is intended to be a proof of concept of the definite stake reward idea.  For more
information about this idea, please see the 'Proof of Stake: Definite' white paper:

http://www.proofofsteak.org/resources/proof_of_stake_definite-whitepaper.pdf


CashCow Features
------------------

* 1 billion COW + ~5.25% inflation (virtually uncapped)
* Free initial coin distribution, 100% PoS
* 1st 'Proof of Stake: Definite' coin, branded playfully as "Proof of Steak: Delicious!"
* PoS:D! reward: 120 COW/block, or 52.56 million COW/year
* 72 second block spacing -- 20% smaller block chain


License
-------

CashCow is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.


Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the CashCow
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
appropriate channels.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/CashCow-Project/cashcow/tags) are created
regularly to indicate new official, stable release versions of CashCow.

Feature branches are created when there are major new features being
worked on by several people.

From time to time a pull request will become outdated. If this occurs, and
the pull is no longer automatically mergeable; a comment on the pull will
be used to issue a warning of closure. The pull will be closed 15 days
after the warning if action is not taken by the author. Pull requests closed
in this manner will have their corresponding issue labeled 'stagnant'.

Issues with no commits will be given a similar warning, and closed after
15 days from their last activity. Issues closed in this manner will be 
labeled 'stale'.


Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./cashcow-qt_test
