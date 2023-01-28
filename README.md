# BOOKOFRASPINNER OPENSOURCE
Скрипт настраивающий Macro Scheduler 15.0.21e на отмывку бонусных баллов в vulkancasino-games.ru
Label>Spinfast
let>z=0
let>b=0
Wait>0.179
MouseMove>1049,727
LClick
//....AND STOP FAST
MouseMove>1049,727
Wait>0.327
LClick
//WAIT ROLL GAMBLE OR TAKE 3535090
//WAIT ROLL game over 3601911
Label>wait
Wait>0.5
GetPixelColor>711,609,outColor
GetPixelColor>899,677,a
//Message>WINGAMBLEGAMEOVER : %outColor%
If>nColor==3535090
  goto>notwait
ELSE If>a==203091
  goto>bmc
ELSE If>a==104406
  goto>notwait
ELSE
  goto>wait
Endif
Label>notwait
Wait>2.5179
goto>Spinfast

Label>bmc
Wait>1.5179

ScreenCapture>782,654,913,685,%TEMP_DIR%\screenrect.bmp
FindImagePos>%BMP_DIR%\image_3.bmp,%TEMP_DIR%\screenrect.bmp,0.5,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Message>MESSAGE
  goto>Spinfast
Endif

MouseMove>930,718
LClick
Wait>2.5179
goto>Spinfast
