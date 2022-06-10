## rules
1. map阶段应该将中间键值划分为桶？
2. woker应该将第x个reduce任务输出到mr-oux-x文件中
3. mr-oux-x文件应该有正确的格式 %v %v
4. woker应该将map输出在当前目录的文件中，作为reduce任务的输入
5. main/mrcoordinator.go 希望mr/mrcoordinator.go 实现done方法
6. 完成任务后，所有进程应该退出

## Hints
1. 修改mr/worker.go 的work
2. 中间文件命名 mr-X-Y X是map任务号，y是reduce任务号
3. 修改了mr/内容 就需要重新build
4. 中间文件的保存： go的 encoding/json 包
5. 可以从mrsequential.go借鉴代码
6. coordinator是并发的
7. 10s
8. 