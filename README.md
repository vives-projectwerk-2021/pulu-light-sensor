# LightSensorDriver

Library for the light sensor LTR329ALS01

## Example

```c
#include "mbed.h"
#include "Lightsensordriver_refactored.h"

I2C i2c(I2C_SDA, I2C_SCL);

LightSensors light(&i2c);

int main()
{
    while (1) 
    {
        ThisThread::sleep_for(500ms);
        
        // because printf doesn't support float values in mbed
        double AmountLux = light.readLux();
        printf("Lux:", int(AmountLux));
    }
}

```
