# Данная программа позволяет нарисовать месторасположения базовых станций LTE на карте Google Earth Pro на основе широты и долготы с учётом азимутов секторов.
Азимуты представлены с точностью 90 градусов. Всего было подготовлено 4 картинки: 
1) 0-90 градусов
2) 90-180 градусов
3) 180-270 градусов
4) 270-360 градусов
С помощью данных картинок на карте будут отмечены азимуты секторов базовой станции. Необходимо ознакомиться с эксельным файлом, где указаны столбцы. Именно по названию столбцов программа будет находить нужные столбцы и подгружать оттуда данные.
Самые важные столбцы:
['Cell Name', 'Longitude', 'Latitude', 'Azimuth']
Если вы будете запускать данную программы на основе своей таблицы, то необходимо, чтобы названия столбцов назывались точно также. В столбце Cell Name - указывается название соты, в столбце Longitude - долгота, Latitude - широта, в Azimuth - азимут сектора.
После того, как программа обработает данные, она предоставит файл в формате .kml. При открытии которого на карте гугл будут отображаться базовые станции с указанием азимутов секторов с точностью до 90 градусов.
Точность азимутов может быть увеличина, если сделать разбивку не через каждые 90 градусов, а например, через каждые 45. 


Draw LTE ENB's location and azimuth based on longitude, latitude, azimuth(optinal) in Google Earth Pro. 
Full guide you can find in read_me.txt
This program can help to prepare a KML file with the location and azimuth of lte base station using Longitude and Latitude and Azimuth(optional).
You can use this KML file to check location and azimuth of eNB base station. 
There are some important dependencies. 
Add a path for azimuth's picures:
1) Download all files
2) Open the folder "picures" and save the path of its location on your PC. For example: C:/Users/local/Downloads/pictures

3) Open file header_styles.txt and find all string with <href>C:/Users/garbu/Downloads/</href>,
then replace path with your path from previous step like this: "your_path"/empty1.png, "your_path"/0_90.png,
but you shoudn't touch last part with picture name /empty1.png, 0_90.png, 90_180.png, 180_270.png, 270_360.png

4) Check the file 'test_list_1000.xlsx' with enb information or take your file, BUT you should add column's name according to mines:
  dfcp.columns:
    Index(['Cell Name', 'Longitude', 'Latitude', 'Azimuth', 'pic'], dtype='object')

5) Open file prod.ipynb and start the code. As a result you will get the file result.kml in the same folder

6) Open result.kml file in Google Earth Pro.

