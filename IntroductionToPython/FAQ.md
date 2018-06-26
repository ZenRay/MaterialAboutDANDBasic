**目录**

[TOC]

### 1. [[解释]频繁车程](https://discussions.youdaxue.com/t/topic/58800)
项目中要求计算 `display most frequent combination of start station and end station trip` 的问题，[这里](https://discussions.youdaxue.com/t/topic/58800)给出了解决思路。



### 2. 配置课程中需要的工作环境

在课程中用到的 `Python` 工作环境，可以使用 `conda` 导出后在本地进行配置工作环境。其基本的流程如下：

1. 确认课程中用到的环境名称

   直接在 `workspace` 中运行 `!conda env list`，其中带 $*$  的表示当前在使用的 `env`

2. 导出工作环境

   上图中 `/opt/conda` 前面的 $*$ 表示该环境路径，而环境的名称就是 `root`。需要导出`root` 工作环境，使用命令 `!conda env export --name root > environment.yaml`，这样即将环境导出为了 `environment.yaml`

   ![](https://user-images.githubusercontent.com/24636410/41887169-25aaf3c4-7932-11e8-969f-f364cb7ef08e.png)

   3. 下载导出的工作环境

      可以通过两种方式进去工作目录页面，方法一是点击 `Jupyter` `Logo`；方法二是点击 `File` 下拉菜单的 `Open`。找到 `environment.yaml` 将其下载下来——选中文件复选框，点击 `Download`

      ![](https://user-images.githubusercontent.com/24636410/41887422-1d7ab1b6-7933-11e8-9f4e-2ce4c1dfaeea.png)

   4. 安装本地工作环境

      找到 `environment.yaml` 在本地运行 `conda env create -f environment.yaml`命令以安装工作环境。

   报错信息：

   * `CondaValueError: prefix already exists: ` 因为环境名称和已有环境名称冲突，需要修改`environment.ymal`中环境的 `name` 值
   * `Solving environment: failed ResolvePackageNotFound:`：建议使用 `conda env export --name root --no-build > environment.yaml`，但是还是没有完全解决掉该问题，某些 `package` 还是没法安装；尝试过删除提到的 `package` 和 将 `package` 放到 `pip` 之后，还是没有解决问题 
   * `UnsatisfiableSpecifications error`：这个是因为某些 `package` 需要在依赖`python 2.x`
   * `UnsatisfiableError: The following specifications were found to be in conflict:`：这个是版本冲突

   5. **因为存在以上相关的报错信息，**提出一个相对完善的解决方案，直接查询在课程课程中需要的 `package` 版本号，使用 `conda install ` 命令进行本地安装。步骤如下：

      * 在 `workspace` 中输入命令查询相关 `package` 版本，例如查询 `pandas`——`!conda list | grep pandas`

        ![](https://user-images.githubusercontent.com/24636410/41892456-b6f4bcd0-794a-11e8-9137-3ffcaa938068.png)

      * 在本地运行安装命令并指定版本号——`conda install pandas=0.20.3`。配置新工作环境，保持 `python` 版本一致，需要使用命令——`conda create -n workspace python=3.6`，这样就能配置上 `python 3.6` 版本且工作环境名称为 `workspace`。如果需要指定特定的 `package` 和 `python` 一起安装，使用命令：`conda create -n workspace python=3.6 pandas=0.20.3 matplotlib=2.1.0 scipy=0.19.1`

      * 激活相关的工作环境名称即可，`source activate workspace`（`Mac` 和 `Linux` 可使用）或者 `activate workspace`（`Windows` 使用）

