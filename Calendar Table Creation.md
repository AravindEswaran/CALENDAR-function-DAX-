# CALENDAR-function-DAX-
To Create A Calendar table with fixed interval of Dates with only Custom New Table 

    Calendar = 

    ADDCOLUMNS (

    CALENDAR (DATE(2021,1,1), DATE(2022,06,31)),

    "DateAsInteger", FORMAT ( [Date], "YYYYMMDD" ),

    "Year", YEAR ( [Date] ),

    "Monthnumber", FORMAT ( [Date], "MM" ),

    "YearMonthnumber", FORMAT ( [Date], "YYYY/MM" ),

    "YearMonthShort", FORMAT ( [Date], "YYYY/mmm" ),

    "MonthNameShort", FORMAT ( [Date], "mmm" ),

    "MonthNameLong", FORMAT ( [Date], "mmmm" ),

    "DayOfWeekNumber", WEEKDAY ( [Date] ),
  
    "DayOfWeek", FORMAT ( [Date], "dddd" ),

    "DayOfWeekShort", FORMAT ( [Date], "ddd" ),

    "Quarter", "Q" & FORMAT ( [Date], "Q" ),

    "YearQuarter", FORMAT ( [Date], "YYYY" ) & "/Q" & FORMAT ( [Date], "Q" )

    )
