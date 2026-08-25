# izhevsk-gmu-calendar

Tenant repository for the **Ижевский государственный медицинский университет (Ижевский ГМУ)** schedule project.

## Responsibility

This repository owns university-specific schedule integration only:

- official source discovery and download;
- parsing and normalization;
- QA and review policy;
- source/watch logic;
- tenant-specific operational integrations.

Generic customer runtime, commerce, subscriptions, trials and public schedule API belong to `gmarkov634-stack/medical-calendar-core`.

## Current migration state

The existing IzhGMU adapter is still running from `gmarkov634-stack/kirov-gmu-calendar`. Migration into this repository must be staged and must not change production publication state until separately authorized.

Official schedule source currently used by the existing adapter:
`https://www.igma.ru/component/content/article/647-raspisanie?Itemid=108&catid=132`

Tenant id: `izhgmu`.
