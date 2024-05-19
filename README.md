# 简介
* 使用多线程异步操作rknn模型, 提高rk3588/rk3588s的NPU使用率, 进而提高推理帧数
* 此分支使用模型[yolov8_rknn](https://github.com/airockchip/rknn_model_zoo),
* [测试视频](https://github.com/leafqycc/rknn-multi-threaded/releases/download/v0.2/720p60hz.mp4)
* 本人环境ubuntu22.04，librknnrt version: 2.0.0b0，RKNN_Driver version：0.92,rknn_toolkit version: 2.0.0b0+9bab5682

# 更新说明
* 无


# 使用说明
### 演示
  * 将仓库拉取至本地, 并将Releases中的演示视频放于项目根目录下, 运行main.py查看演示示例
  * 切换至root用户运行performance.sh可以进行定频操作(约等于开启性能模式)
  * 运行rkcat.sh可以查看当前温度与NPU占用
### 部署应用
  * 修改main.py下的modelPath为你自己的模型所在路径
  * 修改main.py下的cap为你想要运行的视频/摄像头
  * 修改main.py下的TPEs为你想要的线程数, 具体可参考下表
  * 修改func.py为你自己需要的推理函数, 具体可查看myFunc函数

# 多线程模型帧率测试
* 使用performance.sh进行CPU/NPU定频尽量减少误差
* 测试模型为[yolov8_rknn](https://github.com/airockchip/rknn_model_zoo)
  

# Acknowledgements
* https://github.com/rockchip-linux/rknn-toolkit2
* https://github.com/airockchip/rknn_model_zoo
