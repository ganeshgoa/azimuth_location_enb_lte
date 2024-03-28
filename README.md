# azimuth_location_enb_lte
This program can help to draw the location and azimuth of lte base station using Longitude and Latitude and Azimuth(optional).
There are some important dependenties. 
Add a path for azimuth's picures:
1) Download all files
1) Open the folder "picures" and save the path of its location on your PC. For example: C:/Users/local/Downloads/pictures
2) Open file header_styles.txt and find all string with <href>C:/Users/garbu/Downloads/</href>,
then replace path with your path from previous step like this: "your_path"/empty1.png, "your_path"/0_90.png,
but you shoudn't touch last part with picture name /empty1.png, 0_90.png, 90_180.png, 180_270.png, 270_360.png
  
  <Style id="s_ylw-pushpin">
		<IconStyle>
			<scale>2.7</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/empty1.png</href>
			</Icon>
    
   <Style id="s_ylw-pushpin_hl">
		<IconStyle>
			<scale>3.19091</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/empty1.png</href>
			</Icon>

   <Style id="sh_0_90">
		<IconStyle>
			<scale>3.19091</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/0_90.png</href>
			</Icon>

    <Style id="sh_180_270">
		<IconStyle>
			<scale>3.19091</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/180_270.png</href>
			</Icon>

    <Style id="sh_270_360">
		<IconStyle>
			<scale>3.19091</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/270_360.png</href>
			</Icon>

    <Style id="sh_90_180">
		<IconStyle>
			<scale>3.19091</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/90_180.png</href>
			</Icon>

    <Style id="sn_0_90">
		<IconStyle>
			<scale>2.7</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/0_90.png</href>
			</Icon>

    <Style id="sn_180_270">
		<IconStyle>
			<scale>2.7</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/180_270.png</href>
			</Icon>

    <Style id="sn_270_360">
		<IconStyle>
			<scale>2.7</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/270_360.png</href>
			</Icon>

    <Style id="sn_90_180">
		<IconStyle>
			<scale>2.7</scale>
			<Icon>
				<href>C:/Users/garbu/Downloads/90_180.png</href>
			</Icon>
3) Check the file 'test_list_1000.xlsx' with enb information or take your file, BUT you should add column's name according to mines:
  dfcp.columns:
    Index(['Cell Name', 'Longitude', 'Latitude', 'Azimuth', 'pic'], dtype='object')

4) Open file prod.ipynb and start the code. As a result you will get the file result.kml in the same folder

5) Open result.kml file in Google Earth Pro:
    ![Uploading image.png…]()


