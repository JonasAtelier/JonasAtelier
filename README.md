<p align="center">
  <img src="assets/atelier-banner.svg"
       alt="Jonas Atelier embedded library workshop"
       width="100%">
</p>

<h1 align="center">Jonas Atelier</h1>

<p align="center">
  Drivers for the parts robots are actually built from — motors and encoders,
  sensing, power, buses. Plain C99, no dependencies, no allocation, and no
  build system to adopt: copy two files in and go.
</p>

<p align="center">
  Every register value is traced to a line in the datasheet, and the comment
  next to it says which one. Where a vendor does not publish a register map,
  the README says so rather than pretending otherwise.
</p>

<p align="center">
  IMUs, barometers, encoders and magnetometers each share one subsystem,
  <code>esp-imu</code>, <code>esp-baro</code>, <code>esp-encoder</code> or
  <code>esp-compass</code>, built the way Linux IIO is: every chip probes into
  the same <code>struct imu_dev</code>, <code>struct baro_dev</code>,
  <code>struct encoder_dev</code> or <code>struct compass_dev</code> and reads
  out one sample shape, so swapping the sensor never touches the code above it.
</p>

<p align="center">
  ✅ Available · 🧪 Hardware validation · 🚧 On-going
</p>

<pre>
├── ⚡ ESP32 / ESP-IDF
│   ├── esp-c620-control       — RoboMaster M3508 / C620 motor control  🧪
│   ├── esp-HT03               — HT-03 actuators, MIT protocol over CAN 🚧
│   ├── esp-drv8323-gatedriver — DRV8323 three-phase gate driver        🚧
│   ├── esp-tmc5240-stepper    — TMC5240 stepper, on-chip ramps         🧪
│   ├── esp-tmc2209-stepper    — TMC2209 stepper over UART              🚧
│   ├── esp-pca9685-pwm        — PCA9685 16-channel PWM                 🧪
│   ├── esp-servo-pwm          — RC servos on LEDC                      🚧
│   ├── esp-imu                — IMUs: MPU-6050, ICM-45686, BMI088      🧪
│   ├── esp-encoder            — Encoders: AS5600, AS5047P, AMT102-V    🚧
│   ├── esp-baro               — Baro: BMP280, BMP388, DPS310, MS5611   🧪
│   ├── esp-compass            — Magnetometers: QMC5883L, QMC5883P      🧪
│   ├── esp-ld19-lidar         — LD19 / LD06 360° lidar                 🚧
│   ├── esp-vl53l1x-tof        — VL53L1X time-of-flight                 🚧
│   ├── esp-hx711-loadcell     — HX711 load cell amplifier              🧪
│   ├── esp-nau7802-loadcell   — NAU7802 24-bit bridge ADC              🧪
│   ├── esp-ads1115-adc        — ADS1115 16-bit ADC                     🧪
│   ├── esp-ina2xx-sensor      — INA219/226/228 power monitors          🧪
│   ├── esp-max17048-fuelgauge — MAX17048 1S fuel gauge                 🧪
│   ├── esp-bq769x0-bms        — bq769x0 3–15S pack monitor             🧪
│   ├── esp-ps-controller      — DualShock 4 / DualSense over BT        🧪
│   ├── esp-crsf-rc            — CRSF / ELRS receiver                   🧪
│   ├── esp-mcp23-expander     — MCP23017 I/O expander                  🚧
│   ├── esp-ssd1306-oled       — SSD1306 OLED                           🧪
│   ├── esp-ws2812-led         — WS2812 LEDs over RMT                   🚧
│   ├── esp-sn65hvd230-can     — Classic CAN over TWAI                  ✅  <a href="https://github.com/JonasAtelier/esp-sn65hvd230-can">🔗</a>
│   ├── esp-mcp2515-can        — MCP2515 CAN over SPI                   🧪
│   ├── esp-dw1000-uwb         — DW1000 UWB two-way ranging             🧪
│   ├── esp-espnow-link        — ESP-NOW packets between boards         🚧
│   ├── esp-ota-wifi           — On-demand Wi-Fi OTA                    🧪
│   └── esp-sdlog              — Buffered SD-card logger                🚧
│
├── 🔩 STM32 / HAL
│   ├── stm-imu           — IMUs: MPU-6050, ICM-45686, BMI088    🚧
│   ├── stm-baro          — Baro: BMP280, BMP388, DPS310, MS5611 🚧
│   ├── stm-compass       — Magnetometers: QMC5883L, QMC5883P    🚧
│   └── stm-ina2xx-sensor — INA219/226/228 power monitors        🚧
│
├── 🐧 Linux
│   ├── nv-ps-controller — PS4 / PS5 pads on NVIDIA Jetson       🚧
│   └── Robust           — ROS 2's model, in plain C, one device 🚧
│
└── 🧰 General
    ├── upid            — Portable PID control                 ✅  <a href="https://github.com/JonasAtelier/upid">🔗</a>
    ├── adrc            — Active disturbance rejection control 🚧
    ├── lqr             — Discrete-time LQR gains              🚧
    ├── foc             — Field-oriented control maths         🧪
    ├── fsm             — Table-driven finite state machines   🧪
    ├── bt              — Behaviour trees                      🚧
    ├── kin             — Forward / inverse kinematics         🧪
    ├── dyn             — Arm dynamics, recursive Newton-Euler 🚧
    ├── mob             — Wheel kinematics &amp; odometry          🚧
    ├── path            — Spline path &amp; pure pursuit           🚧
    ├── imp             — Impedance &amp; admittance control       🧪
    ├── f_kalman        — Scalar Kalman filter                 🧪
    ├── f_complementary — Complementary filter                 🧪
    ├── f_particle      — Particle filter                      🧪
    ├── f_madgwick      — Madgwick AHRS filter                 🚧
    ├── f_ekf           — Extended Kalman filter               🚧
    └── f_rls           — Recursive least squares              🚧
</pre>

<p align="center">
  <img src="assets/ledger.svg"
       alt="82 repositories, 67 written in C, 712 commits, active since 2023"
       width="100%">
</p>

<p align="center">
  Everything here is plain C99 — one header, one source file, copy them in.
  <br>
  Projects become clickable after hardware validation and public release.
</p>

<p align="center">
  <a href="https://github.com/JonasAtelier/jonas-atelier-libraries"><b>Full catalog, including what is coming →</b></a>
</p>
