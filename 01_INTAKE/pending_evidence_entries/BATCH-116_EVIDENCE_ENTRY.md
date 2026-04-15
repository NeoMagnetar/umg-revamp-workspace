# BATCH-116 — Evidence Entry

- **Batch ID:** BATCH-116
- **Title:** Google Drive file listing and connector boundary
- **Source Type:** Derived extraction / handoff note
- **Disposition:** ACCEPT_AS_EVIDENCE
- **Primary Domain:** Governance semantics versus connector capability
- **Key Signal:**
  - Explicit distinction between governance exclusion and connector/tool-surface limitation
  - User-mediated fallback workflows for producing deterministic inventories
  - Terminology pressure around enabled, authorized, attached, and enumerable states
- **Notable Candidate Language:**
  - Connector enabled does not imply folder enumeration permitted
  - Governance blocks tools only via explicit exclusion
- **Main Risk:**
  - Tool-surface limitations could be misread as governance behavior
- **Next Decision Target:**
  - Standardize artifact fallback for non-enumerable connectors
