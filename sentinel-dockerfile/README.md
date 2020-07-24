# Redis - Docker Compose + Dockerfile
這個範例使用了 DockerCompose 結合 Dockerfile，以下介紹使用 Dockerfile 的好處 : 

* 設定環境變數  
sentinel.conf 可以使用環境變數，這樣就不需要每個 Redis Container 啟動時都要寫一份 sentinel.conf 可能只是為了改 port 號。
