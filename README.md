## 安装python 3.7.11
```
yum install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel libffi-devel gcc make gcc-c++ libstdc++-devel git
wget https://www.python.org/ftp/python/3.7.11/Python-3.7.11.tgz

tar -xzvf Python-3.7.11.tgz 
cd Python-3.7.11/
./configure --prefix=/usr/local/python3 
make && make install
```

```
ln -s /usr/local/python3/bin/python3 /usr/local/bin/python3  
ln -s /usr/local/python3/bin/pip3 /usr/local/bin/pip3  
```

## rasa 安装
```
python3 -m venv ./venv
source ./venv/bin/activate
pip3 install -U pip
pip3 install rasa
```
## rasa demo

```
git clone git@github.com:DreamerLark/rasa-demo.git

pip install git+https://github.com/mit-nlp/MITIE.git (pip install git+https://gitclone.com/github.com/mit-nlp/MITIE.git 解决国内服务器github访问)
pip install rasa[mitie] 
pip install jieba

```
中文词向量模型total_word_feature_extractor_zh.dat(密码：p4vx)（https://pan.baidu.com/s/1kNENvlHLYWZIddmtWJ7Pdg）
需要将该模型拷贝到创建的python项目data目录下(可任意位置)，后面训练NLU模型时用到


参考

https://www.iteye.com/blog/784838898-2515975

https://blog.csdn.net/weixin_43815222/article/details/121649581

https://rasa.com/docs/rasa/installation

