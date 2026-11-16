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

<img width="1533" height="484" alt="image" src="https://github.com/user-attachments/assets/8e76a793-cc55-41a6-9cba-3aebfe33ff5e" />
<img width="1533" height="484" alt="image" src="https://github.com/user-attachments/assets/bc1d6f57-f60f-48d2-a99b-c1803e9d7bbf" />
<img width="1452" height="307" alt="Screenshot 2026-11-15 204539" src="https://github.com/user-attachments/assets/0ab1066c-8b1c-477c-a5f3-5f33dcae1038" />
<img width="804" height="477" alt="Screenshot 2026-11-15 204508" src="https://github.com/user-attachments/assets/f396fe1c-1df8-49ab-9b50-8850b1c1f6ce" />
<img width="1333" height="434" alt="Screenshot 2026-11-16 185001" src="https://github.com/user-attachments/assets/2fe317ff-ff93-4de7-8e76-b7cc8ea8f524" />
<img width="950" height="686" alt="Screenshot 2026-11-08 205756" src="https://github.com/user-attachments/assets/7d51cbea-7fb2-41c7-b01a-532133c92470" />
<img width="742" height="380" alt="image" src="https://github.com/user-attachments/assets/44ec949e-4721-4b64-8066-3432b9f1deca" />



