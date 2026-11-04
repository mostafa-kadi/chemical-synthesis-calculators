# Scientific validation notes

## Independent numerical reference checks

| Calculator | Reference inputs | Expected result |
|---|---|---:|
| Molecular weight | BaTi0.96Nb0.04O3 | 234.992560 g mol⁻¹ |
| Stoichiometric batch (product moles) | 10 g BaTiO3; M = 233.192 g mol⁻¹ (atomic-weight table dependent) | approximately 0.042883 mol |
| Precursor mass | 10 g BaTiO3 target; BaCO3 precursor; coefficient ratio 1; purity 99% | 8.547855 g |
| Doping concentration | 0.96 host-site mol + 0.04 dopant-site mol | 4.000000% |
| Molarity | 0.1 mol in 0.5 L | 0.200000 mol L⁻¹ |
| Dilution | 1.0 mol L⁻¹ stock to 0.2 mol L⁻¹; final volume 0.5 L | 0.1 L stock |
| Oxygen deficiency | m0 = 1.000 g; m1 = 0.990 g; Mformula = 200 g mol⁻¹ | δ = 0.125008 |

## Scope and assumptions

- Formula parser supports the listed element symbols, decimal occupancies and nested parentheses. It does not currently support hydrate dot notation, charge states, isotope notation, or every element in the periodic table.
- Atomic weights are fixed values embedded in app.js; values can differ slightly from a chosen IUPAC table/version.
- Stoichiometric Batch currently converts target product mass to product moles. It does not balance reactions or calculate a complete multi-precursor batch.
- Precursor Mass uses a user-entered precursor/product coefficient ratio. The user must supply a chemically balanced reaction and correct coefficient ratio; the tool does not verify elemental balance.
- Doping Concentration is the dopant fraction on the specified sublattice, not total elemental atomic percent or mass percent.
- Molarity and dilution assume additive-volume effects are negligible for the requested preparation, and dilution is only possible when target concentration does not exceed stock concentration.
- Oxygen δ from mass loss assumes the full mass change is oxygen and that m0 is the mass of the defined stoichiometric reference composition. Other volatile losses or redox changes invalidate the result.

## Validation status

The formula parser was checked against BaTi0.96Nb0.04O3 (234.992560 g mol⁻¹) and Ca3(PO4)2 (310.174000 g mol⁻¹). Invalid element symbols, zero/invalid precursor purity and mass gain in an oxygen-loss calculation are rejected.

This is a formula-level and numerical validation, not a substitute for reaction balancing, thermogravimetric endpoint verification, or independent analytical measurements.