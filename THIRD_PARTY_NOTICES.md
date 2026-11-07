# Third-party components — Rawaq 0.6.0

Rawaq is an independent implementation. No Snaptube source, artwork, bundled binary
or endpoint credentials are shipped. Its original APK remains a separate analysis
input. Rawaq source is GPL-3.0; see LICENSE. Component notices remain separate.

## Source-built native runtime

All prior JNI payload members were removed from the selected wrappers. New local
Maven coordinates are `app.rawaq.sourcebuilt:library:0.18.1-source.1` and
`app.rawaq.sourcebuilt:ffmpeg:0.18.1-source.1`. Upstream 0.18.1 wrapper classes and
non-JNI resources remain byte-identical. Python, QuickJS, FFmpeg and their native
dependencies were built from pinned source for ARM64, ARMv7 and x86_64. The carrier
inventory contains 341 ELF instances including materialized aliases and outer
executables; this is not a count of independent libraries.

FFmpeg 7.1.1 uses `--enable-gpl --enable-version3`, nonfree disabled, fresh static
external dependencies and seven shared FFmpeg cores. A recorded source patch
enables authenticated HTTPS and client DNS/IP checks by default. CPython 3.12.11
targets API26; common libraries, QuickJS and FFmpeg target API24, compatible with
the app minimum26. Sources/default bytecode remain unchanged; only redundant
opt-1/opt-2 caches are excluded with a recorded transform.

| Native component | Retained full source input | Observed upstream terms |
|---|---|---|
| python | Python-3.12.11.tar.xz | PSF combined license; embedded third-party terms |
| pycryptodomex | pycryptodomex-3.23.0.tar.gz | BSD/public-domain and nested component terms |
| ffmpeg | ffmpeg-7.1.1.tar.xz | GPLv3 selected by --enable-gpl --enable-version3 |
| libmp3lame | libmp3lame-0-ddfe36cab873-lame-3.100.tar.gz | LGPL; inspect upstream LICENSE/COPYING |
| libopus | libopus-0-65c1d2f78b9f-opus-1.5.2.tar.gz | BSD-style and patent notices in COPYING |
| webp | libwebp-v1.6.0-tag.tar.gz | BSD-style plus patent grant |
| libdav1d | dav1d-1.5.1.tar.bz2 | BSD-style plus patent notice |
| openssl | openssl-0-c53a47e5e441-openssl-3.5.2.tar.gz | Apache-2.0 (3.5.2) |
| zlib | zlib-0-38ef96b8dfe5-zlib-1.3.1.tar.xz | zlib |
| libffi | libffi-0-138607dee268-libffi-3.4.7.tar.gz | MIT and build-tool terms |
| libbz2 | libbz2-0-47fd74b2ff83-bzip2-1.0.8.tar.xz | bzip2 |
| liblzma | liblzma-0-0b54f79df859-xz-5.8.1.tar.xz | Mixed per-file terms; liblzma primarily 0BSD/public domain |
| libsqlite | libsqlite-0-b7b4dc060f36-sqlite-src-3500400.zip | Public-domain dedication with build-tool terms |
| libxml2 | libxml2-2.14.6.tar.xz | MIT-style per Copyright |
| libiconv | libiconv-1.18.tar.gz | LGPL library and GPL build/tool portions |
| quickjs | quickjs-2025-04-26.tar.xz | MIT |
| mutagen | mutagen-1.47.0.tar.gz | GPL-2.0-or-later |

The source bundle `artifacts/rawaq-0.6.0-native-sources.zip` contains selected full
archives, modifications, executed recipes, notices and text producer proofs.
`licenses/source-built-carriers.json` identifies the selected AARs; the full package
receipt maps every inner file, alias transform and output hash. Build tools and
NDK compiler runtime notices are distinguished from Android system libraries.
CPython's combined terms include HACL, Expat and mpdecimal notices. Verbatim
component notices appear in the app's license list as `Native-*.txt`; they also
accompany private runtime ZIPs.

## Engine, networking and Android components

| Component | Pinned version | License / source |
|---|---|---|
| youtubedl-android library, common and FFmpeg wrapper | 0.18.1 | GPL-3.0; https://github.com/yausername/youtubedl-android |
| yt-dlp bundled by wrapper | 2025.11.12 | Unlicense, with separately licensed bundled components; https://github.com/yt-dlp/yt-dlp/tree/2025.11.12 |
| yt-dlp pinned offline upgrade shipped in this app | 2026.10.21 | Unlicense, with separately licensed bundled components; https://github.com/yt-dlp/yt-dlp/tree/2026.10.21; exact archive SHA-256 is checked by VerifiedEngineUpdater. |
| yt-dlp-ejs | 0.3.1 | Unlicense, with bundled Meriyah 6.1.4 (ISC) and Astring 1.9.0 (MIT); https://github.com/yt-dlp/ejs/tree/0.3.1 |
| Requests | 2.34.2 | Apache-2.0; unchanged pure-Python source, LICENSE and NOTICE retained; https://pypi.org/project/requests/2.34.2/ |
| urllib3 | 2.8.0 | MIT; unchanged pure-Python source and license retained; https://pypi.org/project/urllib3/2.8.0/ |
| IDNA | 3.20 | BSD-3-Clause; unchanged source and license retained; https://pypi.org/project/idna/3.20/ |
| charset-normalizer | 3.5.2 | MIT; pure-Python wheel without native extensions, original license retained; https://pypi.org/project/charset-normalizer/3.5.2/ |
| certifi | 2026.10.23 | MPL-2.0; unchanged Python source, Mozilla CA bundle and original notice retained; https://pypi.org/project/certifi/2026.10.23/ |
| AndroidX Core | 1.13.0 | Apache-2.0; https://android.googlesource.com/platform/frameworks/support/ |
| AndroidX Media3 | 1.11.1 | Apache-2.0; https://github.com/androidx/media |
| Kotlin, Guava and other transitive JVM libraries | exact resolved coordinates in licenses/dependency-sources.json | Matching source JARs and original embedded notices retained; JVM notices also packaged in the app. |

The pinned networking bundle retains unchanged sources, checked-hash bytecode and
Requests/urllib3/IDNA/charset-normalizer/certifi notices. Existing source-JAR records
remain evidence for unchanged JVM components. The old prebuilt native inventory is
historical and does not describe the new carrier selection.

Engineering provenance and runtime tests do not certify a legal conclusion or
Google Play approval. Provide the applicable source access method alongside public
binary distribution; sources prepared locally have not been published automatically.
The 0.5.9 producer limitations remain historical and are not retroactively closed
by building 0.6.0. Download-source rights and Play Console review remain separate.
