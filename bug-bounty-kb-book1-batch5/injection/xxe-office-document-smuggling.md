# XXE in Office Document Archives

- DOCX, PPTX, and XLSX are archive containers holding XML files that may be processed server-side.
- Unarchive a test document and locate the core XML file:
```text
DOCX: /word/document.xml
PPTX: /ppt/presentation.xml
XLSX: /xl/workbook.xml
```
- Insert a safe XXE test payload into the relevant XML file.
- Repack from inside the extracted directory using the syntax shown in the chapter:
```bash
cd example
zip -r new_example.docx *
```
- Upload the repacked document through the target's document-processing feature and observe parser behavior.
- False-positive trap: merely accepting the file does not prove the embedded XML is parsed server-side.
- Remediation: harden all document XML parsers and disable DTD/external entity expansion.
## Source: Bug Bounty Bootcamp, Ch. 15
