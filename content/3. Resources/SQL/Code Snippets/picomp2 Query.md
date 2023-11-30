```SQL
SELECT [tag]
      ,[time]
      ,[value]
  FROM [P42HISTSVR].[piarchive]..[picomp2]
  where [tag] = 'LAWR.HotEnd.Data_CLX:RSLinx Enterprise:AllGlass34.LehrDumpTimeL34'
and [time] between '2022-02-07' and '2022-06-08'
GO