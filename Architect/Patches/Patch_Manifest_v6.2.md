# Patch Manifest v6.2 (Canon v4.1 | Architect v6.1 | Elite v5.4)

Order of operations:
1) QA_Integrity_v5.5.json
2) RepoHealth_v2.2.json
3) SourceLock_v6.2.json

After each patch:
- /qa_pre_game --focus "repo_integrity,lines_sync,contracts_map"
- /dynasty_savepoint --tag "Post_Patch_<Name>_<YYYY-MM-DD>"
- /verify_strategies

Notes:
- All patches are Canon-safe. No drift allowed.
- SourceLock v6.2 enforces checksum + timestamp validation on source_map files.