# DIY 4-Port USB 2.0 Hub

I wanted to build a reliable, custom USB hub that I could easily assemble myself using through-hole (THT) components and house inside a clean, 3D-printed slide-in enclosure. Instead of buying a generic commercial hub, I decided to design my own board around the classic FE1.1s controller and build a custom housing from scratch.

## How it works & Hardware choices

The circuit keeps things maker-friendly by sticking to hand-solderable parts where possible:

- **FE1.1s Controller (SSOP-28):** The reliable workhorse for DIY 4-port USB 2.0 hubs, mounted via manual drag-soldering or an SSOP-to-DIP adapter.
- **1x USB-C (Upstream):** For a modern, clean connection to the host computer.
- **4x USB-A (Downstream):** Robust THT connectors for everyday peripherals.
- **Support components:** Standard `DIN0207` resistors, `C_Disc` capacitors, and an `HC-49U` crystal oscillator to keep assembly straightforward.

## Design notes & Things I ran into

- **KiCad Layout & DRC:** I ran into a few classic layout hurdles along the way. I had isolated GND copper islands on the top layer (`F.Cu`) that lost connection to the main ground plane, which required placing strategic vias to bridge them. I also had to clean up duplicate vias that were accidentally stacked on top of each other.
- **Enclosure & Tolerances:** Designing the slide-in housing in Fusion 360 taught me the importance of precise clearances. Factoring in a 0.1 to 0.2mm offset for the port cutouts on the front lid—using the "Combine/Cut" tool—ensured the USB connectors fit smoothly without binding.
- **Finishing Touches:** Adding extruded text labels directly onto the 3D-printed front panel gave the hub a professional, finished look right before exporting the design to STL/3MF for printing.

## Total Cost & Fabrication

Getting custom PCBs fabricated via JLCPCB, sourcing components, factoring in shipping costs, and accounting for 3D-printing filament brought the total project cost to **22.01 € (~$24.54 USD)** for a batch of 5 boards. A complete breakdown with suppliers and search terms is available in the `BOM.csv` file.