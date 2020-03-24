# Anaconda安装
   - **使用pip下载Anaconda**： 
             
         
                                 
          pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package
- **安装Anaconda** ：
         
      bash / xxx.sh
 - **注意** 
 
     
     注意自动环境配置。
 
 


# Tensorflow2.0- GPU环境配置

- 使用conda命令创建一个Pyhton3.7的环境，并激活该环境。
  
      conda create --name tf2 python=3.7      # “tf2”是你建立的conda虚拟环境的名字
      conda activate tf2                      # 进入名为“tf2”的conda虚拟环境
- 使用pip命令安装tensorflow。

      pip install tensorflow

 - 安装cudnn以及cuda，注意版本之间的对应关系。
 
       conda install cudatoolkit=10.1
       conda install cudnn=7.6.5
       conda search cudatoolkit，   conda search cudnn搜索conda源版本。

- 注意 

  该步骤建立在已经核显已经禁用，并且N卡驱动已安装完毕的情况下。



# jupter Notebook的配置

- 在tensorflow环境下

      conda install ipython

      conda install jupyter 

      ipython kernelspec install-self--user











 


+ 主要参照

https://tf.wiki

https://www.cnblogs.com/guohaoblog/p/9319791.html
