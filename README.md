# Rawaq release sources

Developer/publisher: **hamzah naji**  
Support: **hamzahnaji61@gmail.com**

This public repository distributes reviewed **release source archives**. The development repository and its future history remain private. Publication of these release sources was expressly authorized by the publisher on 7 November 2026.

## Rawaq 0.6.1 / Android versionCode 16

The release delivery has **three archives that must be used together**:

| Archive | SHA256 |
|---|---|
| `rawaq-0.6.1-source.zip` | `7ff840932c82856309bdcecebbd3e95e148793de89024e328c2eaf29149339dc` |
| `rawaq-0.6.0-managed-sources.zip` | `e01b9946f37a07f1eb100baeef26605b0e9f46fc0573b2c7831e9075d27fb58f` |
| `rawaq-0.6.0-native-sources.zip` | `7885721c895e50e98567125136526105e915afa7e368ac9ea0902c6220f3a548` |

The native and managed dependencies are unchanged from the reviewed 0.6.0 build and retain their original filenames. Use the matching member manifests and `rawaq-0.6.1-source-offer.json` to verify the complete delivery. The project archive contains application/configuration/test source, current build recipes and notices. The other archives contain corresponding dependency sources and executed native recipes.

[Release downloads](https://github.com/hamzahgithub/rawaq-sources/releases/tag/v0.6.1) are available after the release is published. GitHub automatic Source code ZIP/tar downloads contain this index only; they are **not substitutes for the three attached archives**.

## Build and licensing

Extract the project and managed archives together, merging their `Rawaq/` roots. Extract the native archive beside them under `Rawaq-native-0.6.0/`. Read `Rawaq/docs/source-delivery-0.6.1.md` and `Rawaq/docs/source-delivery-0.6.0.md` for exact build requirements, source mapping and the ordered native build. Use your own signing key; private signing material and account sessions are excluded.

Rawaq application source is distributed under GPLv3, with components retaining their own licenses. Consult `LICENSE`, `THIRD_PARTY_NOTICES.md`, component sources and native build review boundaries. Some frozen archive documents describe the earlier private planning state; this public release was authorized **after** that snapshot. The code/archive bytes and hashes have not been changed to rewrite history.

This publication does not certify all component obligations, grant rights to third-party media, or constitute Google Play approval. The app must be used where content rights and source terms permit downloading.

[English privacy policy](https://hamzahgithub.github.io/rawaq-privacy/).
