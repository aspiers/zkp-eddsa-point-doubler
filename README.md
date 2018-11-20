Zero-knowledge proof for doubling of a point on an elliptic curve
=================================================================

This is the code from one of the projects started during the 
[two-day Zero Knowledge Proof developer workshop & hackathon](https://www.eventbrite.com/e/free-two-day-zero-knowledge-proof-developer-workshop-hackathon-tickets-52320521087)
run by [Work on Blockchain](https://workonblockchain.com/) in London,
17th-18th November.

Project goal
------------

The goal was to use [ZoKrates](https://zokrates.github.io/) to implement
a zero-knowledge proof of knowledge of a secret point `(x, y)` on a
[Twisted Edwards elliptic
curve](https://en.wikipedia.org/wiki/Twisted_Edwards_curve)
(specifically [the "baby Jubjub"
curve](https://github.com/barryWhiteHat/baby_jubjub_ecc)) which doubles
to a given known point `(x2, y2)` on that curve.  In this scenario, the
prover and verifier both know `(x2, y2)`, but the prover additionally
claims to know `(x, y)` which doubles to `(x2, y2)`, and the verifier
wishes to be able to verify this claim (as does the prover, assuming
honesty), whilst the prover wishes to provide the proof without
disclosing any information about `(x, y)` itself.

Motivation
----------

Generalising and maturing this implementation further within ZoKrates
could result in a library which could be useful in implementing more
complex cryptographically secure statements within this zero-knowledge
context.

Participants
------------

[@aspiers](https://github.com/aspiers) and
[@GuthL](https://github.com/GuthL).  Considerable help from
[@daira](https://github.com/daira) and
[@str4d](https://github.com/str4d) gratefully acknowledged.

See also
--------

During development, a bug in ZoKrates was discovered regarding
[associativity of subtraction of field values with function
calls](https://github.com/Zokrates/ZoKrates/issues/167).
