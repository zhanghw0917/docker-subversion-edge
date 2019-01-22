# zhanghw0917/docker-subversion-edge

fork from   mamohr/docker-subversion-edge https://github.com/mamohr/docker-subversion-edge

This is a docker image of the Collabnet Subversion Edge Server

## Usage

* pull image 

        docker push brotherdavid/csvn:0.1
    
* 创建宿主机 工作目录
   
        mkdir -p /mtdata/csvn_repo
        chown 777 -R csvn_repo
   
 * 运行
 
        docker run -d -p 3343:3343 -p 4434:4434 -p 18080:18080 -v /mtdata/csvn_repo:/opt/csvn/data --name csvn-server brotherdavid/csvn:0.1
 
* 说明

 > * 3343 - HTTP CSVN Admin Sites
 > * 4434 - HTTPS CSVN Admin Sites (If SSL is enabled)
 > * 18080 - Apache Http SVN

* 使用 

    访问 http://docker-host:3343/csvn 进入web管理页面
    svn 资源库访问地址  http://docker-host:18080

更多信息访问
[CollabNet](http://collab.net/products/subversion).
