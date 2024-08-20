아주 간단하게 시작할 수 있습니다.
mac 기준입니다.
windows, linux도 가능합니다.
https://spring.io/projects/spring-ai

java는 17 이상 가능합니다.

이제 시작해 보겠습니다.
```
spring boot new --from ai --name okai
```

여기 오타 있어요.
> ./mvw spring-boot:run

`./mvnw spring-boot:run` 입니다.
mvn 있으면 `mvn spring-boot:run` 도 가능합니다.

ㅠㅠ 망했습니다.
jdk를 17로  맞추어서 다시 해 보겠습니다.

OPENAI 키가 설정이 되어야 됩니다.
https://platform.openai.com

```
SPRING_AI_OPENAI_API_KEY=sk-proj-gTvn8IQBwfjO30KXMDWEOX-7ED07J-aqj87HrlGAPyWVJzuj- mvn spring-boot:run
```
으로 떴습니다.
http://localhost:8080

이상입니다.
좋은 하루 되시길 바랍니다. 시청 감사합니다.🙇🏻‍♂️

openai key 때문에 업로드가 안 된 것이었네요.
키는 삭제합니다.
