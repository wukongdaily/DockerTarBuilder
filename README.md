[![GitHub](https://img.shields.io/github/license/wukongdaily/DockerTarBuilder.svg?label=LICENSE&logo=github&logoColor=%20)](https://github.com/wukongdaily/DockerTarBuilder/blob/master/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/wukongdaily/DockerTarBuilder.svg?style=flat&logo=appveyor&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/wukongdaily/DockerTarBuilder.svg?style=flat&logo=appveyor&label=Forks&logo=github)

## 🤔 这是什么？
它是一个工作流。可快速构建指定架构/平台的docker镜像

## 使用说明
### 用法一：pull镜像打成tar包下载
https://wkdaily.cpolar.cn/archives/gc
### 用法二：pull镜像并push到自己的仓库
首先在settings/secrets/actions中设置如下的Repository secrets：

    TARGET_REGISTRY: 自己的镜像仓库地址，例如registry.cn-hangzhou.aliyuncs.com/yourname/
    TARGET_REGISTRY_PASSWORD: 镜像仓库用户名
    TARGET_REGISTRY_USERNAME: 镜像仓库密码

<img width="581" alt="image" src="https://github.com/user-attachments/assets/ecd9f847-c200-49c3-8d1c-7fbb3a87a7ff">

其中镜像仓库可以通过阿里云获得。访问 https://cr.console.aliyun.com/ 扫码登录后进入个人实例，创建一个命名空间，例如yourname，然后获取访问凭证

<img width="412" alt="image" src="https://github.com/user-attachments/assets/cad2a207-0ff3-4044-b9d8-0cded4ed7201">

然后，参照用法一启动工作流，注意选择Pull And Push版的

<img width="163" alt="image" src="https://github.com/user-attachments/assets/f52fdcd7-2cc3-402e-bd58-b701acc308aa">

工作流执行完毕后，就可以去自己的镜像仓库pull到本地了

