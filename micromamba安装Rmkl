# micromamba安装Rmkl

## 一、下载安装

```shell
# 如果是macOS、Linux或Windows上的Git Bash，则有一种简单的安装方法micromamba。只需在您喜欢的shell中执行安装脚本即可。
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
```

## 二、配置mambarc文件

```shell
# 配置.mambarc文件
vim ~/micromamba/.mambarc
```

## 三、添加channels至mambarc文件

```shell
## 添加以下内容，并保存
channels:
  - defaults
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda
custom_channels:
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch-lts: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
always_yes: true
auto_activate_base: false

# source配置
source ~/.bashrc
```

## 四、检查micromamba是否成功安装配置

```shell
# 输入以下命令，若显示了版本号，则说明安装成功
micromamba --version
```

## 五、创建R环境

```shell
# 创建R环境，链接mkl的blas库
micromamba create -n Rmkl r-base=4.3.1 "libblas=*=*mkl*" -c conda-forge
```

## 六、其他说明

```shell
# micromamba简介
1、mamba是使用C++对conda的重实现：使用多线程并行下载仓库数据和包文件；采用libsolv更快解决包依赖关联；核心部分使用C++获取最大效率
1、micromamba为mamba的精简版，十分轻量化，不需要base环境和Python，且由于是静态版本，可放置在任意位置
3、mamba和conda命令几乎一样，学习成本低，conda环境也可迁移至mamba
# 脚本中调用时命令
micromamba run -n Rmkl Rscript xxx.R
```

