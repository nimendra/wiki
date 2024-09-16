Resampling with 'ME' in pandas has the following effects on time series data:

1. 'ME' stands for "Month End" frequency. It will resample the data to the last day of each month.

2. It performs downsampling, reducing the frequency of the data from whatever the original frequency was (e.g. daily, hourly, etc.) to monthly.

3. All data points within each month will be aggregated into a single value for that month-end date.

4. By default, no aggregation function is applied, so you need to specify how to combine the values within each month (e.g. mean, sum, last, etc.).

5. The resulting resampled data will have one data point per month, on the last day of each month.

6. Any months that don't have data will result in NaN values unless filled.

7. The datetime index of the resampled data will be on the last day of each month.

For example:

```python
# Original daily data
data = pd.Series([1,2,3,4,5], index=pd.date_range('2023-01-01', periods=5, freq='D'))

# Resample to month end
monthly = data.resample('ME').mean()
monthly = data.resample('ME').last()

```

This would aggregate the daily values to a single monthly value at the end of January.

The key points are:
- It reduces frequency to monthly 
- Aggregates all data within each month
- Results in one value per month, on the last day
- Requires specifying an aggregation method

Citations:
[1] https://link.springer.com/article/10.1007/s41060-017-0044-3
[2] https://www.datacamp.com/tutorial/pandas-resample-asfreq
[3] https://campus.datacamp.com/courses/manipulating-time-series-data-in-python/basic-time-series-metrics-resampling?ex=5
[4] https://repository.fit.edu/cgi/viewcontent.cgi?article=1701&context=etd
[5] https://machinelearningmastery.com/resample-interpolate-time-series-data-python/
[6] https://tanzu.vmware.com/content/blog/time-series-analysis-part-3-resampling-and-interpolation
[7] https://towardsdatascience.com/time-series-data-analysis-resample-1ff2224edec9?gi=7bf15c75eed3