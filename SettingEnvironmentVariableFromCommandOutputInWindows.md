
## On command line 
for /f "delims=" %a in ('C:\location\date.exe -n 1 -X 22') do set DATE_TIME=%a

## In batch file 
for /f "delims=" %%a in ('C:\location\date.exe -n 1 -X 22') do @set DATE_TIME=%%a 

## Running the commands given on argument 
echo %*
%* 
