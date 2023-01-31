Website for reference: https://www1.ncdc.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf

GHCN (Global Historical Climatology Network) – Daily Documentation
NOTE: English units are displayed on pdf output format; Either Metric or standard English units on csv
or txt output formats depending on user specification.
I. Description
GHCN (Global Historical Climatology Network)-Daily is a database that addresses the critical need for
historical daily temperature, precipitation, and snow records over global land areas. GHCN-Daily is a
composite of climate records from numerous sources that were merged and then subjected to a suite of
quality assurance reviews. The archive includes over 40 meteorological elements (see Table 4 below for
complete list) including temperature daily maximum/minimum, temperature at observation time,
precipitation, snowfall, snow depth, evaporation, wind movement, wind maximums, soil temperature,
cloudiness, and more.
GHCN-Daily will serve as a replacement product for older NCDC-maintained data sets that are
designated for daily temporal resolution (i.e. DSI 3200, DSI 3201, DSI 3202, DSI 3205, DSI 3206, DSI 3208,
DSI 3210, etc.). It will function as the official archive for daily data from the Global Climate Observing
System (GCOS) Surface Network (GSN) and is particularly well suited for monitoring and assessment
activities related to the frequency and magnitude of extremes. Containing observations of one or more
of the above elements at more than 100,000 stations that are distributed across all continents, the
dataset is the world's largest collection of daily climatological data. The total of 1.4 billion data values
includes 250 million values each for maximum and minimum temperatures, 500 million precipitation
totals, and 200 million observations each for snowfall and snow depth. Station records, some of which
extend back to the 19th century, are updated daily where possible and are usually available one to two
days after the date and time of the observation.
Some of the data provided here are based on data exchanged under the World Meteorological
Organization (WMO) World Weather Watch Program according to WMO Resolution 40 (Cg-XII). This
allows WMO member countries to place restrictions on the use or re-export of their data for commercial
purposes outside of the receiving country. Those countries' data summaries and products which are
available here are intended for free and unrestricted use in research, education, and other noncommercial activities. For non-U.S. locations data, the data or any derived product shall not be provided
to other users or be used for the re-export of commercial services.
II. Format/Observation Definitions
(note: the term ‘element ’or ‘value’ is used throughout this documentation and refers to an individual
meteorological/climatological measurement or statistical value such as temperature, precipitation (amount), etc.)
Users are given the choice between the following two delivery formats:
1) GHCN-Daily Form- Portable Document Format (PDF) output giving 5 core values (see Table 4)
and, if available, the following additional values: TOBS (temperature at the time of observation),
EVAP (evaporation of water from evaporation pan), WDMV (24-hour wind movement), SN*#
(minimum soil temperature) and SX*# (maximum soil temperature). More details about these
values are in Table 4 (below). There are no flags (attributes) given with the GHCN- Daily Form
pdf file other than measurement flag “T” (trace value for precipitation, snowfall or snow depth,
as per table 3 below). Units for data values can be in metric or standard depending on user
preference for both CSV and text output. Empty, or blank, cells indicate that a data observation
was not reported.
2) Custom GHCN-Daily CSV- Output files contain .csv extension and optimized for spreadsheet
usage (i.e. delimited file). Besides unit preference, user is also given the choice whether to
include flags, station name or geographic location in data request. The user can define which of
the elements listed in Table 4 (below) to include in the data request.
3) Custom GHCN-Daily ASCII Form-Output is ASCII text file and the user is given the choice whether
to include flags, station name or geographic location in data request. The user can define which
of the elements listed in Table 4 (below) to include in the data request.
A. Data observations (values)
Each record represents all selected observations (values) available for a given station-day. The initial
section of each record is ordered as follows with the following definitions:
STATION (17 characters) is the station identification code. Please see
http://www1.ncdc.noaa.gov/pub/data/ghcn/daily/ghcnd-stations.txt
for a complete list of stations and their metadata.
STATION_NAME (max 50 characters) is the name of the station (usually city/airport name). Optional
output field.
GEOGRAPHIC_LOCATION (31 characters) is the latitude (decimated degrees w/northern hemisphere
values > 0, southern hemisphere values < 0), longitude (decimated degrees w/western hemisphere
values < 0, eastern hemisphere values > 0) and elevation above mean sea level (tenths of meters). This is
an optional output field.
DATE is the year of the record (4 digits) followed by month (2 digits) and day (2 digits).
B. Observations (values) and flags (attributes)
Following this initial section of the record, all selected observations and flags are given in the following
order:
Observation(s) | Measurement Flag | Quality Flag | Source Flag | Time of Observation | repeat for next
element (when more than one element is selected), where:
Observation(s) is/are defined in Table 4 below. 9’s in a field (e.g.9999) indicate missing data or data that
has not been received.
Measurement Flag (attribute) is defined in Table 1 below
Quality Flag (attribute) is defined in Table 2 below
Source Flag (attribute) is defined in Table 3 below
Time of Observation is the (2 digit hour, 2 digit minute) 24 hour clock time of the observation given as
the local time at the station of record.
Note: The 4 flags listed above are optional on the Custom GHCN-Daily ASCII Form.
Table 1 (Measurement Flag/Attribute)
Blank = no measurement information applicable
 A = value in precipitation or snow is a multi-day total, accumulated since last measurement
 (used on Daily Form pdf file)
 B = precipitation total formed from two twelve-hour totals
 D = precipitation total formed from four six-hour totals
 H = represents highest or lowest hourly temperature (TMAX or TMIN)
 or average of hourly values (TAVG)
 K = converted from knots
 L = temperature appears to be lagged with respect to reported
 hour of observation
 O = converted from oktas
 P = identified as "missing presumed zero" in DSI 3200 and 3206
 T = trace of precipitation, snowfall, or snow depth
 W = converted from 16-point WBAN code (for wind direction)
