# Networking Study Bank

50 original networking questions for self-study and CI-driven maintenance.

[日本語](README.ja.md)

The questions are written for this repository and reference public RFCs. They are not copied from certification exams or commercial study books.

## Topics

| Topic | Questions |
| --- | ---: |
| Internet layer and addressing | 10 |
| TCP and UDP | 10 |
| DNS | 10 |
| HTTP | 10 |
| TLS and application protocols | 10 |
| **Total** | **50** |

## Run StudyCI

No global install is required:

```bash
npx --yes studyci@0.2.0 check questions
```

Expected result on `main`:

```text
StudyCI checked 50 question(s) in 5 file(s).
Errors: 0 | Warnings: 0
```

## GitHub Actions

Pull requests and pushes to `main` run StudyCI automatically.

```yaml
- uses: yushi0405/studyci@v0.2.0
  with:
    path: questions
```

If a change introduces a duplicate ID or another deterministic finding, StudyCI reports it in the workflow and can attach an annotation to the affected file.

## Question format

```yaml
questions:
  - id: dns-001
    question: Which DNS resource record type maps a name to an IPv4 address?
    answer: A
    category: dns
    tags: [dns, records, ipv4]
    source: "RFC 1035 — Domain Names — Implementation and Specification: https://www.rfc-editor.org/rfc/rfc1035.html"
```

Each question should have:

- a unique `id`
- a short question with one clear answer
- a category
- useful tags
- a primary source

## Sources

The current question set uses public RFCs from the RFC Editor. See [SOURCES.md](SOURCES.md).

## Contributing

Corrections and new questions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT
