https://okdevtv.com/mib/nutch

더그 커팅이라는 전설적인 개발자가 있습니다.
자바를 배워볼까? 그냥 문법만 알면 심심하니까, 뭐 하나 만들면서 자바를 배우자 해서 만든 게 검색엔진 Lucene입니다.
https://lucene.apache.org

검색엔진 만들고 보니 검색할 게 필요했죠. 그래서 만든 게 웹 크롤러 nutch 입니다. https://nutch.apache.org

웹 크롤러로 웹페이지들을 긁다 보니, 저장 공간이 필요해지죠.
그래서 만든 게 hadoop입니다. https://hadoop.apache.org

이중에서 넛치를 돌려 보겠습니다.

구글 클라우드에 크레딧이 40만원 정도 있는데, 그거 사용해야 할 것 같아서 aws가 아닌 구글로 진행하겠습니다. 11/25까지 90일 크레딧입니다. 날짜 지나면 사라집니다.

https://console.cloud.google.com/

40만원 거의 다 남아 있어서 메모리 16G에 cpu 4개 짜리사용합니다.
aws는 t2.2xlarge 정도 될 겁니다.

gcloud는 브라우저 인증이 필요하고, 또는 gcloud cli를 설치해야 됩니다.

---
일단 zsh 부터 설치하겠습니다.
https://okdevtv.com/mib/zsh

```
Failed to set locale, defaulting to C.UTF-8
```

이 메시지는 /etc/environment 에 설정해 주면 됩니다.
`sudo vi /etc/environment`

```
LANG=en_US.UTF-8
```

환경은 세팅이 되었고, 이제 자바 설치입니다.
https://okdevtv.com/mib/sdkman

```
sdk install java 11.0.24-amzn
```

구글 클라우드 서버에 amazon jdk를 설치합니다. ^^;

nutch를 다운 받고, 압축을 풀었습니다.
기본 튜토리얼을 요약한 페이지입니다.

user agent 꼭 넣어야 됩니다. 그래야 동작합니다.

```sh
echo "export JAVA_HOME=~/.sdkman/candidates/java/current" >> ~/.zshrc
. ~/.zshrc
```

한글이 다 깨지죠. ㅠㅠ
다시 접속하겠습니다.

테스트는 잘 되었습니다.
다음 단계는 seed urls 등록입니다.

바로 긁어 보겠습니다.

헐
+https://openai.com/gptbot)
얘 뭐야? 헐
엄청 긁어 가네요 ㄷㄷㄷ
1초마다 ㄷㄷㄷ gptbot

nutch의 기본 딜레이 시간은 5초입니다.
### Solr

```sh
sudo vi /etc/security/limits.conf
```

```
* hard nofile 65535
* soft nofile 65535

* hard nproc 65535
* soft nproc 65535
```

### Crawling with n iterations

```shell
bin/nutch inject crawl/crawldb urls
nohup bin/crawl crawl 2 &
```

2 loop만 돌렸습니다.
이렇게 쌓인 텍스트를 solr에 집어넣습니다.

```
#!/bin/zsh

# Nutch Indexing Script with Automatic Segment Detection

# Define the path to the segments directory
CORE_NAME="crawl"
SEGMENTS_DIR="$CORE_NAME/segments"

# Check if the segments directory exists
if [ ! -d "$SEGMENTS_DIR" ]; then
    echo "Error: $SEGMENTS_DIR directory not found."
    exit 1
fi

# Read segment folders into an array
segments=($(ls -1 "$SEGMENTS_DIR"))

# Check if any segments were found
if [ ${#segments[@]} -eq 0 ]; then
    echo "No segments found in $SEGMENTS_DIR."
    exit 1
fi

echo "Found ${#segments[@]} segments to process."

# Loop through each segment and run the indexing command
for segment in "${segments[@]}"; do
    echo "Indexing segment: $segment"
    bin/nutch index $CORE_NAME/crawldb -linkdb $CORE_NAME/linkdb "$SEGMENTS_DIR/$segment" -filter -normalize -deleteGone

    # Check if the command was successful
    if [ $? -eq 0 ]; then
        echo "Successfully indexed segment: $segment"
    else
        echo "Error indexing segment: $segment"
    fi

    echo "------------------------"
done

echo "All indexing tasks completed."
```

aws말고 gcp는 포트 열기가 ㅠㅠ
익숙하지 않아서 8983 열어 보겠습니다.

AI 없었으면, 구글링 삽질 엄청했을 겁니다. ㅠㅠ
아, 참고로 skt 사용자는 https://perplexity.ai 1년간 사용료 대신 내줍니다.
` 24년 9월 4일부터 _skt_ 이용자_는_ 1년간 무료로 이 서비스를 이용할 수 있습니다`

오늘 네트워크가 많이 느리네요 ㅠㅠ

이제 nutch 라는 core를 만들고 거기에 크롤링한 데이터를 붇겠습니다.

```python
import requests

# Solr 쿼리 URL
url = "http://localhost:8983/solr/nutch/select?indent=true&q.op=OR&q=*%3A*"

# GET 요청 보내기
response = requests.get(url)

# JSON 형식으로 데이터 파싱
data = response.json()

# 유니크한 호스트 추출
unique_hosts = set()
for doc in data['response']['docs']:
    if 'host' in doc:
        unique_hosts.update(doc['host'])

# 결과 출력
print("Unique hosts:")
for host in unique_hosts:
    print(host)
 # type: ignore

```

여튼 여기까지입니다.
시청 감사합니다.

아마 7시부터 불꽃 축제가 시작되겠죠. 좋은 밤 되시길 바랍니다.

하고 끝난 줄 알았죠?

방송 초반 삽질 다시 반복할께요.
GCP 인스턴스부터 다시 만들게요.

