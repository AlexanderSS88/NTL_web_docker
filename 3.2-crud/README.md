sudo docker build . -t=second_hw

sudo docker run -d -e DEVELOP="False" -p 8000:88 second_hw
