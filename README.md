# Pebble the 65% keyboard
A 65% keyboard with fully custom parts designed using KiCAD and Solidworks. Made with a resin case, aluminum switch plate and hot swap Epomaker silent keyswitches. 
This project is my introduction to Solidworks as someone preparing for a new robotics season, When I started this project, I knew little about keyboards so I went with the essential 65% in order to keep things compact yet still having all the necessary keys, ensuring to include arrows for gaming. I named her pebble because of her smaller size, and cutesy frame design as well as the nature inspired look i origanlly had for her. 
Pebble originally had a side bar intended for stickers but with more adjustments I decided on a more compact under the spacebar component set up in order to make many of my calculations easier and lower risk of mistakes. 
features:
- 65% QWERTY layout
- Sandwich style assembly
- 6.25U spacebar
- Plate-mounted switches
- Custom PCB
- USB-C connection
- Custom switch plate

CAD photos (CAD has since been updated to accomidate standard 6.25u spacebar):
<img width="1692" height="736" alt="Screenshot 2026-09-23 135233" src="https://github.com/user-attachments/assets/03ef8f03-9678-4b7b-8c7c-2a08ce149c83" />
<img width="1536" height="836" alt="Screenshot 2026-09-23 005843" src="https://github.com/user-attachments/assets/1f91d7c1-1839-4681-b785-2610dd9647b9" />
<img width="1084" height="424" alt="Screenshot 2026-09-29 185807" src="https://github.com/user-attachments/assets/0c272561-7c0d-4330-880e-dca3fb140cb7" />

PCB photos:
<img width="1106" height="420" alt="Screenshot 2026-10-04 002206" src="https://github.com/user-attachments/assets/ae0c0b1f-ced0-4428-a67e-1a2a63f9ea39" />
<img width="1376" height="936" alt="Screenshot 2026-09-23 134752" src="https://github.com/user-attachments/assets/c899a03e-4a9b-4658-b632-a7a24c2c175c" />
<img width="1906" height="686" alt="image" src="https://github.com/user-attachments/assets/921df819-28b6-460f-965a-a5f17abc1b15" />
<img width="1206" height="836" alt="image" src="https://github.com/user-attachments/assets/a5a65e39-f813-4992-9e18-50e4539f542d" />

assembly guild: 
1. Solder all parts onto PCB (including capacitors, diodes and hot swap sockets)
2. Flash the microcontroller (Code is in "Code" folder)
3. lower the pcb into the casing
4. attack stablizers to the underside of the switch plate
5. place switch plate on top of casing (be careful to align the keys)
6. press all 69 keys into their positions
7. place bezel on top of switch plate and screw into place (9 M3 16mm screws)
8. click keycaps onto key switches


Pictures of assembly design process below: 
<img width="1090" height="390" alt="image" src="https://github.com/user-attachments/assets/360135db-9f00-4a4c-987c-7e2b63983f19" />

