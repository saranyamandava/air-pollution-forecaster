# air-pollution-forecaster

The 'data\daily_clean_full.csv' file contains the daily data of the weather parameters and air pollution (pm10) parameters. This is the cleaned merge of the 'daily_pm10.xlsx' and the 'hourly_lorinc_2011-2018.xls'

datasources:

https://rp5.ru/Weather_archive_in_Budapest,_Lorinc_(airport)

http://www.levegominoseg.hu/automata-merohalozat?city=2

'daily_pm10.xlsx': measured PM10 in Budapest, 12 stations We made forecast only for one point: Budapest, Teleki square airquality station.

'hourly_lorinc_2011-2018.xls': Budapest Pestszentlőrinc weather station history - measurement

'data\daily_clean_full.csv' columns:
temp_avr: average temperature based on hourly averages - ºC
temp_max: maximum hourly temperature during the day - ºC
temp_min: minimum hourly temperature during the day - ºC
pres: mean sea level pressure - Hpa
u, v: meridional and zonal component of wind (daily averages) - m/s
prec: precipitation - mm (In station data we have 6h, 12h and 24h totals, and not hourly data. Some of the periods are missing. For simplicity in the cleaned data we use the largest of the above numbers, this way the order of magnitude of the precipitation remains, but the 24h total isn't precise. Later with better data this can be corrected.)
datetime: datetime - UTC
station name: daily average pm10 concentration of station - μg/m3
