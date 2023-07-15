# ESP32 tgBot
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) 
![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)

Разработано программно-аппаратное решение отображения текущей освещённости в помещении и управления включением подсветки. Решение основано на esp32, плате nucleo stm32f411RE, фоторезисторе.
________
## Модель работы  
Общая схема работы: *фоторезистор → stm32f411re → UART → esp32 → tgBot*.  
:white_check_mark: В STM32 производится расчет освещенности в lux.  
:white_check_mark: STM32 по UART передает показание освещенности на ESP32.  
:white_check_mark: Управление светодиодом и передача показаний от esp32 в чат с тг-ботом осуществляется по запросу в чате.  
___
## Заметки
:one: Использована библиотека для работы с Telegram-ботом   
[https://github.com/witnessmenow/Universal-Arduino-Telegram-Bot?ysclid=lk3nk88px9625161661](https://github.com/witnessmenow/Universal-Arduino-Telegram-Bot?ysclid=lk3nk88px9625161661)  
:two: ESP32 использует UART2, STM32 использует UART1 для общения  
:three: Настройки WI-FI и тг-бота вынесены в setup.h :key:  
:four: Фоторезистор подключен к ADC1 STM32 через делитель напряжения 10кОм
