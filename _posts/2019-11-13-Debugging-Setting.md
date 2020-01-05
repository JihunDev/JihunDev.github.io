---
layout: post
title: Nucleo Debugging Setting
tags: Nucleo
comments: true
---

Nucleo Debugging Setting

## Download

### Windows

[ST Link Driver](https://os.mbed.com/teams/ST/wiki/ST-Link-Driver)

[Trea Term](https://ko.osdn.net/projects/ttssh2/releases/)



## Example Code

```C++
#include "mbed.h"

// define the Serial object
Serial pc(USBTX, USBRX);

DigitalOut led1(LED1);

int main() {
    while (true) {
        led1 = !led1;

        // Print something over the serial connection
        pc.printf("Blink! LED is now %d\r\n", led1.read());

        wait(0.5);
    }
}
```

## Seeing the Log Message

### Windows

1. open TeraTerm
2. File > New connetion
3. Serial Button
4. Chooce `mbed Serial Port`
5. Click OK
6. Log message

