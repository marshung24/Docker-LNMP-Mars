# Docker-LNMP
Docker LNMP 環境

> - Author: MarsHung
> - Date: 2021-12-25
> - 封存，將由 [marshung24/docker-local-dev-devcontainer](https://github.com/marshung24/docker-local-dev-devcontainer) 取代

## 說明
- 建立LNMP開發環境範本-MacOS版，供開發&測試應用

## 檔案結構
- code_data
  - index.php
- config
  - nginx
    - nginx.conf
  - php7.4
    - Dockerfile
    - php.ini
- .env
- docker-compose-mac.yaml
- docker-compose.yaml
- README.md

## 關命令

- 建構
  - `docker-compose up -d`
  - 指定設定檔: `docker-compose -f docker-compose-mac.yaml up -d`
- 移除
  - `docker-compose down`
- 開啟
  - `docker-compose start`
- 關閉
  - `docker-compose stop`
- 查看容器
  - 執行中容器 `docker container list`
  - 所有容器 `docker container list -a`
- 進入容器 dev_php
  - `docker exec -ti dev_php sh`

## 瀏覽
- 主程式: [http://localhost](http://localhost)
- PHPMyAdmin: [http://localhost:8080](http://localhost:8080)
- PHPRedisAdmin: [http://localhost:8081](http://localhost:8081)

## 開發
- 網頁程式根目錄在 ./code_data ，可調整 .env 程式碼路徑 CODE_PATH 變數，以變更連結的程式碼路徑







## 參考資料
- [用Docker建立php + Nginx 開發環境](https://charlie-c.medium.com/%E7%94%A8docker%E5%BB%BA%E7%AB%8Bphp-nginx-%E9%96%8B%E7%99%BC%E7%92%B0%E5%A2%83-33c5f88edeb3)
