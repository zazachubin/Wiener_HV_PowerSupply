WIENER (MPOD Mini crate) multi-channel high and low voltage power supply system controller and data logger

OS Linux, Windows 10
Terminal commands :
------------------------------------------------- SET --------------------------------------------------------
snmpset -Oqv -v 2c -m +WIENER-CRATE-MIB -c guru 192.168.0.250 outputVoltage.u0 F 60
snmpset -Oqv -v 2c -m +WIENER-CRATE-MIB -c guru 192.168.0.250 outputCurrent.u0 F 0.000001
snmpset -Oqv -v 2c -m +WIENER-CRATE-MIB -c guru 192.168.0.250 outputSwitch.u0 i 1
snmpset -Oqv -v 2c -m +WIENER-CRATE-MIB -c guru 192.168.0.250 outputTripTimeMaxCurrent.u0 i 3000
------------------------------------------------- GET ---------------------------------------------------------
snmpget -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputVoltage.u0
snmpget -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputMeasurementSenseVoltage.u0
snmpget -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputMeasurementCurrent.u0
snmpget -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputSwitch.u0
snmpget -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputTripTimeMaxCurrent.u0
snmpget -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputStatus.u0
-------------------------------------------------- General -----------------------------------------------------
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputName
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputVoltage
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputMeasurementSenseVoltage
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputSwitch
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputVoltageRiseRate
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputStatus
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputTripTimeMaxCurrent
snmpwalk -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputMeasurementCurrent

snmpgetx -Oqv -v 2c -m +WIENER-CRATE-MIB -c guru 192.168.0.250 outputMeasurementCurrent.u8

snmpgetx -Oqv -v 2c -m +WIENER-CRATE-MIB -c public 192.168.0.250 outputMeasurementCurrent.u100