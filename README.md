# Cobol-Date-Routines
GnuCOBOL date and time routines
Here are some programs that may help someone that needs a few date routines. I have them as executables to run on command line or in a script. I also have them as callable Subroutines from GnuCobol executables. 
The programs and purpose are listed below. They also have more information in the program as comments.

-
getdatex  -  batch (executable) program that will add a number argument to the current date and give you the new date. If you want to know the date from 31 days from now just execute it with: getdatex 31 

getdatey  -  batch (executable) program that will subtract a number argument from the current date and give you the new date. If you want to know the date for 31 days ago from now just execute it with: getdatey 31

-
getdatez  -  batch (executable) program that will allow you to enter a date, add or subtract, and the number days, then it will give you the new date. This program will add or subtract a number of days for the gregorian date that is passed to this program and return the given new date:  getdatez 24351225 - 600   .  Will take the entered date and subtract 600 days and give you the new date.  You can add or subtract.

sbrdatex  -  is a callable subroutine that does the same as getdatex. 

-
sbrdatey  -  is a callable subroutine that does the same as getdatey. 

sbrdatez  -  is a callable subroutine that does the same as getdatez. 

-
weekday   -  batch (executable) program that will return the name of the Day of the week for a valid gregorian date passed as argument. To find day of week:  weekday 20240212  

sbrwkday  -  is a callable subroutine that does the same as weekday.

-
daysdiff  -  batch (executable) program that will return the nubmer of days bewteen two date:  daysdiff 20010101 20240101

sbrdydff  -  is a callable subroutine that does the same as daysdiff.

-
secsbdt2  -  batch (executalbe) program that will return the number of seconds between two dates and times. ccyymmdd hhmmss ccyymmdd hhmmss

sbrsbdt2  -  is a callable subroutine that does the same as secsbdt2. 

-
Notes:  date limits are, minimum 16010101  maximum 99991231.  time must conform to 24 hour clock min 000001 max 235959  
The biggest possible number of days: daysdiff 16010101 99991231 = 3067670 
The biggest time between dates: secsbdt2 16010101 000001 99991231 235959 = +0000000000000000000265046774398 

And finally some Epoch information: 
The z/Architecture®, ESA/390, and System/370 architectures established the epoch for the TOD clock as January 1, 1900, 0 a.m. GMT. 
Apple macOS considers its Epoch Time as starting from January 1, 1904.
Microsoft Windows considers its Epoch Time as starting from January 1, 1601.
Unix and Linux Systems consider their Epoch Time as starting from January 1, 1970. This time is also referred to as Unix Time and Unix Epoch.
--
The Unix year problem, also known as the Year 2038 problem, is a time formatting bug in computer systems that represent times after 03:14:07 UTC on 19 January 2038. This problem exists in systems that measure Unix time and store it in a signed 32-bit integer.2 Many Unix and other major operating systems moved from signed 32-bit integers to signed 64-bit integers to represent the epoch count. 
-

 
