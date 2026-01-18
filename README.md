<!-- TOC -->
* [Docker](#docker)
  * [docker常用命令](#docker常用命令)
  * [DOCKERFILE 文件编译docker镜像](#dockerfile-文件编译docker镜像)
* [FLink](#flink)
  * [Flink2.2官方文档](#flink22官方文档)
<!-- TOC -->
# Docker
## docker常用命令
<BR>https://www.bilibili.com/video/BV1MC4y1P7GE?spm_id_from=333.788.player.switch&vd_source=fa7bdbb85b3026e2a92e276472cd8bc7
<BR>// run :: docker启动命令 -i :: 交互 -t :: 终端 -bash :: docker终端； 每个docker都有自己唯一的containerId, 重复输入docker run命令只会生成新容器
<BR><B>docker run -it \<dockerContainerId>/\<dockerName>:\<dockerTag> bash</B>
<BR>// -p \<dockerHostPort>:\<dockerContainerPort> :: 启动时设置docker端口映射dockerPort Mapping Function
<BR><B>docker run -p \<dockerHostPort>:\<dockerContainerPort> \<dockerName>:\<dockerTag></B>
<BR>// -e \<valName>=\<valValue> :: 启动时设置系统环境变量
<BR><B>docker run -e \<valName>=\<valValue> \<dockerName>:\<dockerTag></B>
<BR>// -v \<dockerHostPath>:\<containerPath> :: 使容器配置路径映射到主机同一位置, 避免数据丢失
<BR><B>docker run -v \<dockerHostPath>:\<containerPath> \<dockerName>:\<dockerTag></B>
<BR><BR>
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

<BR><-- 私仓 -->
<BR>git clone git@github.com:Monster-Way/Hw-BigData.git
<BR>docker build -t .\ hw-docker-images:1.0.0
<BR>docker login
<BR>docker push hwmonsterway/hw-docker-images:1.0.0
<BR>docker pull hwmonsterway/hw-docker-images:1.0.0

## DOCKERFILE 文件编译docker镜像
<BR><B>FROM</B>
<BR>
<BR><B>RUN</B>
<BR>
<BR><B>ENV</B>
<BR>
<BR><B>WORKDIR</B>
<BR>
<BR><B>COPY</B>
<BR>
<BR><B>CMD</B> :: 用于指定容器默认运行的程序(可替换)
<BR> - CMD \<shell命令>
<BR> - CMD ['要执行的命令', '参数1', '参数2']
<BR>&nbsp;&nbsp;&nbsp;&nbsp;1. 如果Dockerfile中存在多条CMD命令, 只有最后一条生效
<BR>&nbsp;&nbsp;&nbsp;&nbsp;2. CMD 可以被容器启动时的命令行参数替换 "docker run -it \<image> <命令> <参数1> <参数2>"
<BR>
<BR><B>ENTRYPOINT</B> :: 用于指定容器默认运行的程序(不可替换)
<BR> - ENTRYPOINT \<shell命令>
<BR> - ENTRYPOINT ['要执行的命令', '参数1', '参数2', ...]
<BR>&nbsp;&nbsp;&nbsp;&nbsp;1. Dockerfile中只能定义一个ENTRYPOINT
<BR>&nbsp;&nbsp;&nbsp;&nbsp;2. ENTRYPOINT指定的命令不能被替换, 在容器启动时可以追加参数
<BR>&nbsp;&nbsp;&nbsp;&nbsp;3. CMD 可以用于给ENTRYPOINT指定参数, ENTRYPOINT设置指定命令 CMD用作可选可替换参数
<BR><B>
<BR>
<BR><B>
<BR><B>
<BR><B>
<BR><B>
<BR><B>


# FLink
## Flink2.2官方文档
<br>https://nightlies.apache.org/flink/flink-docs-release-2.2/docs/learn-flink/overview/
