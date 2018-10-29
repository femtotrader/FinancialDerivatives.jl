# FinancialDerivatives.jl

[![Build Status](https://travis-ci.org/JuliaQuant/FinancialDerivatives.jl.svg?branch=master)](https://travis-ci.org/JuliaQuant/FinancialDerivatives.jl)

[![](https://img.shields.io/badge/docs-stable-blue.svg)](https://juliaquant.github.io/FinancialDerivatives.jl/stable) or [![](https://img.shields.io/badge/docs-dev-blue.svg)](https://juliaquant.github.io/FinancialDerivatives.jl/dev/)

Financial derivatives modeling and pricing in Julia.

## Derivatives

* `AmericanOption`
* `AsianOption`
* `EuropeanOption`
* `FXOption`
* `InterestRateDerivative`

## Models

* `BlackKarasinski`
* `BlackScholes`
* `BrennanSchwartz`
* `CoxIngersollRoss`
* `CoxRossRubinstein`
* `GarmanKohlhagen`
* `JarrowRudd`
* `LeisenReimer`
* `LongstaffSchwartz`
* `RendlemenBartter`
* `Tian`
* `Vasicek`

## Installation

```julia
(v1.0) pkg> add https://github.com/JuliaQuant/FinancialDerivatives.jl
```

## Usage

```julia
julia> using FinancialDerivatives

julia> american_put = AmericanOption(100.0, 90.0, 0.05, 0.3, 180/365, -1)
AmericanOption{Float64}(100.0, 90.0, 0.05, 0.3, 0.4931506849315068, -1)

julia> evaluate(american_put, BlackScholes())
3.2281936525908073
```
