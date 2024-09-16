1. "M" and "ME" both means month-end.
2. They have no difference, just before pandas 2.1, we use "M", and after that version it changed to "ME" to let it look less confused with "MS" meaning month-start.
3. Concerning resampling, you can think of it as "Grouping", that's about the definition of "sample" in statistics which is quite confusing to non-stat people. For example, lets say we did a survey gathered a year of data (365 data points), but in statistics, we call it 1 sample (not 365 samples), so the sample mean will be the mean of these 365 data points. In resampling, we assume doing the survey again, but this time threating a month as a "Group", so what we have is 12 samples each containing about 30 data points, so we can calculate 12 sample means
4. Returning to the code .resample("M") <- this is calling Python to group data by month, and assign a number to month end
In "MS", the number will be assigned to month-start
5. the number to be assigned is determined by the code following it: .last(), .sum(), .mean() etc
