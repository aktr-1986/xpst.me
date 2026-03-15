## プロセス管理ルール
- taskkill /IM でのプロセス名指定による広範なプロセス殺しは禁止
- 必ず netstat -ano | findstr :<ポート> でPID特定後、taskkill /F /PID <PID> で個別終了
- Claude Boss（8890）は全PJの親プロセスであり、これを落とすと全てが止まる
