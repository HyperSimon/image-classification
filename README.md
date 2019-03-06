# image-classification

图像分类。

## 快速上手

```bash
# 获取代码
git clone https://github.com/HaveTwoBrush/image-classification.git
cd image-classification

# 安装依赖
pip install -r requirements.txt

# 根据下文中数据集链接下载数据，并将数据放入 /datas 下的对应文件夹中。（划分数据脚本后续上传）
# 训练模型
python -m app.train

# 在 /save 中找到训练效果最好的模型，记录模型路径
# 开始测试
python -m app.test --model_path $your_best_model_path

# 开启图片分类 api
python -m app.api
# 发送一张图片进行测试
curl -F "upload=@/your/image/path/1.jpg; filename=1.jpg" http://127.0.0.1:8008/image_classification
```

## 数据集

### 二分类数据集

我们这里选择【猫】和【狗】，当然它也适用于【正例】和【反例】。

你可以在 kaggle 上下载到这个[数据集](https://www.kaggle.com/c/dogs-vs-cats/)。

## 网络模型

-[ ] AlexNet
-[ ] GoogLeNet
-[ ] VGG
-[ ] ResNet
-[ ] MobileNet
-[X] ShuffleNet

## License

[MIT LICENSE](./LICENSE)