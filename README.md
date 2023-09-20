[![Build](https://github.com/jorgelserve/Marlin-ToAuto/actions/workflows/build.yaml/badge.svg?branch=dev)](https://github.com/jorgelserve/Marlin-ToAuto/actions/workflows/build.yaml)
# Firmware Marlin para Artillery A1.1 de ToAuto

Este proyecto contiene las configuraciones necesarias para el firmware [Marlin 2.1.2.1](https://github.com/MarlinFirmware/Marlin/releases/tag/2.1.2.1) para las impresoras Artillery A1.1 de ToAuto

## Los cambios realizados son los siguientes:

### ```Configuration.h```
```cpp
#define MOTHERBOARD BOARD_MKS_ROBIN_NANO
#define SERIAL_PORT 3
#define BAUDRATE 115200
#define X_DRIVER_TYPE TMC2208_STANDALONE
#define Y_DRIVER_TYPE TMC2208_STANDALONE
#define Z_DRIVER_TYPE A4988
#define Z2_DRIVER_TYPE A4988
#define TEMP_SENSOR_BED 1
#define DEFAULT_Kp 22.52
#define DEFAULT_Ki 2.07
#define DEFAULT_Kd 61.26
#define PIDTEMPBED
#define DEFAULT_bedKp 77.87
#define DEFAULT_bedKi 14.98
#define DEFAULT_bedKd 269.96
#define DEFAULT_AXIS_STEPS_PER_UNIT { 80, 80, 400, 406.76 }
#define DEFAULT_MAX_FEEDRATE { 100, 100, 12, 120 }
#define DEFAULT_MAX_ACCELERATION { 960, 960, 200, 5000 
#define DEFAULT_ACCELERATION 1000
#define DEFAULT_RETRACT_ACCELERATION 1000
#define DEFAULT_TRAVEL_ACCELERATION 1000
#define CLASSIC_JERK
#define DEFAULT_XJERK 20.0
#define DEFAULT_YJERK 20.0
#define DEFAULT_ZJERK  0.4
#define S_CURVE_ACCELERATION
#define PROBE_MANUALLY
#define DISABLE_X true
#define DISABLE_Y true
#define INVERT_X_DIR true
#define INVERT_Y_DIR false
#define INVERT_Z_DIR true
#define INVERT_E0_DIR true
#define Z_HOMING_HEIGHT  5
#define Z_AFTER_HOMING  5
#define X_BED_SIZE 300
#define Y_BED_SIZE 280
#define Z_MAX_POS 40
#define FILAMENT_RUNOUT_SENSOR
#define MESH_BED_LEVELING
#define PREHEAT_BEFORE_LEVELING // To be removed
#define LCD_BED_LEVELING
#define LCD_BED_TRAMMING
#define NOZZLE_PARK_FEATURE
#define LCD_LANGUAGE es
#define SDSUPPORT
#define MKS_ROBIN_TFT35
#define TFT_COLOR_UI
#define TOUCH_SCREEN
#define TOUCH_IDLE_SLEEP_MINS 5
//#define TOUCH_SCREEN_CALIBRATION
#define TOUCH_CALIBRATION_X   16976
#define TOUCH_CALIBRATION_Y   -11527
#define TOUCH_OFFSET_X        -28
#define TOUCH_OFFSET_Y        339
#define TOUCH_ORIENTATION     TOUCH_LANDSCAPE
```
### ```Configuration_adv.h```
```cpp
#define EMERGENCY_PARSER
#define ADVANCED_PAUSE_FEATURE
```

### ```platformio.ini```
```ini
default_envs = mks_robin_nano_v1v2
```

### ```Marlin/config.ini```
```ini
monitor_speed     = 115200
```
---
### Hardware settings

|	Axis    |	X		|	Y		|	Z1		|	E0		|	Z2		|
|	---		|	---		|	---		|	---		|	---		|	---		|
|	Current |	1		|   1		|	0.8		|	0.8		|	0.8		|
|	Driver  |	TCM2208	|	TCM2208	|	A4988	|	A4988	|	A4988	|
|	Vref	|	1		|	1		|	?		|	?		|	?		|


Autor: [@jorgelserve](https://github.com/jorgelserve)
