![MIKES DATA WORK GIT REPO](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_01.png "Mikes Data Work")        

# Break the 8192 SQL Character Limit
**Post Date: May 1, 2014**        



## Contents    
- [About Process](##About-Process)  
- [SQL Logic](#SQL-Logic)  
- [Build Info](#Build-Info)  
- [Author](#Author)  
- [License](#License)       

## About-Process

<p>Occassionaly you'll run into a point where you aren't getting enough characters in the Text output of SSMS. Fortunately; there's a quick thing you can do (within TSQL), and you don't have to mess around with setting the results to Text Output either through the SSMS GUI, or CTRL+T.
You simply add a single line at the end of your statement.</p>      


## SQL-Logic
```SQL
FOR XML PATH(''), TYPE
```	

You can do this after any statement and see what kind of results you get. They will be displayed in another Tab. You'll get the XML syntax with that but there's another way you can do it below.
Example:



## SQL-Logic
```SQL
use master;
set nocount on
select
name
from
sys.databases
for xml path(''), type
```

![Run Query](https://mikesdatawork.files.wordpress.com/2014/05/image001.jpg "Run Query")
 
Or… If you want the results in straight text without all the XML syntax ( that you can simply copy and paste into something else ), you can put the results into a variable, and select the variable SELECT @MyVariable, and the xml path will list only text after you click on the link. Like so…
![Get XML Path](https://mikesdatawork.files.wordpress.com/2014/05/00558.jpg "Get XML Path")
 


[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

[![Gist](https://img.shields.io/badge/Gist-MikesDataWork-<COLOR>.svg)](https://gist.github.com/mikesdatawork)
[![Twitter](https://img.shields.io/badge/Twitter-MikesDataWork-<COLOR>.svg)](https://twitter.com/mikesdatawork)
[![Wordpress](https://img.shields.io/badge/Wordpress-MikesDataWork-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)


## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Mikes Data Work](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_02.png "Mikes Data Work")

