# Redis - Docker Compose + Dockerfile
這個範例使用了 DockerCompose 結合 Dockerfile，以下介紹一些使用 Dockerfile 的好處 : 
* 可以直接複製 sentinel.conf 到 Redis Container
如果是用 Volume 掛載的話，sentinel.conf 會和 Container 裡的 sentinel.conf 同步，這樣下次要再建一個 Redis Container 又要再建一個 sentinel.conf。

* 設定環境變數
sentinel.conf 可以使用環境變數，這樣就不需要每個 Redis Container 啟動時都要寫一份 sentinel.conf 可能只是為了改 port 號。
