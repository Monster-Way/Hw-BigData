# Docker
## docker常用命令
<BR>https://www.bilibili.com/video/BV1MC4y1P7GE?spm_id_from=333.788.player.switch&vd_source=fa7bdbb85b3026e2a92e276472cd8bc7
<BR>// run :: docker启动命令 -i :: 交互 -t :: 终端 -bash :: docker终端； 每个docker都有自己唯一的containerId, 重复输入docker run命令只会生成新容器
<BR><B>docker run -it \<dockerContainerId>/\<dockerName>:\<dockerTag> bash</B>
<BR>// stop :: docker关闭命令, 如果服务执行完成, docker也会自动关闭
<BR><B>docker stop \<dockerContainerId>/\<dockerName>:\<dockerTag></B>
<BR>// image rm :: 删除本地image
<BR><B>docker image rm \<imageName>/\<imageName>:\<imageTag></B>
<BR>// images/image ls :: 查看本地已有的Image
<BR><B>docker images</B>
<BR>// pull \<imageName> :: 隐式下载最新latest版本镜像 / pull \<imageName>:\<imageTag> :: 显示下载指定版本
<BR><B>docker pull \<dockerName>:\<dockerTag></B>
<BR>// build \<path> -t \<imageName>:\<imageTag> :: 构造镜像并指定镜像名和镜像标签
<BR><B>docker build \<path> -t \<imageName>:\<imageTag></B>
<BR>// -p \<dockerHostPort>:\<dockerContainerPort> :: 启动时设置docker端口映射dockerPort Mapping Function
<BR><B>docker run -p \<dockerHostPort>:\<dockerContainerPort> \<dockerName>:\<dockerTag></B>
<BR>// -e \<valName>=\<valValue> :: 启动时设置系统环境变量
<BR><B>docker run -e \<valName>=\<valValue> \<dockerName>:\<dockerTag></B>
<BR>// -v \<dockerHostPath>:\<containerPath> :: 使容器配置路径映射到主机同一位置, 避免数据丢失
<BR><B>docker run -v \<dockerHostPath>:\<containerPath> \<dockerName>:\<dockerTag></B>
<BR>
## DOCKERFILE 文件编译docker镜像


# FLink
## Flink2.2官方文档
<br>https://nightlies.apache.org/flink/flink-docs-release-2.2/docs/learn-flink/overview/
