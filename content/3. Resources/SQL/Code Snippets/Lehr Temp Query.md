```SQL
SELECT [tag]
      ,[time]
      ,[value]
  FROM [P42HISTSVR].[piarchive]..[picomp2]
  where [tag] in ('LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_1','LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_2',
  'LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_3','LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_4',
  'LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_5','LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_6',
  'LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_7','LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_8',
  'LAWR.HotEnd.Data_CLX:RSLinx Enterprise:Lehr31.Temperature_9')
and [time] between '2023-03-24' and '2023-09-05'
GO
```
