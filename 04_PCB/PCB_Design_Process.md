# PCB Design Process

## Workflow

Schematic → Annotate → Footprints → ERC → Update PCB → Board outline →
Placement → Routing → Copper pour → DRC → 3D inspection → Gerbers

## Placement priorities

1.  Mechanical interfaces.
2.  ESP32-S3 antenna keepout.
3.  Power subsystem grouping.
4.  Audio path.
5.  Low-speed control signals.

## Routing priorities

1.  Power.
2.  Ground/return paths.
3.  Clock/data interfaces.
4.  I²S.
5.  Low-speed GPIO.

## Custom board outline

The outer boundary belongs on **Edge.Cuts** and must be a single closed,
non-self-intersecting contour.

Reference geometry should be placed on a user drawing layer, not
Edge.Cuts.

## Copper

Use a ground copper pour where appropriate and refill after routing
changes.

## DRC

Run DRC after major routing, outline, footprint and copper changes. Save
a screenshot of the final result.

## Status

-   Schematic: designed
-   Footprints: assigned
-   Placement: iterated
-   Routing: iterated
-   Copper pour: completed
-   Custom outline: created
-   DRC: iterated
-   Fabrication: pending
