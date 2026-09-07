# Release preparation

2026-09-06: Prepared a portable setup recipe from accepted framework `0fc2b04150360cfeaa8094620e5ad89a1c2ee01a`.
The release snapshot keeps functional code and title seed bytes, adds the bounded setup backport, and excludes private input/history.
Consulted the local release process, PSX-PUB-016, the accepted title handoff, and [Git orphan-branch documentation](https://git-scm.com/docs/git-checkout).
The shared archive gate now accepts only exact hashes for two intentional SDK path-example files; changed and relocated fixtures still fail.
Native CI and Windows package acceptance are pending.

2026-09-07: Native canary gates required the existing PSX-BUILD-024 C-linkage correction and the exact public recomp-ui be8ac1d portable tool text fix. The package now carries all four complete public dependency identities (PSX-PUB-027). No game runtime behavior or recipe settings changed in this update. Native build and package checks remain required.

2026-09-07: Native canaries found the accepted GL coherence fixture was not registered with CTest. Added its exact Windows GCC/SDL3 build and scale1/4 tests; both pass through the actual runtime CMake project. Other toolchains report an explicit unsupported-test skip. No accepted renderer or recipe code changed. Fresh canary follows.
