To build the digital model for a **spray extruder nozzle** inside your CAD software, the system requires precise fluid dynamic geometries to process the waxy maize amylopectin matrix and corn lipids cleanly without clogging.

Nozzle Geometry Constants

-   **Orifice Diameter (\(D_{o}\)):** 150 to 250 micrometers (\(\mu m\)).
-   **Capillary Aspect Ratio (\(L/D_o\)):** 4:1 (ensures uniform laminar flow development).
-   **Extrusion Pressure Boundary (\(\Delta P_{ext}\)):** 45 to 65 psi.

Shear-Rate Dependent Viscosity Equation

Because your plant-derived fluid is non-Newtonian, your code or simulation software must track the **Cross-Power Law Model** to predict fluid behavior inside the extruder barrel:

\(\mu (\.{\gamma })=\mu _{\infty }+\frac{\mu _{0}-\mu _{\infty }}{1+(\lambda \.{\gamma })^{n}}\)

Where:

-   \(\mu _{0}\) = Zero-shear viscosity (the fluid's thickness at rest).
-   \(\mu _{\infty }\) = Infinite-shear viscosity (the minimum thickness under high extrusion force).
-   \(\lambda \) = Structural relaxation time constant of the plant lipids.
-   \(\.{\gamma }\) = Local shear rate inside the capillary channel (\(s^{-1}\)).
