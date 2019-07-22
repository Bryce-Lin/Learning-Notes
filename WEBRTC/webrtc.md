### 基本格式

基本格式
let mediaRecorder = new MediaRecorder(stream[,options])

开始录制媒体
mediaRecorder.start(timeslice) 


停止录制

MediaRecorder.stop()


暂停

MediaRecorder.pause()



MediaRecorder.resume()

每次记录一定时间的数据时
MediaRecorder.ondataavailable
    
错误
MediaRecorder.onerror


javascript 操作数据类型

字符串

blob

arraybuffer

arraybufferview



参数说明

stream // 媒体流
options {
    mimeType   //   video/mp4;codecs=h264   视频格式
    videoBitsPerSecond  //视频码率
    videoBitsPerSecond   // 音频码率
}

