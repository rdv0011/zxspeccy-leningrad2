# zxspeccy-leningrad2

## First program I have modified for ZX Spectrum
  It was the text game named 'Dictator' created by dKTroniks [Dictator game cover](http://zxspectrum.online/zxcover/dictator.jpg). To enrich the game I have created basic operations with the bank account to make extra money. To get to the additional screen with the account operations press the button "B" while staying in the main menu which is shown on screenshot:
 <img src="dictator-main-screen.png?sanitize=true&raw=true" />
 The following is the title screen of the app:
 <img src="dictator-initial-screen.png?sanitize=true&raw=true" />
 The additional screen with bank operations looks like this:
 <img src="dictator-account-screen.png?sanitize=true&raw=true" />
 
 The modified game itself can be found in this repo in the file: [dictator in TZX format](dictator-mod-by-dry.tzx). To play it try one of the great online emulator like the following: http://jsspeccy.zxdemo.org

 The following is the core code of the modification:
```basic
839 PRINT AT 20,3;" (OPERACII S BANKOM-""B"") "
842 BRIGHT 0:RETURN 
843 CLS :INK 4:PAPER 2:FOR k=1 TO 20:PRINT AT k,0;"$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$":NEXT k:INK 3:FOR k=0 TO 21:PRINT AT k,0;"J":NEXT k:FOR k=0 TO 21:PRINT AT k,31;"j":NEXT k:PRINT AT 0,1;"JJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJ";AT 21,0;"JJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJ":BRIGHT 1:INK 7:PRINT FLASH 1;AT 2,6;"Hto V{ xotite?:";FLASH 0;AT 4,4;"1.Procent{";AT 14,4;"Procent{:";prp;AT 16,4;"V KAZNAHE_STVE:";bk;AT 18,4;"Shet v banke:";sw;AT 6,4;"2.Vs& summu";AT 8,4;"3.Polovinu summ{";AT 10,4;"4.Polovinu procentov";AT 12,2;"Najmite nujnu& klaviqu(1-4)";AT 20,2;"V{xod-v"
844 IF INKEY$ ="1" THEN GO TO 849
845 IF INKEY$ ="2" THEN GO TO 850
846 IF INKEY$ ="3" THEN GO TO 851
847 IF INKEY$ ="4" THEN GO TO 852
848 GO TO 858
849 LET bk=bk+prp:GO TO 853
850 LET bk=bk+sw:GO TO 854
851 LET bk=bk+INT (sw/2):GO TO 855
852 LET bk=bk+INT (prp/2):LET sw=sw-INT (prp/2):LET prp=INT (prp/2):CLS :INK 3:RETURN 
853 LET sw=sw-prp:LET prp=0:CLS :INK 3:RETURN 
854 LET sw=0:CLS :INK 3:RETURN 
855 LET sw=INT (sw/2):CLS :INK 3
857 RETURN 
858 IF INKEY$ ="b" THEN CLS :INK 3:RETURN 
859 GO TO 844
```
## Front view of the case
<img src="front.jpeg?sanitize=true&raw=true" />

## Back view of the case
<img src="back.jpeg?sanitize=true&raw=true" />

## Keyboard disassembled
<img src="keyboard-disassembled.jpeg?sanitize=true&raw=true" />

## Main board with CPU
<img src="main-board-cpu.jpeg?sanitize=true&raw=true" />

## Main board closer look
<img src="main-pcb.jpeg?sanitize=true&raw=true" />

## Power supply closer view
<img src="power-supply.jpeg?sanitize=true&raw=true" />

## Sound system closer view
<img src="sound-system.jpeg?sanitize=true&raw=true" />

## Tape recorder to load/save software
<img src="tape-recorder.jpeg?sanitize=true&raw=true" />
