# 手把手的深度學習實務
## 課前準備: 安裝 Keras
1. 安裝 Keras，請依 https://github.com/tw-cmchang/hand-on-dl/blob/master/keras_installation.pdf 安裝說明。
2. 下載 https://github.com/fchollet/keras/blob/master/examples/mnist_mlp.py 這份範例程式並執行測試。
```python
python mnist_mlp.py
```
+ 若能成功執行，表示安裝成功。
+ 由於作業系統環境因人而異，若有任何安裝上的問題，請不吝來信詢問: cmchang@iis.sinica.edu.tw 或 chihfan@iis.sinica.edu.tw。先謝謝大家的海涵，希望各位能在 12/18 上課前完成安裝流程，謝謝！

## (optional) 安裝運算加速庫
1. 下載並執行 https://github.com/tw-cmchang/hand-on-dl/blob/master/checkblas.py 測試是否有安裝運算加速庫。
2. 安裝 Anaconda 的學員，也確認是否有通過 checkblas.py 測試。儘管 Anaconda 內有 mkl 運算加速庫。
3. 安裝 openblas，請依 https://github.com/tw-cmchang/hand-on-dl/blob/master/openblas_installation.pdf 。
4. 另外，若需要安裝 openblas 可至 https://drive.google.com/drive/folders/0ByfnsehogjWtbndTY3JncE95bjQ 下載 (謝謝 Chih-Fan)。

## 下載課程程式碼與資料集
1. 請至 http://mmnet.iis.sinica.edu.tw/~cmchang/hand-on-dl.zip 下載。
2. 跟各位學員致歉，因近日伺服器有些不穩，若上方連結失效，可至 https://drive.google.com/open?id=0By9xOgk3An1wSlRVX2JvUElicnM 下載。

## Questions
+ 有學員回報在 win10 安裝 Anaconda 後，使用 pip install theano/ pip install keras 出現下方錯誤訊息：
```pyhon
UnicodeDecodeError: 'ascii' codec can't decode byte 0xb8 in position 0: ordinal not in range(128)
```
此為 Anaconda2 的預設編碼問題。請在 Anaconda2\Lib\site-packages 裡增加一個 sitecustomize.py，內容如下：
```python
import sys 
sys.setdefaultencoding('gbk')
```
之後在 pip install theano/keras 試試看，若有問題請再來信。謝謝該位熱心的同學提供解法 :)。
