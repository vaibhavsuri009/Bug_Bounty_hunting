# XXE in Office Document Uploads

- What it is: `.docx`, `.xlsx`, and `.pptx` are ZIP containers containing XML that a server may parse.
- Look for document-upload features processed by custom server-side tooling.
- Make a copy of a valid document and open the archive with a ZIP tool such as 7-Zip.
- Insert a harmless external-entity callback into an appropriate XML part.
- Repack the document and upload it through the normal workflow.
- A callback from the target demonstrates server-side XML parsing.
- False positive: Office files may be stored without being parsed.
- Edge case: document validators can reject malformed package relationships before XML parsing.
- Remediation: disable external entities in every XML parser used by document-processing pipelines.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 11
