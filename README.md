## 리액트 워드 클라우드 웹 앱 프로젝트: Flask Python 모듈

### API 구축 방법
```
git clone https://github.com/ndb796/ReactWordCloudWebApp-Python.git
cd ReactWordCloudWebApp-Python
python word_cloud.py
# 리눅스에서는 다음과 같이 수행
sudo python3 word_cloud.py
# Ctrl + Z
bg
disown -h
```
### API 호출 예제
> [워드 클라우드 생성] URL: http://localhost:5000/process
```json
{
  "textID": "1",
  "text": "안녕하세요? 저는 한국교원대학교 나동빈입니다. 여러분들과 함께 다양한 공부를 진행하면서 스터디에 참여하고 싶어요. 한 번 공부를 할 때 제대로 공부를 하는 것이 목표입니다. 공부는 쉽지 않지만 열심히 하다 보면 재미를 느끼고 참여할 수 있을 것 같아요.",
  "maxCount": 15,
  "minLength": 2,
  "words": {"1":{"weight":"7","word":"스터디"},"2":{"weight":"5","word":"참여"},"3":{"weight":"5","word":"분노"},"4":{"weight":"4","word":"치킨"}},
  "stopwords": {"1": {"word": "그"}, "2": {"word": "저"}}
}
```
> [워드 클라우드 보기] URL: http://localhost:5000/outputs
```
http://localhost:5000/outputs?textID=1
```
> [가중치 정보 보기] URL: http://localhost:5000/weights
```json
{
  "textID": "1",
  "text": "안녕하세요? 저는 한국교원대학교 나동빈입니다. 여러분들과 함께 다양한 공부를 진행하면서 스터디에 참여하고 싶어요. 한 번 공부를 할 때 제대로 공부를 하는 것이 목표입니다. 공부는 쉽지 않지만 열심히 하다 보면 재미를 느끼고 참여할 수 있을 것 같아요.",
  "maxCount": 15,
  "minLength": 2,
  "words": {"1":{"weight":"7","word":"스터디"},"2":{"weight":"5","word":"참여"},"3":{"weight":"5","word":"분노"},"4":{"weight":"4","word":"치킨"}},
  "stopwords": {"1": {"word": "그"}, "2": {"word": "저"}}
}
```

### Reboot
```
* Check the freenom domain service.
* Check the cloudflare service.
* Open terminal with administrator authorization.
* Connect to server instance using ssh.
sudo netstat -nap | grep 80
* Terminate the process that uses 80 port.
sudo kill -9 {PID}
cd KnueWordCloud-Python
* Run the wordcloud server.
sudo python3 word_cloud.py
* [Ctrl + Z]
bg
disown -h
```
