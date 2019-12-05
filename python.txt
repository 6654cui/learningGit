使用pip来查看python安装的包：
    pip list

使用pip卸载安装包：
    pip uninstall 模块名

virtualenv使用方法：
mac os 安装virtualenv：
    pip install --user virtualenv
    pip3 install virtualenv

使用virtualenv创建python环境：
    virtualenv -no-site-packages env

创建制定版本：
    virtualenv env --python=python2.7

激活虚拟环境：
    source env/bin/activate

退出虚拟环境：
    deactivate

pip区分python版本问题：
    py -2 -m pip install xxx
    py -3 -m pip install xxx

使用python2和3运行脚本：
    在脚本前面加上#！ python2/3

调用python3/2
    py -3/2



