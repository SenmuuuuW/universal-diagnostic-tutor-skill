# Cryptography Foundation Example

## User Question

"Why does modern cryptography need number theory?"

## Diagnosis

This is a cryptography foundations question. The learner is asking why abstract
math matters, not asking for an implementation recipe.

## Prerequisite Gap

The likely gap is modular arithmetic: clocks, remainders, primes, one-way
operations, and why some computations are easy in one direction but hard to
reverse.

## Source-Pack Behavior

Use `source_packs/crypto_security_addendum.md`. For learning, start with
Stanford CS255 or the applied cryptography book. Use NIST or RFCs only for
standard details, not beginner intuition.

## Teaching Depth Level

Level 4: foundation-first full explanation.

## Example Answer

Modern cryptography needs number theory because many cryptographic systems rely
on mathematical operations that are easy to do but hard to undo without secret
information. Modular arithmetic gives a clean way to build those operations.

Think of a clock. If it is 10 o'clock and you add 5 hours, you get 3 o'clock.
That wraparound behavior is modular arithmetic. Cryptography uses much larger
versions of this idea with primes, exponentiation, and finite groups.

The important idea is not "big numbers are secure." The important idea is that
some number-theory problems have structure: multiplying large primes is easy,
but factoring the product is hard; exponentiating modulo a prime can be easy,
but reversing it can be hard in the right setting. Cryptographic protocols turn
that asymmetry into encryption, signatures, and key exchange.

## Source List Behavior

- Stanford CS255 Cryptography: formal course path.
- Applied Cryptography Book: deeper public reference.
- NIST FIPS 197 AES: standard reference for symmetric encryption terminology.
- RFC 8446 TLS 1.3: advanced protocol reference after the basics.

## Common Mistakes

- Thinking cryptography is just "hiding text."
- Assuming larger numbers automatically mean stronger security.
- Jumping into TLS details before understanding keys, threats, and modular
  arithmetic.

## Why This Is Diagnosis-First And Resource-Augmented

The answer identifies the prerequisite gap, teaches the intuition first, then
routes sources by level and purpose.

## Answer-First Or Source-Dumping Mistake

A weak assistant would say "because RSA uses primes" and dump links to RFCs or
standards without teaching modular arithmetic or the easy-vs-hard idea.
