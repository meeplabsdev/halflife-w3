# Piano Keys
<img width="940" height="667" alt="image" src="https://github.com/user-attachments/assets/bc1ea58e-d6db-41e2-bf91-b83135cea26a" />


# What it is
For the third week of [halflife](https://halflife.hackclub.com/), I decided to create a midi instrument. It uses capacitive touch to recognise when the keys are pressed, and use 16 zones per key (multiplexed). This means that while each key is single touch itself, it supports full multi touch across all the keys. It also allows us to determine the exact position of the finger on the key by taking readings from each zone and interpolating between them (since the readings differ depending on how close or far you are from each zone). It ALSO allows us to determine the velocity the key was pressed with and also the aftertouch pressure being applied, which can be approximated by the rate of change of the distance proxy, and by the reading produced by each zone respectively. (If four zones, one on each size of the finger, all show a lower reading then the finger is not compressed against the key, and if they show a higher reading it is because the finger is pushed harder against the key and has spread out).

# Cost
This is a rough outline of the cost, see [`BOM.csv`](BOM.csv) for more details.

| Part | Cost |
| --- | --- |
| [Unpopulated PCB](https://jlcpcb.com/) | $62.10 |
| [Pi Pico](https://www.rapidonline.com/raspberry-pi-sc0915-pico-rp2040-microcontroller-board-75-1132) | $4.83 |
| [Multiplexers](https://www.lcsc.com/product-detail/C6525.html) | $15.11 |
| **Total + Shipping** | **$99.56** |
