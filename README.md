# paintbot
CNC Pigment
# Q: How would you describe an X–Y plotter that applied liquid pigment to surfaces?

Short description
- A liquid-pigment X–Y plotter is a gantry-style robotic system that moves a dispensing head precisely over a flat substrate and deposits controlled amounts of liquid pigment (inks, dyes, watered-down paint, etc.) to draw lines, fills or raster images. Think of an industrial inkjet + CNC plotter hybrid configured for higher-viscosity pigments and larger droplets than typical office printers.

What it consists of
- Motion system: X and Y axes (belt/rail/lead-screw or linear rails) driven by stepper or servo motors, with a Z axis or fine Z-adjust for nozzle height. Resolution typically ranges from ~50 µm (desktop/bespoke) to 200 µm (large-format).
- Dispensing head: could be a pen/fountain-feed, valve-based micro-dispenser, syringe/piston pump, peristaltic pump, or piezo/thermal inkjet head depending on pigment viscosity and droplet control needed.
- Fluidics: reservoirs, tubing, valves, filters, and sometimes a pressurization or suction system to maintain steady flow and prevent drips.
- Electronics & control: microcontroller or motion controller that accepts vector paths (G-code or SVG->paths), stepper drivers, pump/valve drivers, and optionally closed-loop encoders.
- Software: toolpath generation from vector graphics or raster-to-path conversion, flow-pressure synchronization, and feed-rate/duty adjustments for line thickness or opacity.
- Ancillary: substrate fixtures, drying/curing module (heat, blower or UV if using UV-curable pigments), cleaning station, and optionally a vision/camera system for registration.

Key performance variables and design tradeoffs
- Droplet/line size: nozzle diameters from <100 µm (fine inkjet) to >1 mm (thicker paint lines). Smaller droplets = higher resolution but higher clogging risk and stricter pigment chemistry.
- Flow control: peristaltic/syringe pumps give volumetric control but slower; valve dispensers give fast on/off for strokes; inkjet offers high speed and fine control if pigment is low-viscosity and well-filtered.
- Motion accuracy vs speed: belts are fast but lower positional repeatability than ball screws; choose based on required line smoothness and throughput.
- Pigment properties: viscosity, particle size, solids content and surfactants determine whether a piezo head will clog or a syringe/valve is needed. Surface tension and substrate wetting affect line spreading and feathering.
- Nozzle-to-substrate gap and dwell time control wetting and bleed; drying/curing rate affects layering and color mixing.

Practical challenges
- Clogging and maintenance are the biggest operational issues (need filtration, purge/flush cycles).
- Color mixing and gradients require careful control of per-channel flow and possibly a mixing manifold.
- Substrate variability (porous vs non-porous) changes line profile; test prints & pre-treatment may be necessary.
- Safety/ventilation if solvents or volatile pigments are used.

Typical specs (examples to guide choices)
- Working area: 200×200 mm (desktop) to 1200×2400 mm (large-format).
- Positioning accuracy: 0.05–0.2 mm (50–200 µm).
- Line width: 0.1–5.0 mm depending on nozzle.
- Flow rate control: 0.01–10 mL/min depending on pump/nozzle.
- Throughput: tens to hundreds of mm/s for vector drawing; lower for high-res raster passes.

Applications
- Generative or algorithmic art, signage, textile printing, prototyping surface coatings, material deposition for experiments, custom ceramic/wood staining, and educational “drawbot” projects.

Follow-up offer
- If you want one designed or compared: tell me whether the pigment is low-viscosity (ink-like) or high-viscosity (paint), the working area you need, required line resolution, and whether you need multi-color mixing or just a single-channel dispenser—I can propose specific head types, pump choices, and a basic bill of materials or architecture.
