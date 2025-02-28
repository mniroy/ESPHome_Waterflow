# ESPHome Water Flow Monitoring

This project uses ESPHome to monitor water flow from two sources: a ground well and PDAM. The configuration is designed for an ESP8266-based board (esp01_1m) with two pulse counter sensors.

## Configuration

### Board
- **Platform:** ESP8266
- **Board:** esp01_1m

### WiFi
Replace `your_ssid` and `your_password` with your WiFi credentials.

### Sensors
- **Ground Well Water Flow Rate**
  - **Pin:** D5
  - **Unit:** L/min
  - **Total Usage:** L
- **PDAM Water Flow Rate**
  - **Pin:** D6
  - **Unit:** L/min
  - **Total Usage:** L

### Web Server
- **Port:** 80

## Installation

1. Install ESPHome on your computer.
2. Create a new directory for the project.
3. Save the `water_flow.yaml` configuration file in the project directory.
4. Run the following command to upload the configuration to your ESP8266 board:

   ```bash
   esphome run water_flow.yaml
   ```

## Usage

After uploading the configuration, the ESP8266 board will connect to your WiFi network. You can access the web server at `http://<your_esp8266_ip>` to monitor the water flow rates and total usage.

## License

This project is licensed under the MIT License.