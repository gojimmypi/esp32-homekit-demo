# Example for `Partitions`

## What it does

It's makes sure it fit's into a 2 MB flash size insuring, that it even works on the smallest ESP32.

## Partition


| # Name                    |      Type   |   SubType |   Offset     |      Size |  Flags |
|---------------------------|-------------|-----------|--------------|-----------|--------|
| # partition table         |  0x08000    |   0x1000  |              |           |        |
| otadata                   |    data     |   ota     |      0x09000 |  0x2000   |        |
| phy_init                  |   data      |   phy     |      0x0b000 |  0x1000   |        |
| lcmcert_1                 |  0x65       |   0x18    |     0x0c000  |  0x1000   |        |
| lcmcert_2                 |  0x65       |   0x18    |     0x0d000  |  0x1000   |        |
| nvs                       |        data |   nvs     |      0x10000 |  0x4000   |        |
| homekit                   |    data     |   homekit |  0x14000     |  0x1000   |        |
| ota_0                     |      app    |    ota_0  |    0x20000   |  0xF0000  |        |
| ota_1                     |      app    |    ota_1  |    0x110000  |  0xF0000  |        |



| # Name                    |  Type |  SubType |  Offset  |  Size |  Flags |
|---------------------------|-------|----------|----------|-------|--------|
| otadata                   | data  | ota      | 0x9000   | 8K    |        |
| phy_init                  | data  | phy      | 0xb000   | 4K    |        |
| lcmcert_1                 | 101   | 24       | 0xc000   | 4K    |        |
| lcmcert_2                 | 101   | 24       | 0xd000   | 4K    |        |
| nvs                       | data  | nvs      | 0x10000  | 16K   |        |
| homekit                   | data  | homekit  | 0x14000  | 4K    |        |
| ota_0                     | app   | ota_0    | 0x20000  | 960K  |        |
| ota_1                     | app   | ota_1    | 0x110000 | 960K  |        |


## Requirements


## Notes