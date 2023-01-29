//OPENSOURCE

//ОТРЫТОЕ ПРОГГРАММНОЕ ОБЕСПЕЧЕНИЕ

//ИСПОЛЬЗОВАТЬ НА СВОЙ СТРАХ И РИСК

//АВТОР ЗА ЛЮБЫЕ ПОСЛЕДСТВИЯ ИСПОЛЬЗОВАНИЯ ПРОГРАММЫ ОТВЕТСТВЕННОСТИ НЕ НЕСЁТ

//ПРОГРАММА ПРЕДОСТАВЛЯЕТСЯ КАК ЕСТЬ БЕЗ КАКИХ ЛИБО ГАРАНТИЙ НА КОРРЕКТНУЮ ИЛИ ПРАВИЛЬНУЮ РАБОТУ 

//НЕ ИСПОЛЬЗУЙТЕ ТЕКСТ ОТСЮДА НИГДЕ ДЛЯ СВОЕГО - ЖЕ СПОКОЙСТВИЯ

//КОРРЕКТНУЮ УСТАНОВКУ КАРТИНОК МОЖНО ПРОВЕРИТЬ ПРИЗНАКОМ ОТОБРАЖЕНИЯ ИХ МИНИАТЮР ПРЯМО В ОКНЕ mouse scheduler 15 
//![alt text](https://iili.io/H0DVxa9.md.png)

//TO USE APPROPRIATELY YOU MUST CHANGE IMAGES EVERY USE OF THIS HIT
//Для того чтобы использовалось по назначению необходимо переопределить картинки каждое использование этого фирма

//DELETE BOTH IMAGE RECOGNITION BLOCKS
//Удалите оба куска кода с распознаванием картинки
//ScreenCapture.......
//FindImagePos>.........
//If>NumFou...
//  goto>start
//En....

//ScreenCapture.......
//FindImagePos>.........
//If>NumFou...
//  goto>start
//En....

//REPLACE FIRST BLOCK with 2.bmp image captured on screen
//Замените первый блок распознавания картинок на картинку 2.bmp схваченную на экране при помощи функции в программе macro schedule recorder
//Script->Image Recognition-> Find position->What to look->Capture An Image->ВЫИГРЫШ->Where to look->Search within rectangle->Draw->Select Area bmp within->What to do left Click->Where Center of image->Advanced correlation 0.6 worked in my tests WaitScreenImageTimeout 1 sec worked out in my tests > insert code 

//change 
// MouseMove>{%XArr_0%+678},{%YArr_0%+580}
//  LClick
//to goto->start
//на goto->start

//REPLACE SECOND BLOCK with 1.bmp image captured on screen
//Замените второй блок распознавания картинок на картинку 1.bmp схваченную на экране при помощи функции в программе macro schedule recorder
//Script->Image Recognition-> Find position->What to look->Capture An Image->ЗАСЧИТАНО->Where to look->Search within rectangle->Draw->Select Area bmp within->What to do left Click->Where Center of image->Advanced correlation 0.6 worked in my tests WaitScreenImageTimeout 1 sec worked out in my tests -> insert code 

//change 
// MouseMove>{%XArr_0%+678},{%YArr_0%+580}
//  LClick
//to goto->start
//на goto->start

//=========================================================COPY BELOW===========КОПИРОВАТЬ НИЖЕ================================================================
// C:\Users\PC\AppData\Local\Temp\msrBB46.scp
// Recorded on  воскресенье, Январь 29, 2023, at 10:54 AM

//Recorded Events
Let>WW_TIMEOUT=5
CapsOff

WaitWindowOpen>Игровой автомат Book of Ra ?? (Книжки, Бук оф Ра) играть бесплатно в казино Вулкан Россия - Google Chrome
MoveWindow>Игровой автомат Book of Ra ?? (Книжки, Бук оф Ра) играть бесплатно в казино Вулкан Россия - Google Chrome,-8,-8
ResizeWindow>Игровой автомат Book of Ra ?? (Книжки, Бук оф Ра) играть бесплатно в казино Вулкан Россия - Google Chrome,1616,886
Wait>0.156
MouseMove>1030,624
Wait>2.066
LClick
Wait>0.203

Let>c=0
Label>start
//продаю exe для вашего windows pc произведу настройку и установку программного обеспечения бота для любых 
//слотовых аппаратов и других компьютерных игр обращаться telegram +79104784319 

//перед запуском скрипта в macro scheduler скопируйте все картинки
//по соответствующим путям файлов указанные в строках
//с инструкцией FindImagePos....c:\book of ra....
//если надо - поменяйте
//copy all images from repository to corresponding file path
//i.e. c:\book of ra\won.bmp 103pix 18pix
//c:\book of ra\win.bmp 91pix 17pix
//c:\book of ra\bet10.bmp 26pix 21pix
//c:\book of ra\bet20.bmp 24pix 18pix
//c:\book of ra\bet50.bmp 25pix 20pix
//c:\book of ra\bet200.bmp 23pix 20pix

