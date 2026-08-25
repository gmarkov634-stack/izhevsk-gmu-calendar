# Architecture boundary

`izhevsk-gmu-calendar` is a university-specific tenant/source repository.

Target flow:

`official IzhGMU source -> discover/download -> parser -> QA/review -> canonical Schedule Batch -> medical-calendar-core -> publication/storage -> student calendar`

## Belongs here

- official source adapters;
- parsers and canonicalization specific to IzhGMU;
- QA/review rules;
- source watcher and change detection;
- tenant-specific operational integrations.

## Does not belong here

- generic checkout/payment logic;
- subscription and trial services;
- generic public schedule HTTP runtime;
- cross-university shared commercial logic.

Those responsibilities belong to `gmarkov634-stack/medical-calendar-core`.

## Migration rule

Existing IzhGMU code must be copied/extracted from `kirov-gmu-calendar` in reviewable stages. Removing the old copy or changing production publication behavior is a separate step and requires explicit production authorization.

Faculty/program/group structure must be populated only from the official university site/server. The bootstrap manifest intentionally leaves `programs` empty until that verification is performed.
