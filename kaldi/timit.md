# Timit

timit - kaldi 工具箱.pptx

cmd.sh 脚本  由于我们是在虚拟机上运行所以配置成 =run.pl
path.sh 脚本中主要存放的是运行程序所需要的环境变量，一般不需我们进行修改

run.sh 该脚本就是我们运行数据集一系列操作的集合，下面详细分析

    这块是整个实验的数据准备工作 ，我们要做的就是修改 timit 数据集路径，按照上面给出的格式，然后调用 local 文件夹下的数据准备和词典准备的脚本，下一步是调用 uitls 文件夹下的 lang 准备脚本，这样数据准备的工作就结束了

    这块就是整个声学模型的参数，这里一般默认不更改 这里 nj 表示的是你使用的 cpu 核心的数目我们在虚拟机上运行一般设为 1 好了。

    这块是整个实验的数据准备工作 ，我们要做的就是修改 timit 数据集路径，按照上面给出的格式，然后调用 local 文件夹下的数据准备和词典准备的脚本，下一步是调用 uitls 文件夹下的 lang 准备脚本，这样数据准备的工作就结束了

    这块主要是为训练集和测试集提取 MFCC 特征，kaldi 支持 mfcc，plp，pitch 等特征，然后做 CMVN，compute cepstral mean and variance per utterence

    这块是单音素的训练和解码部分，是语音识别的最基本部分，在 kaldi 里这些代码都被封装了可以通过 shell 脚本直接调用

    这块是三音素的训练和解码部分

    这块在三音素模型的基础上加上 LDA 和 MLLT 变换，

    这块是在三音素模型的基础上做了 LDA+MLLT+SAT 变换

    这块是在三音素模型的基础上做了 sgmm2，sgmm2 是 povey 提出的

    这块是在三音素模型上做了 sgmm2+MMI
