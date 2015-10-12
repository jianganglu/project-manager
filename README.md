# project-manager
目录与开发规范
使用 Nodejs 在本地进行开发和调试，使用 gulp 把 ./src 的开发文件部署到 ./build 目录。使用打git标签的方式进行发布上线.

项目相关工具
less
gulp
git
nodejs
clam
https://github.com/aui/artTemplate

-root
    -.clam 
    -build //打包以后的线上文件
    -src //开发目录
        -libs //基础库
        -mods //模块
        -pages //页面
环境、开发、调试
git clone 项目地址
sudo npm install
sudo clam on
浏览器访问 http://localhost/ Server指向 ./src 目录
关于git branch
开发新功能

git checkout -b daily/x.y.z 升级y 比如当前线上版本号1.0.0 新功能的版本应该为 1.1.0.

修改bug

git checkout -b daily/x.y.z 升级z 比如当前线上版本号1.0.0 新功能的版本应该为 1.0.1.

版本发布
确认本地已验收通过
gulp //命令行
git push origin daily/x.y.z //提交文件到分支
git tag publish/x.y.z //创建新版本标签
git push origin publish/x.y.z //发布分支
git branch -d daily/x.y.z //删除开发分支

