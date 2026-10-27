# Liquid Class Bench

A simulated P200 air-displacement pipette channel for exploring liquid-class settings: aspirate and dispense rates, delays, and blowout.

**Live page:** https://sl148.github.io/liquid-class-bench/

- **Simulate:** watch one transfer as an animated tip cross-section, with channel pressure, tip contents, and a breakdown of where volume is lost (lag, wall film, hanging drop, splash, and more).
- **Optimize:** random search over liquid classes for the selected liquid, with a speed vs accuracy Pareto front and an aspirate × dispense rate map.
- **Model:** the equations and loss mechanisms.
- **Guide** (top right): labels, per-phase captions, and short notes that explain each view.

The model is a lumped air-spring and liquid-column ODE. It includes cone Poiseuille and Sampson resistance, Cox-Voinov film onset, Jeffreys film drainage, and a Tate-limited hanging drop. Each run takes a few milliseconds in the browser.

**Limits:** the coefficients come from textbook scaling laws and typical polypropylene contact angles. They are not calibrated against an instrument. Use the trends for intuition, not as settings to copy to a robot.

The page is a single self-contained `index.html` with no build step.
