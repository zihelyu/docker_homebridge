#HomeBridge 梓晨网络 www.dawnwl.com

FROM oznu/homebridge:latest

# 更换国内源

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    && apk update

# set registry

RUN npm config set registry http://registry.npm.taobao.org

# set permissions

RUN setcap cap_net_raw+eip $(eval readlink -f `which node`)