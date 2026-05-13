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
| [ad-benchmarks](https://github.com/auto-differentiation/ad-benchmarks) | Reproducible quant-finance benchmarks comparing XAD against CppAD, Adept 2, autodiff, and finite differences | C++ |

## Performance

XAD is the fastest open-source C++ AD library on four quant-finance workloads, benchmarked against [CppAD](https://github.com/coin-or/CppAD), [Adept 2](https://github.com/rjhogan/Adept-2), and [autodiff](https://github.com/autodiff/autodiff). The optional JIT backend ([xad-codegen](https://www.xcelerit.com/xad-enterprise-support)) delivers a further 2x-5x speedup.

<p align="center">
  <a href="https://github.com/auto-differentiation/ad-benchmarks">
    <img src="https://raw.githubusercontent.com/auto-differentiation/ad-benchmarks/main/results/chart.svg" alt="Benchmark chart comparing AD library performance" width="100%">
  </a>
</p>

<p align="center"><em>GCC 13.3, Intel Xeon Platinum 8488C, Ubuntu 24.04, <code>-O3 -mavx2 -mfma</code>, 10K MC paths. Full methodology and source: <a href="https://github.com/auto-differentiation/ad-benchmarks">ad-benchmarks</a>.</em></p>

## Why XAD?

- Fastest AAD library for C++ - [independently benchmarked](https://github.com/auto-differentiation/ad-benchmarks)
- Production-proven in large-scale quantitative finance systems
- Full QuantLib integration with 3 orders of magnitude speedup over bump-and-reval
- Eigen compatible - drops into existing C++ codebases with minimal changes
- 1,200+ tests, ~99% coverage
- Python bindings available via `pip install xad`

## Get Started

[Documentation](https://auto-differentiation.github.io) 

---

If XAD is useful to you, please star the [core repository](https://github.com/auto-differentiation/xad) — it helps others find it.
