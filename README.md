# Capsule ESPHome configuration

This repository contains the ESPHome configuration files for the [domodulo Capsule](https://domodulo.io/capsule) device.

Follow the [official documentation](https://domodulo.io/capsule-docs) to assemble and setup the Capsule.

For more advanced configuration examples, see the [Capsule examples](https://domodulo.io/capsule-examples).

## Configuration files

- [`capsule.yaml`](./capsule.yaml) is the main configurable package. It includes the base board and provides commented examples for enabling the battery sensor, button modules, and LED matrix. Uncomment and configure the modules you have connected.
- [`capsule-button-led-matrix-kit.yaml`](./capsule-button-led-matrix-kit.yaml) is a preset configuration for the [Capsule button & LED matrix kit](https://domodulo.io/shop/p/capsule-button-led-matrix-kit)
- [`capsule-double-button-kit.yaml`](./capsule-double-button-kit.yaml) is a preset configuration for the [Capsule double button kit](https://domodulo.io/shop/p/capsule-double-button-kit)
- [`capsule-factory.yaml`](./capsule-factory.yaml) is the base factory configuration. It enables the base board, ESPHome Dashboard import, and Improv provisioning over Bluetooth LE and serial; optional modules are not enabled.

## Modules

The [`modules/`](./modules) directory contains reusable ESPHome package configurations included by the top-level YAML files:

- [`base.yaml`](./modules/base.yaml) sets up the ESP32-S3 board, Wi-Fi access point and captive portal, API and OTA, base LED, buzzer service, and I²C.
- [`button.yaml`](./modules/button.yaml) configures a button and its four-LED strip. It takes substitutions for the button and LED IDs, names, and GPIO pins.
- [`led_matrix.yaml`](./modules/led_matrix.yaml) configures a 100-LED strip for the matrix and takes its GPIO pin as a substitution.
- [`battery.yaml`](./modules/battery.yaml) adds a battery-voltage ADC sensor with a voltage-divider correction. Include it when using battery power.
