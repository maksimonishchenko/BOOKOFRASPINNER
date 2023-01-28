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

ScreenCapture>584,574,697,595,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_15.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  MouseMove>512,617
  LClick
  Wait>10
  MouseMove>1032,589
  LClick
  Press b
  Press o
  Press o
  Press k
  Press Space
  Press o
  Press f
  Press Space
  Press r
  Press a
  MouseMove>1061,594
  Wait>1
  MouseMove>504,646
  LClick
  Wait>12
  //nominal
  MouseMove>496,654
  LClick
  Wait>1
  LClick
  Wait>1
  LClick
  Wait>1
  LClick
  Wait>1
Endif




Label>setLines

let>halfbsizex=44

let>line9=847

Random>5,randomresult

Let>halfbsizex=halfbsizex*randomresult

Let>line9=line9-halfbsizex

MouseMove>line9,630

LClick

Wait>0.5179

Wait>0.5179

MouseMove>1014,629

LClick

MouseMove>1014,630

Wait>0.2327

LClick

Wait>1.75

let>grabbed=0

ScreenCapture>743,570,946,597,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_4.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  goto>start
Endif

Wait>0.15

ScreenCapture>739,569,945,596,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_2.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>grabbed=1
  goto>btc
Endif


goto>start

Label>btc

Wait>3.5179

Let>raiseNum=0

ScreenCapture>1066,522,1089,542,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_10.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>raiseNum=6
Endif
//1 5 7 1 to raise bet row sequence 7 6 4 1 to low  
ScreenCapture>1064,523,1090,543,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_11.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>raiseNum=6
Endif


ScreenCapture>1075,520,1090,541,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_14.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>raiseNum=4
Endif

ScreenCapture>1062,522,1081,541,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>%BMP_DIR%\image_13.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>raiseNum=1
Endif


//Message grabbed %grabbed%
If>grabbed>0.5
  goto>raiseFixed
Endif

Label>resetRaise

MouseMove>949,630

LClick

Wait>0.75179

MouseMove>908,630

LClick

Wait>0.75179

//goto>setLines

Label>raiseFixed

MouseMove>913,630

//Let>raiseNum=raiseNum-1
//Message %raiseNum%
If>raise>0
  LClick
  Wait>0.75179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.5179
Endif



//Let>raiseNum=raiseNum-1

//place set lines diagonally random shift...


//dedicated to Sergey Genadyevich Verchenko
goto>start



