# OCR-Tesseract-Cpp

Ubuntu

Install Tesseract by running below commands -

sudo add-apt-repository ppa:alex-p/tesseract-ocr
sudo apt-get update
sudo apt install tesseract-ocr
sudo apt install libtesseract-dev

Install OpenCV –
1.	Download the repo: https://github.com/jayrambhia/Install-OpenCV
2.	Go to Ubuntu/dependencies.sh and change lines
    install_dependency libgstreamer0.10-dev to install_dependency libgstreamer1.0-dev
    and
    install_dependency libgstreamer-plugins-base0.10-dev to install_dependency libgstreamer-plugins-base1.0-dev
3.	Follow the steps of https://github.com/jayrambhia/Install-OpenCV/blob/master/README.md to install in Ubuntu

Download pre-trained model from - 
https://github.com/tesseract-ocr/tessdata/raw/master/eng.traineddata

Move the model into directory - 
/usr/share/tesseract-ocr/4.00/tessdata/eng.traineddata

Compile code - 
g++ -O3 -std=c++11 basic_ocr.cpp `pkg-config --cflags --libs tesseract opencv` -o main_ocr

Run executable - 
./main_ocr <image_path>/<image>
