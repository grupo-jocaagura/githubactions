# CHANGELOG Jocaagura Domain

This document follows the guidelines of [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.2] - 2025-09-14
- **CI/CD (GitHub Actions):**
  - `validate_commits_and_lints.yaml`: valida firmas de commits, formatea y analiza con Flutter, verifica `dependency_overrides` y usa caché de dependencias (excluye `develop`, `master` y `rev/**` en push).
  - `validate_pr.yaml` (PR → `develop`): exige actualización de `CHANGELOG.md`, ejecuta `format/analyze/test` y realiza *version bump* automático según etiquetas del PR (`major`, `minor`, `patch`) para PRs del mismo repo.
  - `validate_pr_master.yaml` (PR → `master`): ejecuta formato, análisis estricto, tests con cobertura, verifica ausencia de `dependency_overrides` y que la versión de `pubspec.yaml` sea mayor a la de `master`.

## [0.0.1] - 2025-09-14

### Added
- **CI/CD (GitHub Actions):**
    - `validate_commits_and_lints.yaml`: valida firmas de commits, formatea y analiza con Flutter, verifica `dependency_overrides` y usa caché de dependencias (excluye `develop`, `master` y `rev/**` en push).
    - `validate_pr.yaml` (PR → `develop`): exige actualización de `CHANGELOG.md`, ejecuta `format/analyze/test` y realiza *version bump* automático según etiquetas del PR (`major`, `minor`, `patch`) para PRs del mismo repo.
    - `validate_pr_master.yaml` (PR → `master`): ejecuta formato, análisis estricto, tests con cobertura, verifica ausencia de `dependency_overrides` y que la versión de `pubspec.yaml` sea mayor a la de `master`.
- **Dependencias:** se añade `jocaaguraarchetype: ^3.2.0` (actualización de `pubspec.lock` y *transitive deps* incluyendo `jocaagura_domain`).

### Changed
- **Repositorio:** configuración inicial y preparación del esqueleto del proyecto.
- **Código:** eliminación de comentarios de tema no utilizados (limpieza menor).

### Security
- **Commits firmados:** se habilitan verificaciones para asegurar integridad de autoría en la historia del repositorio.

> **Notas:** Esta es una versión de arranque para validar el pipeline y la configuración base. No introduce cambios funcionales hacia usuarios finales.
