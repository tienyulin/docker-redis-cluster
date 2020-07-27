# Redis

## V2
### 提升 Image 使用彈性
修改 Port 號在建立 Container 時以環境變數方式新增，並在啟動 Container 時才修改 sentinel.conf 的 Port 值。此修改是為了讓設定值在啟動時才賦予，讓 Dockerfile 建立出來的 Image 可以更彈性的被使用。
