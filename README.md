Label>start
Wait>0.179
MouseMove>1014,629
LClick
MouseMove>1014,630
Wait>0.327
LClick
Wait>0.5

ScreenCapture>763,570,954,595,%TEMP_DIR%\screenrect.bmp

FindImagePos>%BMP_DIR%\image_2.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
  goto>start
Endif

ScreenCapture>783,574,931,595,%TEMP_DIR%\screenrect.bmp
FindImagePos>%BMP_DIR%\image_1.bmp,%TEMP_DIR%\screenrect.bmp,0.6,1,XArr,YArr,NumFound,CCOEFF
If>NumFound>0
   goto>start
Endif

Wait>3.5179 
MouseMove>913,630
LClick
Wait>0.5179
goto>start



