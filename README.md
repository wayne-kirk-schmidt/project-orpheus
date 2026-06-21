# Project Orpheus

**Recognition • Recovery • Recollection**

Project Orpheus is an open-source exploration into audio identity, 
archive recovery, acoustic fingerprinting, metadata repair, and musical memory.

## Mission

Given unknown or poorly tagged audio file(s):

1. Recognize what it is
2. Recover accurate metadata
3. Recollect it later through search, archive structure, and eventually melody-based matching

## Stage One Goal

Take a ZIP or audio folder, process the files, validate audio, generate fingerprints, 
attempt public metadata lookup, score confidence, and prepare a human review queue.

## Flow

```text
step1: locate ZIP / audio file
step2: ingest the source materials
step3: validate the source materials
step4: fingerprint the source materials
step5: lookup the target files
step6: score confidence on each of the files
step7: review and/or auto-register
step8: build recgonition tags and metadata
step9: archive the files and register the metadata
```
# Future Improvements

Planned improvements include:

- full directory tree visualization
- dag representation of tags
- dag representation of times, artists, and albums

## Design Principles

- **KISS** – Keep it Simple and Speedy
- **Deterministic** – the output is based on the same notebook


License
=======

Copyright 2026 

* Wayne Kirk Schmidt (wayne.kirk.schmidt@gmail.com)

Licensed under the Apache 2.0 License (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    license-name   Apache 2.0 
    license-url    https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Support
=======

Feel free to e-mail me with issues to: 

+   wayne.kirk.schmidt@gmail.com

I will provide "best effort" fixes and extend the scripts.

