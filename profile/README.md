# XAD - Comprehensive Automatic Differentiation

**XAD** is the fastest automatic differentiation library for C++ and Python, built for production-scale systems. Proven in codebases of hundreds of thousands of lines, with 1,200+ tests and ~99% coverage.

## Ecosystem

| Repository | Description | Language |
|---|---|---|
| [xad](https://github.com/auto-differentiation/xad) | Core AD library - forward & adjoint mode, graph recording, Eigen integration | C++ |
| [xad-py](https://github.com/auto-differentiation/xad-py) | Python bindings for XAD | Python |
| [QuantLibAAD](https://github.com/auto-differentiation/QuantLibAAD) | Full QuantLib integration - compute all Greeks at once, up to 3 orders of magnitude faster than bump-and-reval | C++ |
| [QuantLibAAD-Py](https://github.com/auto-differentiation/QuantLibAAD-Py) | QuantLib risks from Python via XAD | Python |
| [xad-codegen](https://www.xcelerit.com/xad/#editions) | High-performance native code generation backend for XAD - record-once/replay-many at maximum throughput (commercial) | C++ |
| [ad-benchmarks](https://github.com/auto-differentiation/ad-benchmarks) | AD benchmarks on quant-finance workloads (LMM, Heston, CVA, SABR): XAD against CppAD, Adept 2 and autodiff, every gradient checked | C++ |

## Performance

XAD is the fastest open-source C++ AD library on four quant-finance workloads, benchmarked against [CppAD](https://github.com/coin-or/CppAD), [Adept 2](https://github.com/rjhogan/Adept-2), and [autodiff](https://github.com/autodiff/autodiff). XAD computes all sensitivities 6.5x to 83x faster than bump-and-reval, and the commercial code generation add-on ([xad-codegen](https://www.xcelerit.com/xad/#editions)) a further 4x to 17x faster than XAD alone.

<p align="center">
  <a href="https://github.com/auto-differentiation/ad-benchmarks">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/auto-differentiation/ad-benchmarks/main/results/amd/speedup-dark.svg">
      <img src="https://raw.githubusercontent.com/auto-differentiation/ad-benchmarks/main/results/amd/speedup-light.svg" alt="Speed-up over bump-and-reval per workload for XAD, XAD + codegen, Adept 2, CppAD and autodiff" width="600">
    </picture>
  </a>
</p>

<p align="center"><em>XAD v2.2.0, AMD EPYC (Zen 5), one core, GCC 15.2, run 10 November 2026. Full methodology and source: <a href="https://github.com/auto-differentiation/ad-benchmarks">ad-benchmarks</a>.</em></p>

### GradBench

With code generation, XAD is the fastest of the C and C++ AD tools on all 11 [GradBench](https://gradben.ch) problems, and on average 2.4x faster than the next-fastest tool.¹ On seven problems the generated code beats hand-written derivatives. Without code generation, open-source XAD is the fastest tape-based AD tool on 7 of the 11 and second on the other four. [Full results](https://www.xcelerit.com/xad/benchmarks/#bench-gradbench)

<sub>¹ Geometric mean of the 11 ratios to the fastest other AD tool, open-source XAD excluded. Measured by Xcelerit with GradBench's harness and tool images, 16 November 2026; not GradBench's nightly results.</sub>

## Why XAD?

- Fastest AAD library for C++ - [independently benchmarked](https://github.com/auto-differentiation/ad-benchmarks)
- Production-proven in large-scale quantitative finance systems
- Full QuantLib integration with 3 orders of magnitude speedup over bump-and-reval
- Eigen compatible - drops into existing C++ codebases with minimal changes
- 1,200+ tests, ~99% coverage
- Python bindings available via `pip install xad`

## Get Started

[Documentation](https://www.xcelerit.com/xad/docs/) 

---

If XAD is useful to you, please star the [core repository](https://github.com/auto-differentiation/xad) — it helps others find it.
