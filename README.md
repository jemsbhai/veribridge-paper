# veribridge

A bidirectional bridge between JSON-LD-Ex and CBOR-LD-Ex that preserves veracity annotations exactly across textual and binary encodings of the same semantic graph.

Semantic data on the Web moves between verbose textual representations and compact binary encodings as it crosses from cloud services to constrained edge and IoT devices. That translation is usually lossy for exactly the metadata that matters most downstream: provenance and veracity annotations attached to individual statements.

VeriBridge integrates JSON-LD-Ex and CBOR-LD-Ex, two extensions of JSON-LD and CBOR-LD that carry reasoning and veracity metadata, as a single semantic layer with two encodings of the same graph. Annotations are treated as first-class graph content rather than encoding-specific side data, so a statement annotated in JSON-LD-Ex arrives in CBOR-LD-Ex with its veracity record unchanged and can return without loss: annotation identity, scope, and values are preserved exactly, not approximated or dropped.

## Paper

"VeriBridge: Preserving Veracity Annotations Between JSON-LD-Ex and CBOR-LD-Ex"
Muntaser Syed, Sheikh Abujar, Marius Silaghi, Vincent Occhiogrosso, Katherine Burge, Michael Friedberg.
Submitted to The Web Conference 2027 (WWW '27), Short Papers track (OpenReview Submission 930). Full paper due November 16, 2026.

VeriBridge connects previously separate components for veracity-aware data exchange, semantic linked data, and compact linked data for constrained networks into one interoperable stack.

Implementation: [github.com/jemsbhai/veribridge](https://github.com/jemsbhai/veribridge) (monorepo for the PyPI, crates.io, and npm packages).

## Status

Paper in preparation. The evaluation measures round-trip fidelity, conversion overhead, and the size benefit of the binary encoding on annotated graphs representative of Web and IoT exchange.

## License

MIT
