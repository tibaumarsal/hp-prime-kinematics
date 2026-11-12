# HP Prime Kinematics Toolkit

A set of HP Prime programs (HP PPL + CAS) that automate the full kinematic analysis of a particle moving in 2D/3D. Given the trajectory as a function of time, the programs symbolically derive and display:

- Position, velocity and acceleration vectors and their magnitudes
- Frenet–Serret frame: unit tangent, normal and binormal vectors
- Tangential and normal components of acceleration
- Curvature and radius of curvature

The toolkit works in three coordinate systems and includes helper programs to convert between them. It was written from scratch and has been adopted as a support tool by a university tutoring academy.

## Programs

| Program | Coordinate system | Purpose |
|---|---|---|
| `ca`  | Cartesian (x, y, z) | Full kinematic analysis |
| `cac` | Cartesian → polar / spherical | Coordinate conversion |
| `ci`  | Cylindrical (ρ, θ, z) | Full kinematic analysis |
| `cic` | Cylindrical → Cartesian / spherical | Coordinate conversion |
| `es`  | Spherical (r, θ, φ) | Full kinematic analysis |
| `esc` | Spherical → Cartesian / cylindrical | Coordinate conversion |

## How it works

Each analysis program uses the HP Prime CAS to differentiate the trajectory functions symbolically (`diff`, `simplify`), builds the velocity and acceleration vectors in the chosen coordinate system, and then computes the Frenet frame (`cross` products), the intrinsic acceleration components and the curvature. Results are printed to the terminal with readable derivative notation.

## Usage

1. Define the trajectory functions of `t` in the CAS, e.g. for Cartesian coordinates: `x(t):=...`, `y(t):=...`, `z(t):=...`
2. Run the corresponding program (`ca()`, `ci()` or `es()`).
3. Read the results in the terminal.

## Repository structure

- `src/` – readable source code (`.hppl`), extracted from the calculator files
- `hpprgm/` – original HP Prime program files, ready to transfer with HP Connectivity Kit

## Author

Marçal Tibau – Mechanical Engineering student at Universitat Politècnica de Catalunya (UPC)
