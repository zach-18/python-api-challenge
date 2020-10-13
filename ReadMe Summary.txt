Python API Challenge Summary:

This was a challenging exercise.  I exceeded the download limit for the Weather API on Sunday morning, but fortunately they were able to allow me more access.
I did enjoy this however, it is great to have a list of ideal hotels for perfect weather:

city	country	lat	lon	temp	humidity	cloudiness	wind speed	Hotel Name	Hotel	Hotel Address	Hotel Rating
33	Mendoza	AR	-32.89	-68.83	78.80	16	0	6.93		Cavas Wine Lodge S.A.	Costaflores, Cobos s/n, Luján de Cuyo	4.7
112	Morón	AR	-34.65	-58.62	75.27	38	0	1.99		Hilton Buenos Aires	Macacha Güemes 351, BKG	4.6
142	Mercedes	AR	-34.65	-59.43	75.74	43	0	5.01		Hotel San Carlos	Zerboni y Zapiola, San Antonio de Areco	4.3
167	Santa Maria	BR	-29.68	-53.81	72.63	48	0	4.43		Ivlas Boutique Hotel	R. Martins Pena, 120 - Camobi, Santa Maria	4.7
273	Poum	NC	-20.23	164.02	75.47	82	0	6.22		Karem Bay	RPN1	4.8
371	Radaur	IN	30.03	77.15	77.20	40	0	3.02		Noormahal Karnal	Noormahal Crossing, National Highway 1, Sector...	4.4
421	Tigre	AR	-34.43	-58.58	73.60	53	0	8.05		Hilton Buenos Aires	Macacha Güemes 351, BKG	4.6
500	Neuquén	AR	-38.95	-68.06	75.20	25	0	8.05		Hotel del Comahue	AYD, Avenida Argentina 377, Neuquén	4.1
518	Nizwá	OM	22.93	57.53	78.66	17	0	8.19		Alila Jabal Akhdar	Al Roose, Jabal Al Akhdar Al Jabal Al Akhdar OM	4.7
538	Ibrā’	OM	22.69	58.53	77.18	17	0	9.01		معسكر ليالي الصحراء Desert Nights Camp	Al Wasil OM	4.5


Your first requirement is to create a series of scatter plots to showcase the following relationships:

Temperature (F) vs. Latitude
- There is an upside down U shape to this plot.  Near zero latitude, we have the highest temperature as expected.

Humidity (%) vs. Latitude
- There was no correlation between humidity and latitude.

Cloudiness (%) vs. Latitude
- Similar to humidity, there was no visible correlation.

Wind Speed (mph) vs. Latitude
- There was an even concentration of lower wind speed across all latitudes.  The highest wind speed points where spread across the range of latitude.

After each plot add a sentence or too explaining what the code is and analyzing.
Your second requirement is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Northern Hemisphere - Temperature (F) vs. Latitude
For the northern hemisphere the correlation was -0.88.  This shows a high negative correlation between temp and latitude.

Southern Hemisphere - Temperature (F) vs. Latitude
For the southern hemisphere the correlation was 0.67.  Not as strong as the northern hemisphere, but they are also in spring, which could havev an impact.

Northern Hemisphere - Humidity (%) vs. Latitude
Correlation was 0.23.  This matches the scatter plot.  Not much of a correlation.
The r-squared is 0.05, very low.

Southern Hemisphere - Humidity (%) vs. Latitude
Correlation is 0.03.  This means no correlation.
Also, the slope of the fit is 0.05.  This is almost a flat line.  

Northern Hemisphere - Cloudiness (%) vs. Latitude
Correlation = 0.16, low r-squared of 0.26.  Very little correlation between cloudiness and latitude.  Makes sense, weather patterns cover the globe.

Southern Hemisphere - Cloudiness (%) vs. Latitude
Correlation = 0.2, r-squared is 0.04.  Again, little correlation.

Northern Hemisphere - Wind Speed (mph) vs. Latitude
Correlation is 0.07.  Again, no relationship between these factors.

Southern Hemisphere - Wind Speed (mph) vs. Latitude
Correlation is -0.26.  No significant relationship.