# Migration stages

1. Inventory the existing `izhgmu` adapter in `kirov-gmu-calendar`.
2. Copy source/discovery/parser/QA code into this repository without changing production routing.
3. Re-run structural and historical regression tests.
4. Move watcher/review/control-plane ownership after parity is proven.
5. Remove the old Kirov copy only in a separately reviewed step.

No schedule publish, withdraw, storage deletion or sales activation is part of repository bootstrap.