//DeleteFile>c:\book of ra\screenrectwin.bmp
//DeleteFile>c:\book of ra\screenrectwon.bmp
//DeleteFile>c:\book of ra\screenrect1.bmp
//DeleteFile>c:\book of ra\screenrect2.bmp
//DeleteFile>c:\book of ra\screenrect3.bmp
//DeleteFile>c:\book of ra\screenrect4.bmp



let>c=c+1
If c==10
  ScreenCapture>584,578,900,592,C:\Users\PC\Desktop\shots\%c%.bmp
  let>c=0
Endif

GetRectCheckSum>584,556,695,592,clip
//Message %clip%
//check summ credit 9 fields - length empty
Let>max=764753173

Let>bool==
Let>condition=%clip%%bool%%max%
Let>Test={condition}

If>Test=TRUE
  MouseMove>512,617
  LClick
  Wait>0.15179
  LUp
  Wait>12
  MouseMove>1032,589
  Wait>0.12
  LClick
  Wait>0.15179
  LUp
  Let>SK_DELAY=0.1
  SendText>Book of ra
  Wait>1.12
  MouseMove>495,649
  LClick
  Wait>0.15179
  LUp
  Wait>11
  MouseMove>495,652
  LClick
  Wait>0.15179
  LUp
  Wait>1
  LClick
  Wait>0.15179
  LUp
  Wait>1
  LClick
  Wait>0.15179
  LUp
  Wait>1
  LClick
  Wait>0.15179
  LUp
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
Wait>0.15179
LUp
Wait>0.5179

Wait>0.5179

MouseMove>1014,629

LClick
Wait>0.15179
LUp
MouseMove>1014,630

Wait>0.05127

LClick
Wait>0.15179
LUp
Wait>1.75

let>grabbed=0

ScreenCapture>733,570,953,594,C:\book of ra\screenrectwin.bmp
//Find and Left Click Center of
FindImagePos>C:\book of ra\win.bmp,C:\book of ra\screenrectwin.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  goto>start
Endif


Wait>0.15

ScreenCapture>733,570,953,594,C:\book of ra\screenrectwon.bmp
//Find and Left Click Center of 
FindImagePos>C:\book of ra\won.bmp,C:\book of ra\screenrectwon.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  let>grabbed=1
  goto>btc
Endif

goto>start

Label>btc

Let>raiseNum=0

If>NumFound>0
  MouseMove>XArr_0,YArr_0
  LClick
Endif
//6 1 2 5 lower aggressive
//1 5 7 1 high aggressive
ScreenCapture>1062,520,1102,542,C:\book of ra\screenrect10.bmp
//Find and Left Click Center of 
FindImagePos>C:\book of ra\image_10.bmp,C:\book of ra\screenrect10.bmp,0.7,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  //MessageModal "current bet x10 grabbed" %Grabbed%
  let>raiseNum=1
Endif

ScreenCapture>1077,522,1105,541,C:\book of ra\screenrect20.bmp
//Find and Left Click Center of 
FindImagePos>C:\book of ra\image_11.bmp,C:\book of ra\screenrect20.bmp,0.5,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  //Message "current bet x20 grabbed" %Grabbed%
  let>raiseNum=5
Endif

ScreenCapture>1077,520,1102,542,C:\book of ra\screenrect50.bmp
//Find and Left Click Center of 
FindImagePos>C:\book of ra\image_12.bmp,C:\book of ra\screenrect50.bmp,0.7,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  //MessageModal "current bet x50 grabbed" %Grabbed%
  let>raiseNum=7
Endif

ScreenCapture>1060,520,1104,542,C:\book of ra\screenrect200.bmp
//Find and Left Click Center of 
FindImagePos>C:\book of ra\image_13.bmp,C:\book of ra\screenrect200.bmp,0.7,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  //MessageModal "current bet x200 grabbed" %Grabbed%
  let>raiseNum=1
Endif


//Message grabbed %grabbed%
If>grabbed>0.5
  //MessageModal "raisefixed raiseNum" %raiseNum% " grabbed " %grabbed%
  goto>raiseFixed
Endif

Label>resetRaise

MouseMove>949,630

LClick
Wait>0.15179
LUp

Wait>0.75179

MouseMove>908,630

LClick
Wait>0.15179
LUp

Wait>0.75179

goto>start

Label>raiseFixed

MouseMove>913,630

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.75179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.5179
Endif

let>raiseNum=raiseNum-1

If>raiseNum>0
  LClick
  Wait>0.15179
  LUp
  Wait>0.5179
Endif

goto>start

