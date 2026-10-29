# FilterTube reuse assessment

Reviewed public source: [varshneydevansh/FilterTube](https://github.com/varshneydevansh/FilterTube),
commit [`2a983a3be9cbaca8d1fb2e318a7aa233e8dcd9cb`](https://github.com/varshneydevansh/FilterTube/tree/2a983a3be9cbaca8d1fb2e318a7aa233e8dcd9cb).

Review date: October 28, 2026. This is a static source assessment, not a build,
security audit, or validation of the native app.

## License and source availability

The public repository uses the MIT licence. Preserve its copyright and permission
notice in any substantial copied portions. Check dependencies and assets separately.
This licence does not provide video rights, trademark rights, or access to private
repositories.

The public release workflow explicitly places native Android/iOS shells and app
integration in a private `FilterTubeApp` repository. The public sync wrapper invokes
a tool in that private repository. Public runtime source and distributed APKs do
not constitute a complete open-source native app to fork.

## Candidate reuse

| Source | Assessment |
| --- | --- |
| `js/shared/identity.js` | Strong candidate: ID, handle, URL, and channel matching helpers. Extract and test the required subset. |
| `js/settings_shared.js` | Reuse selected normalization and keyword-compilation logic. Replace browser storage and UI dependencies. |
| `js/filter_logic.js` | Contains useful matching logic, but also page globals, renderer schemas, and page messaging. Extract a core rather than importing it wholesale. |
| `js/security_manager.js` | Useful reference for PIN verification and encrypted backups. Keep native profile authority and use appropriate platform storage. |
| `js/io_manager.js` | Import/export behaviour may be useful later; not needed for the first playback experiment. |
| `js/content_bridge.js`, `js/background.js` | Large, browser-specific integration surfaces. Reference material rather than the foundation of a new native shell. |
| `tests/runtime/` | Adapt relevant behavioural cases; test presence alone does not prove TV compatibility or filtering accuracy. |

## New work

- Native TV shell, remote focus and navigation, lifecycle, and playback integration.
- A catalogue and discovery ranking process that can introduce varied new sources.
- Content-pattern labels that distinguish promotion, consumption, and staged drama
  from ordinary play and storytelling.
- Explainable parent preferences and corrections built on those labels.
- An explicit policy for unknown classifications and weak evidence.
- Hardware acceptance checks and a representative filtering evaluation set.

FilterTube documents semantic/ML filtering as future or research work. Its existing
metadata filters do not establish the semantic categories proposed here. Its TV
plans are useful design input, not proof of a released Fire TV implementation.

## Reuse process

Before copying a component, record its upstream commit, source path, licence, local
modifications, and adapted tests. Keep unrelated extension features out of the
extracted core. No FilterTube implementation code is included in this repository
at this checkpoint.

Maintainer collaboration may be valuable. No maintainer has been contacted, and no
access, endorsement, or native-code permission has been requested or granted.

## Primary source references

- [Licence](https://github.com/varshneydevansh/FilterTube/blob/2a983a3be9cbaca8d1fb2e318a7aa233e8dcd9cb/LICENSE)
- [Runtime adapter plan](https://github.com/varshneydevansh/FilterTube/blob/2a983a3be9cbaca8d1fb2e318a7aa233e8dcd9cb/docs/filtertube_mobile_runtime_adapter_plan.md)
- [Native release and sync boundary](https://github.com/varshneydevansh/FilterTube/blob/2a983a3be9cbaca8d1fb2e318a7aa233e8dcd9cb/docs/APP_RELEASE_AND_RUNTIME_SYNC_WORKFLOW.md)
- [Mobile and TV architecture proposal](https://github.com/varshneydevansh/FilterTube/blob/2a983a3be9cbaca8d1fb2e318a7aa233e8dcd9cb/docs/filtertube_mobile_tv_architecture_plan.md)
