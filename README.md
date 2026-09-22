# Root-zone soil moisture and meteorological records from six winter-wheat stations in northern China

Hourly soil and meteorological records from six agro-meteorological stations in
northern China's winter-wheat region, October 2020 to April 2022, used in the study
*"Information requirements for short-term root-zone soil moisture forecasting: A
case study in northern China's winter-wheat region"*.

## What is in this dataset

The original station records, **unprocessed**: no gap filling, outlier removal,
resampling, aggregation or unit conversion. Every value is as delivered by the
stations. Only two things were changed: the file names were translated into
English, and an editor name was removed from the Excel document properties. The
worksheet contents are byte-identical to the originals. The original file names
are kept in `files.csv`.

```
soil/          site1_bozhou_soil.xlsx ... site6_baoji_soil.xlsx
meteorology/   site1_bozhou_meteorology.xlsx ... site6_baoji_meteorology.xlsx
files.csv
```

| Site | Station | Province | Soil records | Meteorological records | Meteorological interval |
|---|---|---|---|---|---|
| 1 | Bozhou | Anhui | 13,416 | 13,824 | hourly |
| 2 | Cangzhou | Hebei | 13,416 | 13,822 | hourly |
| 3 | Zhumadian | Henan | 13,403 | 13,837 | hourly |
| 4 | Heze | Shandong | 13,405 | 13,824 | hourly |
| 5 | Lvliang | Shanxi | 13,405 | 27,647 | 30 min |
| 6 | Baoji | Shaanxi | 13,419 | 82,940 | 10 min |

Soil records run from 1 October 2020 to 14 April 2022 and meteorological records
from 1 October 2020 to 29 April 2022, all at the recording interval of the station.
`files.csv` gives, for each file: site, station, province, record type, number of
records and columns, first and last timestamp, recording interval, original file
name and MD5 checksum.

## Variables

Column headers are in Chinese, as in the original files. Each file has one
worksheet (`data`); the first column (`时间`) is the timestamp.

**Soil files** (22 columns)

| Header | Variable | Unit |
|---|---|---|
| `时间` | Timestamp | - |
| `土壤温度(℃)-地表` | Soil temperature at the surface | °C |
| `土壤温度(℃)-<d>` | Soil temperature at depth *d* | °C |
| `水分含量(%)-<d>` | Soil water content at depth *d* | % (volumetric) |

Depth labels are written `10`, `10cm` or `10CM` depending on the station.

**Measurement depths.** Sites 1, 2, 4, 5 and 6: soil temperature and soil water
content at 10, 20, ..., 100 cm. **Site 3 (Zhumadian)** differs: soil temperature
and soil water content at 10, 20, 30, 40, 50, 60, 80, 100, 120 and 150 cm (no 70 cm
or 90 cm sensor). Check the headers before stacking the sites by depth.

**Meteorological files** (9 columns; column order differs between stations)

| Header | Variable | Unit |
|---|---|---|
| `时间` | Timestamp | - |
| `空气温度(℃)` | Air temperature | °C |
| `相对湿度(%)` | Relative humidity | % |
| `大气压力(hPa)` | Atmospheric pressure | hPa |
| `风速(m/s)` | Wind speed | m/s |
| `风向(°)` | Wind direction | ° |
| `雨量(mm)` | Precipitation | mm |
| `当前太阳辐射强度(W/m²)` | Instantaneous solar irradiance | W/m² |
| `累计太阳辐射量(MJ/m²)` | Cumulative solar radiation | MJ/m² |

## Notes for users

- The records have not been quality-controlled. Missing hours, sensor faults and
  implausible values are left as recorded, so screen the data before use.
- Soil and meteorological loggers record at slightly different minutes past the
  hour; align them on your own time grid.
- The accompanying paper uses daily series derived from these records (23:00 soil
  water content as the forecast target, daily statistics of the other variables as
  inputs). Those derived tables are not included here.

## Source

Records from standard agro-meteorological stations of the China Meteorological
Administration observation network, as described in the accompanying paper.

## Licence

CC BY 4.0. You may use, share and adapt this data provided you give credit.

## Citation

If you use this dataset, please cite the accompanying paper. Citation details will
be added here once the paper is published.

## Contact

Zhiyuan Lyu - lvzhiyuan2020@126.com
College of Mechanical and Electrical Engineering, Hohai University,
Changzhou 213200, China
