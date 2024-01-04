# Yolo Troubleshooting Guide

<details>
  <summary><h3>Error: cuDNN isn't found FWD algo for convolution.</h3></summary>
  
<b>환경</b> : Windows 11, Visual studio 2019, Yolov4, NVIDA GeForce RTX 3070
<br>
<b>증상</b> : RTSP + Yolov4 동작 중 특정 채널 이상이 되면 오류 발생
<br>
<b>원인</b> : Input Data가 GPU Memory의 사이즈보다 커서 발생
<br>
<b>해결 방안</b> : GPU 교체 또는 Parameter 수정
<br>
<b>참고 링크 : </b> [링크](https://gororoman.tistory.com/entry/Error-cuDNN-isnt-found-FWD-algo-for-convolution-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95)

</details>

<br>

# Yolo Troubleshooting Guide

<details>
  <summary><h3>FileNotFoundError: Could not find: nvinfer.dll. Is it on your PATH?</h3></summary>
  
<b>환경</b> : Windows 11, Visual studio 2019, Yolov4, CUDA 11.7, TensorRT-8.6.1.6
<br>
<b>증상</b> : (TensorRT + yolov4) trt_yolo.py 실행 시 오류 발생
<br>
<b>원인</b> : CUDA 폴더에 TensorRT dll이 포함되어 있지 않아 발생
<br>
<b>해결 방안</b> : CUDA 폴더에 TensorRT dll 포함
<br>
<b>참고 링크 : </b> [링크](https://cloud.tencent.com/developer/article/2169877)

</details>

<br>
