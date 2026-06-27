# Networks From Zero Source Example

## User Question

"I want to learn computer networks from zero. What should I study first and
which sources should I trust?"

## Diagnosis

This is a beginner learning-path question. The learner does not need RFCs first;
they need a mental model of clients, servers, packets, layers, DNS, HTTP, TCP,
IP, routing, and reliability.

## Prerequisite Gap

The likely gap is confusing visible web behavior with the hidden network stack.
The learner needs the layers in order before protocol details.

## Source-Pack Behavior

Use `source_packs/networks_from_zero.md` first. Use MDN for beginner concepts,
an open textbook for structured study, Wireshark labs for observation, and
Stanford CS144 or RFCs only after foundations are ready.

## Teaching Depth Level

Level 4: foundation-first full explanation.

## Example Answer

Start with the idea that a network is not one magic pipe. It is a stack of
agreements. At the top, applications like browsers ask for resources. Below
that, HTTP describes requests and responses. DNS helps translate names into
addresses. TCP helps create reliable byte streams. IP moves packets between
networks. Routing decides the path.

For a first path, use MDN's Internet overview to get the picture. Then use MDN's
HTTP overview for client/server communication. After that, use Computer
Networking: Principles, Protocols and Practice for a structured course-like
path. When you want to see real packets, try Kurose/Ross Wireshark labs. Use
Stanford CS144 once you are ready for university-level networking. Use RFCs only
when you need exact protocol definitions.

## Source List Behavior

- MDN How The Internet Works: beginner mental model.
- MDN HTTP Overview: HTTP basics.
- Computer Networking: Principles, Protocols and Practice: structured study.
- Kurose/Ross Wireshark Labs: practical packet observation.
- Stanford CS144: advanced university course.

## Common Mistakes

- Starting with RFCs before understanding layers.
- Memorizing OSI layers without connecting them to HTTP, DNS, TCP, and IP.
- Treating packet capture as hacking instead of authorized local observation.

## Why This Is Diagnosis-First And Resource-Augmented

The answer diagnoses the learner as a beginner, chooses beginner sources first,
then escalates to formal and authoritative sources. The sources become a study
path, not a link dump.

## Answer-First Or Source-Dumping Mistake

A weak assistant would list RFCs, Stanford CS144, and random tutorials without
explaining what to learn first or why those sources match the learner's level.
