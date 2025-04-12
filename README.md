# Arduino-MPU6050
Arduino project utilizing MPU6050 sensor for measuring acceleration and gyroscope information, accompanied by a PLOTTER script that displays motion data through Arduino Serial Plotter.
# MPU6050 Motion Plotter
這是一個搭配Arduino開發板使用的MPU65050偵測器，透過 Serial Plotter 即時顯示六軸運動資料（加速度 + 角速度）。
# 專案內容
- `mpu6050_plot.ino`：主程式。初始化 MPU6050，並以序列格式輸出六軸資料，供 Serial Plotter 繪圖。
- `.gitignore`：忽略 Arduino 編譯產物與本地設定。
- `README.md`：你正閱讀的這份說明文件。
# 硬體需求
- Arduino UNO / Nano / Mega
- Mpu6050模組
- 杜邦線數條
# 接線方式
| MPU6050 腳位 | Arduino UNO/Nano |
|--------------|------------------|
| VCC          | 5V               |
| GND          | GND              |
| SDA          | A4               |
| SCL          | A5               |
# Plotter功能說明
使用 **Serial Plotter** 將下列六個數據以圖像方式顯示：
- `Ax` / `Ay` / `Az`：加速度（m/s²）
- `Gx` / `Gy` / `Gz`：角速度（°/s）
# 使用說明
1. 將Arduino 接上MPU6050感測器
2. 將程式上傳至 Arduino
3. 打開 **序列埠監控視窗**
4. 揮動感測器，觀察即時波形變化
# 備註
本專案可選擇使用 [I2Cdevlib](https://github.com/jrowberg/i2cdevlib) 提供的 MPU6050 library，或使用 Wire 庫手動讀取暫存器。
# License
MIT License — 自由使用，誠摯歡迎 fork、改寫、再創作。
