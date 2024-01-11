# Plume Data Extraction

## Overview 
This repository contains two R Markdowns that extracts plume data from <a href="https://data.carbonmapper.org/" target="_blank">Carbon Mapper</a> and <a href="https://earth.jpl.nasa.gov/emit-mmgis-lb/?mission=EMIT&site=ert&mapLon=-103.84810013696554&mapLat=32.54933309954321&mapZoom=9&globeLon=0&globeLat=3.508354649267438e-15&globeZoom=2&globeCamera=9.000268457972838,-10000000,10.000298286636488,0,1,0&panePercents=0,100,0&on=3d9e9b7f-9c7c-4c92-94d8-dec04c300168$1.00,8fed617c-0c4e-4841-87d1-f4ffd1a56d4e$1.00,37414e25-e3d3-4b78-ade5-75edfe4e5da0$1.00,ba365157-1ba0-4c7e-9a3a-4bce7ad3ed13$0.70" target="_blank">NASA EMIT</a> for a series of locations and a buffer distance specified by the user. The R Markdowns output a CSV file that contains the initial dataset as well as spatially joined plume data.

## Technical Discussion
The tool contains three seperate chunks to import libraries, initialize parameters, and retrieve plume data. Users are only required to edit the second chunk to initialze the following parameters:
<ul>
 <li><b>excel_file_path:</b> Path of the input excel file.</li>
 <li><b>output_folder:</b> Folder that the output file will be saved to.</li>
 <li><b>x_field:</b> Field name of the X-Coordinate.</li>
 <li><b>y_field:</b> Field name of the Y-Coordinate.</li>
 <li><b>bufferDist_mi:</b> Distance of the buffer in miles.</li>
</ul>

### Workflow