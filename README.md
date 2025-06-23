# Data-Analyst-Task1-EL-

1.Handled missing values in the dataset(Deleted NAN values)
2.Removed Duplicates
3. Format Normalization	Identified that the Dt_Customer column contained dates in mixed formats, such as 05/11/2020 and 12-04-2021.	Manually inspected a few entries
4. Uniform Separator	Replaced all slashes (/) with dashes (-) to make the date format consistent across the column.	str.replace('/', '-', regex=False)
5. Safe Date Parsing	Converted the column to datetime format using day-first parsing to handle formats like dd-mm-yyyy.	pd.to_datetime(..., dayfirst=True, errors='coerce')
6. Standard Display Format	Converted the parsed dates into a uniform string format dd-mm-yyyy for clear display and further analysis.	.dt.strftime('%d-%m-%Y')
7. Error Handling	Used errors='coerce' to handle any invalid date values gracefully by converting them to NaT, allowing for easy identification.	errors='coerce' in pd.to_datetime()
