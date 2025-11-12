# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**
```
#include<reg51.h> void main(void)
{
TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;
SCON=0X50; TR1=1;
while(1)
{ SBUF='A';
while(TI==0); TI=0;
}
}
```
**(ii)	Serial port to Transfer a Message**
```
#include<reg51.h> void main(void)
{
unsigned char msg[]="Programming 8051"; unsigned char i;
TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;
SCON=0X50; TR1=1;
for (i=0; i<17;i++)
{
SBUF= msg[i]; while(TI==0); TI=0;
}
while(1);
}
``` 
**OUTPUT:**
<img width="1883" height="1044" alt="Screenshot 2025-11-11 204939" src="https://github.com/user-attachments/assets/0f60873f-8ffd-4cf0-adfb-0417397fc8cb" />
<img width="1903" height="774" alt="Screenshot 2025-11-11 210318" src="https://github.com/user-attachments/assets/ac417b80-fbe7-4ddc-b488-de08a8e09e61" />

**Result:**
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
