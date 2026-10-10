<p align="center">
  <img src="assets/camille.png" alt="Camille, the mascot of Liko" width="240">
</p>

<h1 align="center">kubernetes.liko</h1>

**This repository contains the Kubernetes module for the Liko data language. This module is officially maintained by the Liko team.**

It contains the complete set of Kubernetes schema definitions from the standard API—and only those. For CRDs, you will need to import them yourself or use a separate module, in keeping with the Liko philosophy (small modules, simple repos).

---

## Installation

Initialize a local module with `liko init`, then add `kubernetes.liko` as a dependency.

```bash
liko init
```
```bash
liko add kubernetes
```

```bash
liko install
```

## Usage

The module can now be used from any directory within the current module.

```liko
#Core: import "external/kubernetes/v1.37.0/api/core/v1"

serviceAccount: #Core.ServiceAccount & {
    metadata: {
        name: "my-sa"
        namespace: "my-ns"
    }
}
```
