# YModemForAndroid
A ymodem implementation that suitable for android and BLE 

```
 * MY YMODEM IMPLEMTATION
 * *SENDER: ANDROID APP *------------------------------------------* RECEIVER: BLE DEVICE*
 * HELLO BOOTLOADER ---------------------------------------------->*
 * <---------------------------------------------------------------* C
 * SOH 00 FF filename0fileSizeInByte0MD5[90] ZERO[38] CRC CRC----->*
 * <---------------------------------------------------------------* ACK C
 * STX 01 FE data[1024] CRC CRC ---------------------------------->*
 * <---------------------------------------------------------------* ACK
 * STX 02 FF data[1024] CRC CRC ---------------------------------->*
 * <---------------------------------------------------------------* ACK
 * ...
 * ...
 * <p>
 * STX 08 F7 data[1000] CPMEOF[24] CRC CRC ----------------------->*
 * <---------------------------------------------------------------* ACK
 * EOT ----------------------------------------------------------->*
 * <---------------------------------------------------------------* ACK
 * SOH 00 FF ZERO[128] ------------------------------------------->*
 * <---------------------------------------------------------------* ACK
 * <---------------------------------------------------------------* MD5_OK
 ```