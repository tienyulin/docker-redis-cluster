# Redis Docker Compose + Dockerfile
使用 Dockerfile 的好處是可以自訂一些參數來使用，像是這個範例是根據每個 Container 在 docker-compose.yml 設定 REDIS_PORT 的參數，然後在 Dockerfile 裡面去改 sentinel.conf 裡的 Port 號。  

這樣的作法是我只需要一個 sentinel，不需要建多少 Container 就要新增多少個 sentinel.conf，如本專案的 sentinel 資料夾的範例。那個範例因為 sentinel.conf 要用 Volume 掛載進 Container，所以 Port 號是寫死的。那就必須一個 Container 要新增一個 sentinel.conf。

所以建議結合 Dockerfile 實做，當要新增 Container 時只要改 docker-compose.yml 即可。

## V2
### 提升 Image 使用彈性
修改 Port 號在建立 Container 時以環境變數方式新增，並在啟動 Container 時才修改 sentinel.conf 的 Port 值。此修改是為了讓設定值在啟動時才賦予，讓 Dockerfile 建立出來的 Image 可以更彈性的被使用。
