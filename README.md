cloud-native-apphub:
用户一键安装功能，如何获取相应的Certificate信息

说明：kubectl默认会从$HOME/.kube目录下查找文件名为 config 的文件，但是也能通过设置环境变量 KUBECONFIG 或者通过设置去指定其它 kubeconfig 文件。kubeconfig就是为访问集群所作的配置。

注意：一般config文件处于.kube文件夹内，且kube文件是隐藏文件夹。

若集群master登录用户为root:
cd /root
ls -al     #可以看到隐藏的.kube文件夹
cd .kube   #进入.kube文件件
cat config #即可显示server，certificate-authority-data，client-certificate-data，client-key-data
