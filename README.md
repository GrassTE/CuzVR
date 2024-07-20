# 用于Vrchat的虚拟现实浙传

## 前言

本项目是以我的大学本科毕业设计为基础，制作的在Vrchat中的虚拟现实浙传

## 使用本项目
本项目使用的Unity版本为***2022.3.22f1***,建议严格按照版本下载，不然可能出现不可名状的Bug

在克隆项目之前，需要准备好Vrchat的SDK，[vrchatSDK下载地址](https://vrcpm.vrchat.cloud/vcc/Builds/2.3.2/VRChat_CreatorCompanion_Setup_2.3.2.exe)

本项目已经使用***.gitignore***文件对Unity内不需要参与版本管理的文件进行排除，所以在克隆本项目时，需要使用VrchatSDK新建Unity 2022 World Project，并将项目克隆后的文件全部复制进去（包括隐藏的.git文件夹），之后打开Unity编译完成后即可使用
## 关于OBJ文件
本项目使用的模型是利用***摄影测量倾斜摄影建模***方法，根据航拍照片生成的模型，所以面数比较高，有单个文件超过100M的情况，超过了GitHub的上传限制，所以在修改模型后需要使用***LFS***进行大文件Push。

### 使用LFS

[LFS下载地址](https://git-lfs.com/)

使用命令初始化LFS
```
git lfs install
```
本项目中已经存在.gitattributes，他会将内部配置的所有后缀名的文件列入到LFS提交的范围中
```
*.obj filter=lfs diff=lfs merge=lfs -text
```