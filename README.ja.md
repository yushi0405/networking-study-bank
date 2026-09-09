# Networking Study Bank

ネットワーク基礎を扱う自作問題集です。現在は英語50問を収録しています。

[English](README.md)

問題文はこのリポジトリ用に作成し、公開RFCをsourceとして付けています。資格試験や市販問題集の問題文は転載していません。

## 分野

| 分野 | 問題数 |
| --- | ---: |
| Internet layer / addressing | 10 |
| TCP / UDP | 10 |
| DNS | 10 |
| HTTP | 10 |
| TLS / application protocols | 10 |
| **合計** | **50** |

## StudyCIでチェック

グローバルインストールは不要です。

```bash
npx --yes studyci@0.2.0 check questions
```

`main` では次の結果になる想定です。

```text
StudyCI checked 50 question(s) in 5 file(s).
Errors: 0 | Warnings: 0
```

## GitHub Actions

PRと`main`へのpushでStudyCIを実行します。

```yaml
- uses: yushi0405/studyci@v0.2.0
  with:
    path: questions
```

重複IDなどが入るとworkflowが失敗し、対象ファイルにGitHub annotationを表示できます。

## 問題形式

```yaml
questions:
  - id: dns-001
    question: Which DNS resource record type maps a name to an IPv4 address?
    answer: A
    category: dns
    tags: [dns, records, ipv4]
    source: "RFC 1035 — Domain Names — Implementation and Specification: https://www.rfc-editor.org/rfc/rfc1035.html"
```

各問題には、少なくとも次を付けます。

- 一意な`id`
- 答えが明確な短い問題文
- category
- tags
- 一次資料のsource

## 日本語版について

最初の公開版は英語50問です。日本語訳は別PRで追加できる構成にしています。英語版と日本語版を分けることで、翻訳作業そのものもStudyCIの実運用履歴として残せます。

## Sources

参照しているRFCは [SOURCES.md](SOURCES.md) にまとめています。

## Contributing

修正や問題追加は [CONTRIBUTING.md](CONTRIBUTING.md) を参照してください。

## License

MIT
