# stm32-defects
A list of the known STM32 HAL defects

## Preface
Repository URL : https://github.com/suikan4github/stm32-defects

## Defects

### D001 Nucleo F722ZE wrong clock configuration
| Item                    | Description   |
| ----------------------- | ------------- |
| Affected device         | Nucleo F722ZE |
| Last reproduced CubeIDE | 1.3.0         | 
| Resolved CubeIDE        | -             |
| Last reproduced FW      | F7 V1.16.0    | 
| Resolved FW             | -             |
| Sample program          | -             |
| Reported                | ST Community  |

In the CubeIDE output project, the default input clock frequency of the Nucleo F722ZE is wrong. 

It is configured as 25MHz, while it should be 8MHz. 

This seems to be the problem of the code generator, rather than the embedded firmware. 

![Clock Configuration](img/2020-03-06_07-16.png)

### D002 STM32F7 HAL_EXTI_SetConfigLine() runtime error

| Last reproduced FW | | 
| Resolved FW | |

### D003 STM32G0 HAL_GPIO_EXTI_Callback() incompatibility
### D004 STM32H7 HAL_I2C_Master_Transmit_IT() runtime bug
### D005 STM32L1 HAL_I2C_Master_Sequential_Transmit_IT() incompatibility
### D006 STM32L1 HAL_EXTI wrong configuration


## Resolved

## Author
Seiichi Horie

## License
[MIT license](LICENSE)