Bill of materials:
https://docs.google.com/spreadsheets/d/1lCmeEfUbG34g1hUgpbVch2w63U2JIJnhS8jueZ3TIsw/edit?usp=sharing 
| Id                            | Designator                                                                                                              | Footprint                           | Quantity    | Designation                                                                                                   | Subtotal | Link                                                                                              |
| :---------------------------- | :---------------------------------------------------------------------------------------------------------------------- | :---------------------------------- | :---------- | :------------------------------------------------------------------------------------------------------------ | :------- | :------------------------------------------------------------------------------------------------ |
| 1                             | MX1-MX69                                                                                                                | SW_MX_HS_CPG151101S11_1u            | 69(4 packs) | MX_SW_HS                                                                                                      | $33.96   | https://www.amazon.ca/TOGEVAL-Hot-swappable-Mechanical-Keyboard-Assembly/dp/B0GHMCD6SP            |
| 2                             | U1                                                                                                                      | LQFP-48_7x7mm_P0.5mm                | 1           | STM32F072CBT6                                                                                                 | $10.47   | https://www.digikey.ca/en/products/detail/stmicroelectronics/STM32F072CBT6/4815292                |
| 3                             | C1, C3, C4, C5, C6                                                                                                      | C_1206_3126Metric                   | 7+1         | 100nF                                                                                                         | $4.16    | https://www.digikey.com/en/products/detail/kemet/C1206C104KARACTU/992167                          |
| 4                             | C9, C10                                                                                                                 | C_1206_3126Metric                   | 2           | 1uF                                                                                                           | $1.26    | https://www.digikey.ca/en/products/detail/yageo/CC1206KKX7R7BB105/302915                          |
| 5                             | R1 - R4                                                                                                                 | R_1206_3126Metric                   | 4           | 5.1k                                                                                                          | $0.40    | https://www.digikey.com/en/products/detail/stackpole-electronics-inc/RMCF1206FT5K10/1759499       |
| 6                             | BOOT1, RST1                                                                                                             | SW_SPST_TL3342                      | 2           | SW_SPST                                                                                                       | $2.26    | https://jlcpcb.com/partdetail/ESwitch-TL3342F260QG/C2886894                                       |
| 7                             | J1                                                                                                                      | USB_C_Receptacle_HRO_TYPE-C-31-M-12 | 1           | USB_C_Receptacle_USB2.0                                                                                       | $3.84    | https://www.digikey.ca/en/products/detail/same-sky-formerly-cui-devices/UJ31-CH-G2-SMT-TR/8024063 |
| 8                             | F1                                                                                                                      | Fuse_1206_3216Metric                | 1           | 500mA                                                                                                         | $0.46    | https://www.lcsc.com/product-detail/C135341.html                                                  |
| 9                             | U5                                                                                                                      | C_0402_1005Metric                   | 1           | TXB0101                                                                                                       | $0.71    | https://www.lcsc.com/product-detail/C324081.html                                                  |
| 10                            | U3                                                                                                                      | SOT-23                              | 1           | XC6206PxxxMR-Regulator_Linear                                                                                 | $0.72    | https://www.lcsc.com/product-detail/C5446.html                                                    |
| 11                            | D1-D69                                                                                                                  | D_SOD-123                           | 69+5        | D_small                                                                                                       | $5.42    | https://www.digikey.ca/en/products/detail/shenzhen-slkormicro-semicon-co-ltd/1N4148W/21853071     |
| 12                            | U2                                                                                                                      | SOT-143                             | 1           | PRTR5V0U2X                                                                                                    | $0.43    | https://www.lcsc.com/product-detail/C12333.html                                                   |
| 13                            | C2                                                                                                                      | C_1206_3216Metric                   | 1           | 10uF                                                                                                          | $1.49    | https://www.digikey.ca/en/products/detail/kemet/C1206C106K8RACTU/1090842                          |
| 14                            | C43, C44                                                                                                                | C_1206_3216Metric                   | 2           | 0.1uF                                                                                                         | $0.40    | https://www.digikey.ca/en/products/detail/tdk/C3216X7R2A104M160AA/513969                          |
| 15                            | J2                                                                                                                      | PinHeader_1x05_P2.54mm_Vertical     | 1           | Conn_01x05                                                                                                    | $0.29    | https://www.digikey.ca/en/products/detail/harwin-inc/M20-9990546/3728232                          |
| 16                            | J3                                                                                                                      | PinHeader_1x06_P2.54mm_Vertical     | 1           | Conn_01x06                                                                                                    | 1.39     | https://www.digikey.ca/en/products/detail/sullins-connector-solutions/PEC06SAFN/859339            |
|                               |                                                                                                                         |                                     |             |                                                                                                               |          |                                                                                                   |
| Physical (already purchased): |                                                                                                                         |                                     |             |                                                                                                               |          |                                                                                                   |
| Id                            | Name                                                                                                                    | quantity                            | subtotal    | link                                                                                                          |          |                                                                                                   |
| 1                             | EPOMAKER Lilac Silent Tactile Switch Set                                                                                | 1                                   | $38         | https://epomaker.ca/products/epomaker-lilac-silent-tactile-switch-set?_pos=1&_psq=lilac&_psid=7e47da251&_ss=e |          |                                                                                                   |
| 2                             | DUROCK Plate Mount Stabilizer V3                                                                                        | 1                                   | $19.93      | https://www.amazon.ca/dp/B0CTHT34MJ?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1                                    |          |                                                                                                   |
| 3                             | dagaladoo Coffee Cat 140key keycaps,XDA Profile,dye Sublimation PBT Custom keycap with Key Puller for Gateron MX Switch | 1                                   | $30         | https://www.amazon.ca/dp/B0CF1ZS6D4?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1                                    |          |                                                                                                   |
|                               |                                                                                                                         |                                     |             |                                                                                                               |          |                                                                                                   |
| JLC estimates: $90            |                                                                                                                         |                                     |             |                                                                                                               |          |                                                                                                   |
|                               |                                                                                                                         |                                     |             |                                                                                                               |          |                                                                                                   |
| Total: 245.66                 |                                                                                                                         |                                     |             |                                                                                                               |          |                                                                                                   |

not included in BOM: Soldering iron, Flux, Solder, Wicks, Fume extractor

All designs complete, assembly ongoing
(designed using Kicad, Solidworks and sketchbook)
(files with numbers ex:open2, are completed(not verified works.)

Known issues: None, 
Credits: My father for introducing me to all this. 
Sanity checked by my lovely best friend 
