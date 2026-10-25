# Piano Keys
<img width="940" height="667" alt="image" src="https://github.com/user-attachments/assets/bc1ea58e-d6db-41e2-bf91-b83135cea26a" />


# What it is
For the third week of [halflife](https://halflife.hackclub.com/), I decided to create a midi instrument. It uses capacitive touch to recognise when the keys are pressed, and use 16 zones per key (multiplexed). This means that while each key is single touch itself, it supports full multi touch across all the keys. It also allows us to determine the exact position of the finger on the key by taking readings from each zone and interpolating between them (since the readings differ depending on how close or far you are from each zone). It ALSO allows us to determine the velocity the key was pressed with and also the aftertouch pressure being applied, which can be approximated by the rate of change of the distance proxy, and by the reading produced by each zone respectively. (If four zones, one on each size of the finger, all show a lower reading then the finger is not compressed against the key, and if they show a higher reading it is because the finger is pushed harder against the key and has spread out).

# Schematic
<img width="1506" height="754" alt="image" src="https://github.com/user-attachments/assets/e2ccc334-e4cb-4192-b00c-0bd52bc1e6c8" />

# PCB (4 layers)
<img width="1101" height="707" alt="image" src="https://github.com/user-attachments/assets/e31122f3-827c-468f-a19d-1fb59f80e696" />
<img width="1129" height="731" alt="image" src="https://github.com/user-attachments/assets/4fd0d1b3-a58b-441b-9d12-0cf655dd318a" />
<img width="1090" height="700" alt="image" src="https://github.com/user-attachments/assets/07cd4503-5d76-4c9c-a550-240369221017" />
<img width="1104" height="707" alt="image" src="https://github.com/user-attachments/assets/51e59ab6-5c7d-44f0-9b32-3404250c58c4" />

# Cost
This is a rough outline of the cost, see [`BOM.csv`](BOM.csv) for more details.

| Part | Cost |
| --- | --- |
| [Unpopulated PCB](https://jlcpcb.com/) | $62.10 |
| [Pi Pico](https://thepihut.com/products/raspberry-pi-pico?variant=41925332533443) | $5.08 |
| [Multiplexers](https://www.lcsc.com/product-detail/C6525.html) | $15.11 |
| **Total + Shipping** | **$99.56** |
