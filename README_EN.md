# gov-doc-writer

A Chinese official document (公文) writing skill for government and enterprise secretariat work. Covers the 15 statutory document types and follows **GB/T 9704-2012** (Format for Official Documents of Party and Government Organs) to produce a compliant header (版头), body (主体) and record section (版记).

## Features

- **15 statutory document types**: notice, report, request for instructions, reply, letter, minutes, circular, public notice, announcement, decision, resolution, opinion, order, proposal, communiqué
- **Automatic type detection** from natural-language requests; asks when ambiguous
- **Strict layout compliance**: A4, margins 37/35/28/26 mm, FangSong 16 pt body, SimHei level-1 headings, KaiTi level-2 headings, 22 lines × 28 chars per page, red separator header
- **Complete elements**: issuing-organ mark, document number (hexagonal brackets for the year), signatory (for upward documents), addressees, attachment note, signature, date, seal position, cc and printing record
- **Tone by direction**: deferential upward, decisive downward, courteous lateral; built-in official phrasing
- **No fabrication**: missing elements are marked `[待补充]` instead of being invented

## Quick start

1. Place this folder in your skills directory (or let the agent load `SKILL.md`).
2. Describe the task in plain Chinese, e.g.:

```
帮我写一份通知：关于开展2026年安全生产大检查的通知，主送各下属单位
```

```
写一个请示，向上级申请机房设备更新经费 50 万元
```

3. The skill collects required elements, generates an HTML document (white page, red header) and can export `.docx` / `.pdf` on request.

## Structure

```
gov-doc-writer/
├── SKILL.md
├── references/
│   ├── doc-types.md            # scenarios, format points and body templates per type
│   ├── format-spec.md          # full GB/T 9704-2012 spec + HTML/CSS conversion
│   └── official-phrases.md     # opening/transition/closing phrases, number rules
├── README.md
├── README_EN.md
├── LICENSE
└── .gitignore
```

## License

MIT License. See `LICENSE`.

## Disclaimer

This skill assists with document formatting and drafting patterns only; it is not legal, administrative or compliance advice. Facts, classification level and issuing procedure must be reviewed by the using organization under applicable regulations. Users are responsible for any consequences of adopting generated content.