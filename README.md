OPENSOURCE

ОТРЫТОЕ ПРОГГРАММНОЕ ОБЕСПЕЧЕНИЕ

ИСПОЛЬЗОВАТЬ НА СВОЙ СТРАХ И РИСК

АВТОР ЗА ЛЮБЫЕ ПОСЛЕДСТВИЯ ИСПОЛЬЗОВАНИЯ ПРОГРАММЫ ОТВЕТСТВЕННОСТИ НЕ НЕСЁТ

ПРОГРАММА ПРЕДОСТАВЛЯЕТСЯ КАК ЕСТЬ БЕЗ КАКИХ ЛИБО ГАРАНТИЙ НА КОРРЕКТНУЮ ИЛИ ПРАВИЛЬНУЮ РАБОТУ 


TO USE APPROPRIATELY YOU MUST CHANGE IMAGES EVERY USE OF THIS HIT
Для того чтобы использовалось по назначению необходимо переопределить картинки каждое использование этого фирма

DELETE BOTH IMAGE RECOGNITION BLOCKS
Удалите оба куска кода с распознаванием картинки
ScreenCapture.......
FindImagePos>.........
If>NumFou...
  goto>start
En....

ScreenCapture.......
FindImagePos>.........
If>NumFou...
  goto>start
En....

REPLACE FIRST BLOCK with 2.bmp image captured on screen
Замените первый блок распознавания картинок на картинку 2.bmp схваченную на экране при помощи функции в программе macro schedule recorder
Script->Image Recognition-> Find position->What to look->Capture An Image->ВЫИГРЫШ->Where to look->Search within rectangle->Draw->Select Area bmp within->What to do left Click->Where Center of image->Advanced correlation 0.6 worked in my tests WaitScreenImageTimeout 1 sec worked out in my tests > insert code 

change 
 MouseMove>{%XArr_0%+678},{%YArr_0%+580}
  LClick
to goto->start
на goto->start

REPLACE SECOND BLOCK with 1.bmp image captured on screen
Замените второй блок распознавания картинок на картинку 1.bmp схваченную на экране при помощи функции в программе macro schedule recorder
Script->Image Recognition-> Find position->What to look->Capture An Image->ЗАСЧИТАНО->Where to look->Search within rectangle->Draw->Select Area bmp within->What to do left Click->Where Center of image->Advanced correlation 0.6 worked in my tests WaitScreenImageTimeout 1 sec worked out in my tests -> insert code 

change 
 MouseMove>{%XArr_0%+678},{%YArr_0%+580}
  LClick
to goto->start
на goto->start


Label>start
Random>5,randomresult

let>halfbsizex=44
let>line9=847

Wait>0.179

MouseMove>1014,629

LClick

MouseMove>1014,630

Wait>0.327

LClick

Wait>0.5
let>grabbed=0

ScreenCapture>739,569,945,596,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_2.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>grabbed=1
  goto>btc
Endif

ScreenCapture>743,570,946,597,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_4.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  goto>start
Endif

Label>btc
Wait>3.5179
let>raise = 0
ScreenCapture>1069,516,1107,541,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_7.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Let>raise=1
Endif


ScreenCapture>1064,515,1107,542,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_6.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Let>raise=3
Endif

ScreenCapture>1067,517,1104,543,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_8.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Let>raise=2
Endif

ScreenCapture>1066,520,1102,540,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_9.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Let>raise=1
Endif

Message grabbed %grabbed%
If>grabbed>0.5
  goto>raiseFixed
Endif

Label>resetRaise
MouseMove>949,630
LClick
Wait>0.5179

MouseMove>908,630
LClick
Wait>0.5179

goto>setLines

Label>raiseFixed
MouseMove>913,630

If>raise>0
  LClick
  Wait>0.5179
Endif

Let>raise=raise-1

If>raise>0
  LClick
  Wait>0.5179
Endif

Let>raise=raise-1

If>raise>0
  LClick
  Wait>0.5179
Endif

Let>raise=raise-1

If>raise>0
  LClick
  Wait>0.5179
Endif

Let>raise=raise-1

If>raise>0
  LClick
  Wait>0.5179
Endif

//Let>raise=raise-1


Label>setLines

Let>halfbsizex=halfbsizex*randomresult

Let>line9=line9-halfbsizex

MouseMove>line9,630

LClick

Wait>0.5179

goto>start



