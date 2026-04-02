# XAD - Comprehensive Automatic Differentiation

**XAD** is the fastest automatic differentiation library for C++ and Python, built for production-scale systems. Proven in codebases of hundreds of thousands of lines, with 1,200+ tests and ~99% coverage.

## Ecosystem

| Repository | Description | Language |
|---|---|---|
| [xad](https://github.com/auto-differentiation/xad) | Core AD library - forward & adjoint mode, JIT support, Eigen integration | C++ |
| [xad-py](https://github.com/auto-differentiation/xad-py) | Python bindings for XAD | Python |
| [QuantLibAAD](https://github.com/auto-differentiation/QuantLibAAD) | Full QuantLib integration - compute all Greeks at once, up to 3 orders of magnitude faster than bump-and-reval | C++ |
| [QuantLib-Risks-Py](https://github.com/auto-differentiation/QuantLib-Risks-Py) | QuantLib risks from Python via XAD | Python |
| [xad-codegen](https://www.xcelerit.com/xad-enterprise-support) | High-performance native code generation backend for XAD - record-once/replay-many at maximum throughput (commercial) | C++ |

## Why XAD?

- Fastest AAD library for C++
- Production-proven in large-scale quantitative finance systems
- Full QuantLib integration with 3 orders of magnitude speedup over bump-and-reval
- Eigen compatible - drops into existing C++ codebases with minimal changes
- 1,200+ tests, ~99% coverage
- Python bindings available via `pip install xad`

## Get Started

[Documentation](https://auto-differentiation.github.io) 

---

If XAD is useful to you, please star the [core repository](https://github.com/auto-differentiation/xad) — it helps others find it.
