# sphinx 

> 一个生成文档的应用

`ubuntu20.04` `sphinx` 

## 一、环境安装

### 1. 一键安装


git clone [git@github.com:dspure/sphinx.git](git clone git@github.com:dspure/sphinx.git)

```shell
cd sphinx
chmod a+x install.sh
./install.sh
```

按照步骤二创建工程后，使用 sphinx 文件夹中的相应文件，覆盖 source/config.py index.rst ，讲 sphinx配置文件.md 复制到source目录下即可。 

### 2. 手动安装

#### 2.1 下载

```bash
sudo apt install python3-pip //安装 pip3
pip3 install sphinx //安装 sphinx
sudo apt install docutils-common //reStructuredText 支持包
pip3 install sphinx sphinx-autobuild recommonmark sphinx-markdown-tables
```

#### 2.2 配置 markdown

```
extensions = [
        'sphinx_markdown_tables',
        'recommonmark'
]
from recommonmark.parser import CommonMarkParser
source_parsers = {
        '.md':CommonMarkParser,
}
source_suffix = ['.rst', '.md']
```

## 二、创建工程

- sphinx-quickstart

- 配置文件放在配置文件目录

source/_static目录放一些静态文件，如image等。source/index.rst文档中定义目录结构。source/conf.py为配置文件。

## 三、卸载方法

```shell
pip3 uninstall sphinx
```

## 参考

https://learnblockchain.cn/docs/etherscan/sphinx.html

https://zhuanlan.zhihu.com/p/27544821

https://www.jianshu.com/p/728aac51cc53

https://www.jianshu.com/p/b028ba823219

https://recommonmark.readthedocs.io/en/latest/

https://www.jianshu.com/p/b028ba823219