Table 2 (Quality Flag/Attribute)
Blank = did not fail any quality assurance check
 D = failed duplicate check
 G = failed gap check
 I = failed internal consistency check
 K = failed streak/frequent-value check
 L = failed check on length of multiday period
 M = failed mega-consistency check
 N = failed naught check
 O = failed climatological outlier check
 R = failed lagged range check
 S = failed spatial consistency check
 T = failed temporal consistency check
 W = temperature too warm for snow
 X = failed bounds check
 Z = flagged as a result of an official Datzilla investigation
Table 3 (Source Flag/Attribute)
Blank = No source (i.e., data value missing)
 0 = U.S. Cooperative Summary of the Day (NCDC DSI-3200)
 6 = CDMP Cooperative Summary of the Day (NCDC DSI-3206)
 7 = U.S. Cooperative Summary of the Day -- Transmitted
 via WxCoder3 (NCDC DSI-3207)
 A = U.S. Automated Surface Observing System (ASOS)
 real-time data (since January 1, 2006)
 a = Australian data from the Australian Bureau of Meteorology
 B = U.S. ASOS data for October 2000-December 2005 (NCDC DSI-3211)
 b = Belarus update
 C = Environment Canada
 E = European Climate Assessment and Dataset (Klein Tank et al., 2002)
 F = U.S. Fort data
 G = Official Global Climate Observing System (GCOS) or other government-supplied data
 H = High Plains Regional Climate Center real-time data
 I = International collection (non U.S. data received through personal contacts)
 K = U.S. Cooperative Summary of the Day data digitized from paper observer forms
 (from 2011 to present)
 M = Monthly METAR Extract (additional ASOS data)
 N = Community Collaborative Rain, Hail,and Snow (CoCoRaHS)
 Q = Data from several African countries that had been "quarantined", that is, withheld from
 public release until permission was granted from the respective meteorological services
 R = NCDC Reference Network Database (Climate Reference Network
 and Historical Climatology Network-Modernized)
 r = All-Russian Research Institute of Hydrometeorological Information-World Data Center
 S = Global Summary of the Day (NCDC DSI-9618)
 NOTE: "S" values are derived from hourly synoptic reports
 exchanged on the Global Telecommunications System (GTS).
 Daily values derived in this fashion may differ significantly
 from "true" daily data, particularly for precipitation(i.e., use with caution).
 s = China Meteorological Administration/National Meteorological Information Center/
 Climate Data Center (http://cdc.cma.gov.cn)
 T = SNOwpack TELemtry (SNOTEL) data obtained from the Western Regional Climate Center
 U = Remote Automatic Weather Station (RAWS) data obtained from the Western
 Regional Climate Center
 u = Ukraine update
 W = WBAN/ASOS Summary of the Day from NCDC's Integrated Surface Data (ISD).
 X = U.S. First-Order Summary of the Day (NCDC DSI-3210)
 Z = Datzilla official additions or replacements
 z = Uzbekistan update
Table 4 (observation/value)
Note: 9’s in a field (e.g.9999) indicate missing data or data that has not been received.
The five core values are:
PRCP = Precipitation (mm or inches as per user preference, inches to hundredths on Daily Form pdf file)
SNOW = Snowfall (mm or inches as per user preference, inches to tenths on Daily Form pdf file)
SNWD = Snow depth (mm or inches as per user preference, inches on Daily Form pdf file)
TMAX = Maximum temperature (Fahrenheit or Celsius as per user preference, Fahrenheit to tenths on
Daily Form pdf file
TMIN = Minimum temperature (Fahrenheit or Celsius as per user preference, Fahrenheit to tenths on
Daily Form pdf file

The other values are:
ACMC = Average cloudiness midnight to midnight from 30-second ceilometer data (percent)
ACMH = Average cloudiness midnight to midnight from manual observations (percent)
ACSC = Average cloudiness sunrise to sunset from 30-second ceilometer data (percent)
ACSH = Average cloudiness sunrise to sunset from manual observations (percent)
AWND = Average daily wind speed (meters per second or miles per hour as per user preference)
DAEV = Number of days included in the multiday evaporation total (MDEV)
DAPR = Number of days included in the multiday precipitation total (MDPR)
DASF = Number of days included in the multiday snowfall total (MDSF)
DATN = Number of days included in the multiday minimum temperature (MDTN)
DATX = Number of days included in the multiday maximum temperature (MDTX)
DAWM = Number of days included in the multiday wind movement (MDWM)
DWPR = Number of days with non-zero precipitation included in multiday precipitation total (MDPR)
EVAP = Evaporation of water from evaporation pan (mm or inches as per user preference, or hundredths
of inches on Daily Form pdf file)
FMTM = Time of fastest mile or fastest 1-minute wind (hours and minutes, i.e., HHMM)
FRGB = Base of frozen ground layer (cm or inches as per user preference)
FRGT = Top of frozen ground layer (cm or inches as per user preference)
FRTH = Thickness of frozen ground layer (cm or inches as per user preference)
GAHT = Difference between river and gauge height (cm or inches as per user preference)
MDEV = Multiday evaporation total (mm or inches as per user preference; use with DAEV)
MDPR = Multiday precipitation total (mm or inches as per user preference; use with DAPR and DWPR, if
available)
MDSF = Multiday snowfall total (mm or inches as per user preference)
MDTN = Multiday minimum temperature (Fahrenheit or Celsius as per user preference ; use with DATN)
MDTX = Multiday maximum temperature (Fahrenheit or Celsius as per user preference ; use with DATX)
MDWM = Multiday wind movement (miles or km as per user preference)
MNPN = Daily minimum temperature of water in an evaporation pan (Fahrenheit or Celsius as per user
preference)
MXPN = Daily maximum temperature of water in an evaporation pan (Fahrenheit or Celsius as per user
preference)
PGTM = Peak gust time (hours and minutes, i.e., HHMM)
PSUN = Daily percent of possible sunshine (percent)
SN*# = Minimum soil temperature where * corresponds to a code
for ground cover and # corresponds to a code for soil depth (Fahrenheit or Celsius as per user
preference)

Ground cover codes include the following:
 0 = unknown
 1 = grass
 2 = fallow
 3 = bare ground
 4 = brome grass
 5 = sod
 6 = straw mulch
 7 = grass muck
 8 = bare muck

Depth codes include the following:
 1 = 5 cm
 2 = 10 cm
 3 = 20 cm
 4 = 50 cm
 5 = 100 cm
 6 = 150 cm
 7 = 180 cm

SX*# = Maximum soil temperature where * corresponds to a code for ground
 cover and # corresponds to a code for soil depth. See SN*# for depth codes. (Fahrenheit or
Celsius as per user preference)
THIC = Thickness of ice on water (inches or mm as per user preference)
TOBS = Temperature at the time of observation (Fahrenheit or Celsius as per user preference)
TSUN = Daily total sunshine (minutes)
WDF1 = Direction of fastest 1-minute wind (degrees)
WDF2 = Direction of fastest 2-minute wind (degrees)
WDF5 = Direction of fastest 5-second wind (degrees)
WDFG = Direction of peak wind gust (degrees)
WDFI = Direction of highest instantaneous wind (degrees)
WDFM = Fastest mile wind direction (degrees)
WDMV = 24-hour wind movement (km or miles as per user preference, miles on Daily Form pdf file)
WESD = Water equivalent of snow on the ground (inches or mm as per user preference)
WESF = Water equivalent of snowfall (inches or mm as per user preference)
WSF1 = Fastest 1-minute wind speed (miles per hour or meters per second as per user preference)
WSF2 = Fastest 2-minute wind speed (miles per hour or meters per second as per user preference)
WSF5 = Fastest 5-second wind speed (miles per hour or meters per second as per user preference)
WSFG = Peak guest wind speed (miles per hour or meters per second as per user preference)
WSFI = Highest instantaneous wind speed (miles per hour or meters per second as per user preference)
WSFM = Fastest mile wind speed (miles per hour or meters per second as per user preference)
WT** = Weather Type where ** has one of the following values: