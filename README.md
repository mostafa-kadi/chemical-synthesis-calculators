# Chemical Synthesis Calculators

Seven browser-based tools: molecular weight, target product amount, a three-precursor batch planner, single-precursor mass, dopant fraction on a selected sublattice, molarity and dilution, and oxygen non-stoichiometry from mass loss.

## Scientific conventions
- Formula parser supports common elements, decimal occupancies and parentheses; supported atomic weights are listed in `app.js`.
- Precursor mass requires the correct balanced-reaction coefficient ratio and precursor purity.
- Oxygen δ mass method assumes all measured mass loss is oxygen.
- Doping fraction is defined on the supplied sublattice.

Open `index.html` directly or deploy the repository root as a static site. No backend or external dependencies.