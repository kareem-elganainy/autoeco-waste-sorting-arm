# AutoEco: AI-Powered Waste Sorting Arm with Smart Plant Irrigation

A low-cost robotic system that does two things:

1. **Sorts waste**: a robotic arm uses a camera and AI to recognize items and place them in the right bin (plastic, paper, or metal).
2. **Waters plants**: a separate smart unit waters plants automatically when the soil is dry.

> 🚧 Work in progress. See the [Roadmap](#roadmap) for progress.

## How It Works

```
Camera -> Raspberry Pi (YOLO detects the item) -> Arduino Uno -> robotic arm -> correct bin

Soil sensor -> Arduino Nano -> water pump -> plants   (works on its own)
```

- The camera captures the waste items and the Raspberry Pi identifies each one using a YOLO model.
- The arm picks the item with a vacuum gripper and drops it in the matching bin.
- A metal sensor double-checks metal items, and ultrasonic sensors track how full each bin is.
- The irrigation unit runs on its own board, so plants keep getting water even if the arm stops.
- A simple web dashboard shows sorting counts, bin levels, and soil moisture.

## Main Parts

- Raspberry Pi 5 and USB webcam
- 4-DOF robotic arm (MG996R servos), Arduino Uno, PCA9685 driver
- Vacuum pump with suction cup
- Inductive metal sensor and 3 ultrasonic sensors
- Arduino Nano, soil moisture sensor, and water pump

## Repository Structure

```
├── hardware/        wiring, designs, photos
├── software/
│   ├── vision/      YOLO detection
│   ├── arm_control/ arm movement and serial communication
│   └── dashboard/   web dashboard
├── arduino/
│   ├── arm/         Arduino Uno code
│   └── irrigation/  Arduino Nano code
├── docs/            images and diagrams
└── dataset/         dataset links
```

## Roadmap

- [ ] Build the arm and test servos
- [ ] Gripper, bins, and sensors
- [ ] Irrigation system
- [ ] Collect data and train the model
- [ ] Camera calibration and pick-and-place
- [ ] Full integration
- [ ] Dashboard and final demo

## Team

**Team Leader:** Mohamed Ahmed Mohamed Mawafy

**Members (GitHub):**

[@abdulrahmansabry41-code](https://github.com/abdulrahmansabry41-code) ·
[@ahmedhossamelhadad-ship-it](https://github.com/ahmedhossamelhadad-ship-it) ·
[@AhmedSamir148](https://github.com/AhmedSamir148) ·
[@ahmoda7](https://github.com/ahmoda7) ·
[@ali-gaafar-99](https://github.com/ali-gaafar-99) ·
[@aliarafat034-coder](https://github.com/aliarafat034-coder) ·
[@azabbadr432-debug](https://github.com/azabbadr432-debug) ·
[@badrmohamed80090-sketch](https://github.com/badrmohamed80090-sketch) ·
[@belalashry79-dot](https://github.com/belalashry79-dot) ·
[@elgobarymohamed04-jpg](https://github.com/elgobarymohamed04-jpg) ·
[@eo369638-collab](https://github.com/eo369638-collab) ·
[@hadyayman1213-boop](https://github.com/hadyayman1213-boop) ·
[@hanyasmaylrjb-arch](https://github.com/hanyasmaylrjb-arch) ·
[@hsswd112-boop](https://github.com/hsswd112-boop) ·
[@ibrahimsalem30](https://github.com/ibrahimsalem30) ·
[@KMHob-allah](https://github.com/KMHob-allah) ·
[@M0NZ-ER](https://github.com/M0NZ-ER) ·
[@maged-abu-amer](https://github.com/maged-abu-amer) ·
[@medo-ouf-95](https://github.com/medo-ouf-95) ·
[@medomof7521-tech](https://github.com/medomof7521-tech) ·
[@MohamedAbdallah445](https://github.com/MohamedAbdallah445) ·
[@mohamedabdalmeged](https://github.com/mohamedabdalmeged) ·
[@mohamedsalah20elmo-arch](https://github.com/mohamedsalah20elmo-arch) ·
[@muawiyafathy2137-boop](https://github.com/muawiyafathy2137-boop) ·
[@tarqjlal97-ship-it](https://github.com/tarqjlal97-ship-it) ·
[@tifaanous29-oss](https://github.com/tifaanous29-oss) ·
[@yassenhassan234-bot](https://github.com/yassenhassan234-bot) ·
[@kareem-elganainy](https://github.com/kareem-elganainy)
