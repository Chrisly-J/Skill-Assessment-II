# Skill-Assessment-II


## AIM:
1.Write an assembly language program in 8051 to generate a 5 ms delay using Timer 1 in Mode 1 and toggle an LED connected to Port 1.7 continuously.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software

## PROGRAM:
```
ORG 0000H
MOV TMOD, #10H
HERE:
MOV TH1, #0ECH
MOV TL1, #78H
SETB TR1
WAIT:
JNB TF1, WAIT
CLR TR1
CLR TF1
CPL P1.7
SJMP HERE
END
```


### OUTPUT:
<img width="500" height="500" alt="Screenshot 2025-10-24 202319" src="https://github.com/user-attachments/assets/d9d0bde8-c24a-4fe7-915e-e632fbb13d2c" />


### RESULT:
Thus an assembly language program in 8051 to generate a 5 ms delay using Timer 1 in Mode 1 and toggle an LED connected to Port 1.7 continuously using keil was done and shown the output.
