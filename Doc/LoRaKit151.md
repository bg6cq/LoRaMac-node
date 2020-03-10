# LoRaKit 151 platforms support documents

LoRaKit151 MCU is STM32L151CBU6 & SX1272/6

Now only "LoRaMac" classA works.

Tested under Linux


# how to build

I using the following command to build:

```
git clone -b LoRa151Kit https://github.com/bg6cq/LoRaMac-node 
cd LoRaMac-node
mkdir build
cd build
cmake -DCMAKE_TOOLCHAIN_FILE="cmake/toolchain-arm-none-eabi.cmake" -DAPPLICATION="LoRaMac" -DSUB_PROJECT="classA" -DACTIVE_REGION="LORAMAC_REGION_CN470" -D
REGION_CN470="ON" -DBOARD="LoRaKit151" ..
make
```

The output hex file is `build/src/apps/LoRaMac/LoRaMac-classA.hex`


