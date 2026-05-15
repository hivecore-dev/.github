<p align="center">
  <img src="assets/logo.svg" alt="Hivecore" width="240">
</p>

# Hivecore

**Hivecore** is an [OpenMBEE](https://openmbee.org) sub-project building
next-generation, open-source modeling tools for
[KerML and SysML v2](https://www.omg.org/spec/SysML/2.0/Beta2) — and for
any other metamodel you want to bring.

> *Metadata that feels like JSON.*

---

## What we're building

A modern, queryable, solver-aware model data platform — closer to working
with JSON and graphs than to traditional EMF-style MOF tooling.

```
            ┌──────────────────────────────────────┐
            │  Editors, Views, IDE plugins         │
            ├──────────────────────────────────────┤
            │  Hivecore Framework (HCF)       │
            │  KerML / SysML v2 semantics + API    │
            ├──────────────────────────────────────┤
            │  Hivecore Model Framework (HMF)      │
            │  Metamodel-agnostic MOF + runtime    │
            └──────────────────────────────────────┘
```

### Hivecore Model Framework (HMF)

A next-generation MOF combined with modern model data management. Any
metamodel can be built on top of it.

- **[`hmf`](https://github.com/hivecore-dev/hmf)** — schema layer
  (`MetaClass`, `MetaProperty`, `MetaAssociation`, `MetaConstraint`,
  semantic & ownership bindings) and runtime engine (`MDMEngine`, OCL +
  GQL query, Z3/SMT constraint solver, graph storage).
- **[`hmf-codegen`](https://github.com/hivecore-dev/hmf-codegen)** —
  code generation from metamodel definitions.

### Hivecore Framework (HCF)

KerML and SysML v2 semantics, libraries, and services built on HMF.

- **[`hcf-models`](https://github.com/hivecore-dev/hcf-models)** — KerML
  and SysML v2 metamodels expressed as HMF metamodels.
- **[`hcf-runtime`](https://github.com/hivecore-dev/hcf-runtime)** —
  semantics: implied relationships, name resolution, library loading,
  model validation.
- **[`hcf-server`](https://github.com/hivecore-dev/hcf-server)** — Ktor
  server exposing the SysML v2 API, parametric analysis, simulation, and
  query endpoints over Git-backed project stores.

### Editors and IDE integration

- **[`hcf-view-editor`](https://github.com/hivecore-dev/hcf-view-editor)** —
  view-based editing surface.
- **[`hcf-intellij`](https://github.com/hivecore-dev/hcf-intellij)** —
  IntelliJ plugin for KerML / SysML v2.

---

## Relationship to OpenMBEE

Hivecore is developed under the [OpenMBEE](https://openmbee.org) umbrella
and published under the `org.openmbee.hivecore` and `org.openmbee.hmf`
Maven coordinates. It complements existing OpenMBEE projects (MMS, View
Editor, Flexo) by providing the underlying model framework and KerML /
SysML v2 runtime.

---

## Getting involved

- Browse the repos above and open issues where they belong.
- Cross-cutting discussion: [`hmf`](https://github.com/hivecore-dev/hmf)
  for framework topics, [`hcf-runtime`](https://github.com/hivecore-dev/hcf-runtime)
  for KerML / SysML v2 semantics.
- Licensed under Apache-2.0.
