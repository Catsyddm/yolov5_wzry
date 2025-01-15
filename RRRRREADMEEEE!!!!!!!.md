最开始在b站发现了一个基于yolov5实现王者中各种物体识别的视频，同时发现作者将教程发在了csdn上，于是便想拿来玩玩，于是便有了这个程序
我期望这个程序实现的功能是可以对王者荣耀的对局视频进行英雄(hero)、小兵(soldier)、防御塔(tower)的识别
参考的教程为：https://blog.csdn.net/m0_53392188/article/details/119334634?ops_request_misc=%257B%2522request%255Fid%2522%253A%25223d018553cac93a9e96a81866c7b5b2c8%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=3d018553cac93a9e96a81866c7b5b2c8&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-2-119334634-null-null.142^v101^control&utm_term=yolov5&spm=1018.2226.3001.4187
遇到的困难&解决办法：
No.1 虚拟环境无法创建，出现"conda init"的提示，解决办法为在conda prompt终端进行虚拟环境的建立，然后在vscode中选择对应的python编译器
No.2 github远程提交以及与vscode的交互问题，解决办法为参考vscode官方在油管上发布的视频：https://www.youtube.com/watch?v=i_23KUAEtUM
No.3 我的电脑有GPU算力而且下载过CUDA，但是在train的代码中无法调用，device选项只能选cpu，正在尝试解决
No.4 解决OMP: Error #15: Initializing libiomp5md.dll, but found libiomp5md.dll already initialized.报错问题，解决方法：https://blog.csdn.net/qq_37164776/article/details/126832303?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522cd43ca041553090f2d0bca2a5c961a80%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=cd43ca041553090f2d0bca2a5c961a80&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-126832303-null-null.142^v101^control&utm_term=Initializing%20libiomp5md.dll%2C%20but%20found%20libiomp5md.dll%20already%20initialized.&spm=1018.2226.3001.4187
No.5 train.py 应该是可以运行了，但是训练进度一直为0%，原因暂不知晓

总归，时间有限，代码目前还不完善，后续会继续更新这段代码，并尝试使用别的游戏的训练集。