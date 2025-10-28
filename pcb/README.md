# PCB

> [!TIP]
> If this is your first visit, please read the [Getting Started guide](./../docs/GETTING_STARTED.md) first.

---

## PCB List

| File | Description | Note |
|---|---|---|
| `delta-omega-rev4-handsolder-both` | Main Left & Right PCB with mouse-bite connection | MB Not tested. |
| `delta-omega-rev4-handsolder-left` | Main Left PCB | |
| `delta-omega-rev4-handsolder-right` | Main Right PCB | |
| `delta_omega_bottom_cover` | Bottom cover PCB plate | Reversible |

---

## How to Order

This guide is written based on **[JLCPCB](https://jlcpcb.com)**. While other PCB manufacturers may differ slightly, most ordering steps are very similar.

To place an order, you will need the **Gerber archive**. Simply upload the ZIP file found in [./gerbers/](./gerbers/) to the JLCPCB order page.

> [!NOTE]
> In JLCPCB’s Gerber Viewer, the edge cuts for hand-soldering switch may not appear. This is a known JLCPCB viewer issue and does **not** affect the actual manufacturing.

---

### Recommended Options

| Specification     | Recommended                          | Notes                                                                 |
|-------------------|--------------------------------------|----------------------------------------------------------------------|
| Base Material     | FR-4                                 | Standard PCB substrate material                                      |
| Layers            | 2                                    | Two-layer board                                                      |
| PCB Quantity      | As many as needed                    |                                                                      |
| Product Type      | Industrial / Consumer Electronics    |                                                                      |
| Different Designs | 1                                    | If uploading a combined left & right PCB Gerber, select **2**.[^1]   |
| PCB Thickness     | 0.8 mm or 1.6 mm                     | See [Getting Started](./../docs/GETTING_STARTED.md) for details         |
| PCB Color         | Your preference                      |                                                                      |
| Surface Finish    | Your preference                      |                                                                      |
| Mark on PCB       | Remove Mark                          | Recommended for a cleaner finish                                     |

[^1]: If not selected, JLCPCB will automatically review your order and guide you to the correct option.
