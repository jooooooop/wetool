# WEMVC开发辅助工具
1. 获取工具

   `go get github.com/Simbory/wetool`
   
2. 创建项目文件夹

   `user@local:~/gopath/src/projects$ mkdir sample`
3. cd 到项目文件夹

   `user@local:~/gopath/src/projects$ cd sample`
   
4. 初始化项目

   `user@local:~/gopath/src/projects/sample$ wetool init`
   
5. 创建项目新的Area

   `user@local:~/gopath/src/projects/sample$ wetool area admin`
   
6. 启用Area: 在~/gopath/src/projects/sample/main.go文件中引入

   `import _ "projects/sample/admin"`

7. 创建新的controller

   `user@local:~/gopath/src/projects/sample$ wetool ctrl news`

8. 添加route规则：在~/gopath/src/projects/sample/controllers/init.go文件中添加路由

   `wemvc.Route("/news/<action=index>/<id=>", NewsController{})`

9. 运行项目
   
   `user@local:~/gopath/src/projects/sample$ go run main.go`
   
   或者
   
   `user@local:~/gopath/src/projects/sample$ wetool run`
