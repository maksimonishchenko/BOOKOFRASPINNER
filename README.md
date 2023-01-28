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
//перед запуском скрипта в macro scheduler скопируйте все картинки
//по соответствующим путям файлов указанные в строках
//с инструкцией FindImagePos....c:\book of ra....
//если надо - поменяйте
//copy all images from repository to corresponding file path
//i.e. c:\book of ra\won.bmp 
//c:\book of ra\win.bmp
//c:\book of ra\bet10.bmp
//c:\book of ra\bet20.bmp
//c:\book of ra\bet50.bmp
//c:\book of ra\bet200.bmp


GetRectCheckSum>584,578,695,592,clip
//check summ credit 9 fields - length empty
Let>max=147434936

Let>bool=>
Let>condition=%clip%%bool%%max%
Let>Test={condition}

If>Test=TRUE
 //MessageModal>greater
Else
 MouseMove>512,617
  LClick
  Wait>12
  MouseMove>1032,589
  Wait>0.12
  LClick
  Let>SK_DELAY=0.1
  SendText>Book of ra
  Wait>1.12
  MouseMove>495,649
  LClick
  Wait>11
  MouseMove>495,652
  LClick
  Wait>1
  LClick
  Wait>1
  LClick
  Wait>1
  LClick
  Wait>1
EndIf

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

Wait>0.05127

LClick

Wait>1.75

let>grabbed=0

ScreenCapture>760,578,912,594,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of
FindImagePos>C:\book of ra\win.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Message Win
  goto>start
  LClick
Endif





Wait>0.15

ScreenCapture>740,573,952,597,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of 
FindImagePos>C:\book of ra\won.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  goto>btc
Endif

goto>start

Label>btc

Wait>3.5179

Let>raiseNum=0


ScreenCapture>1067,522,1103,541,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of
FindImagePos>C:\book of ra\bet10.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Message "current bet x10 grabbed" %Grabbed%
  let>raiseNum=6
Endif

ScreenCapture>1077,523,1103,540,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of
FindImagePos>C:\book of ra\bet20.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Message "current bet x20 grabbed" %Grabbed%
  raiseNum=6
Endif


ScreenCapture>1077,522,1104,541,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of
FindImagePos>C:\book of ra\bet50.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Message "current bet x50 grabbed" %Grabbed%
  let>raiseNum=4
Endif

ScreenCapture>1064,522,1090,542,%TEMP_DIR%\screenrect.bmp
//Find and Left Click Center of
FindImagePos>C:\book of ra\bet200.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  Message "current bet x200 grabbed" %Grabbed%
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

goto>start

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

goto>start

//dedicated to 2pac Amaru Shakur 



