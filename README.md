# PC Setting for Development Environment

## 1.  Visual Studio Code

## 2.  Python

## 3.  Git

## 4.  Node.js

## 5.  Docker

## 6.  Docker Compose

## 7.  Docker Machine

## 8.  Docker Toolbox

## 9.  VirtualBox

## 10.  Vagrant

## 11.  VirtualBox Extension Pack

## 12.  VirtualBox Guest Additions

## 13. MySQL

## 14. PostgreSQL

<details>
<summary>data folderの変更</summary>

serviceからpostgresqlを停止しておく。

PostgreSQLの本体のpath

``` Terminal
C:\Program Files\PostgreSQL\14
C:\Program Files\PostgreSQL\15
```

PostgreSQLのデータフォルダ

変更前

``` Terminal
C:\Users\{your_name}\DBs\PostgreSQL\data
```

変更後

``` Terminal
C:\Users\{your_name}\DBs\PostgreSQL\14\data
```

registryの変更

`コンピューター\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\postgresql-x64-14`の`ImagePath`を変更

変更前

``` Terminal
"C:\Program Files\PostgreSQL\14\bin\postgres.exe" -D "C:\Users\{your_name}\DBs\PostgreSQL\data" -p 5432 -h localhost -i -o -k "C:\Users\{your_name}\DBs\PostgreSQL\data"
```

変更後

``` Terminal
"C:\Program Files\PostgreSQL\14\bin\postgres.exe" -D "C:\Users\{your_name}\DBs\PostgreSQL\14\data" -p 5432 -h localhost -i -o -k "C:\Users\{your_name}\DBs\PostgreSQL\14\data"
```

実際の変更後のデータ

``` registry
"C:\Program Files\PostgreSQL\14\bin\pg_ctl.exe" runservice -N "postgresql-x64-14" -D "C:\Users\{your_name}\DBs\PostgreSQL\14\data" -w
```

</details>

## 15. MongoDB

## 16.  Rust

## 17.  Go

## 18.  Java

## 19.  Node.js

## 20.  C++
