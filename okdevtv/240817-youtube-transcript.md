https://npmtrends.com 에서 좋은 모듈을 찾아서 적용해 보려고 합니다.
제 모듈은 올린 게 있는데 쩌리입니다. ㅠㅠ
시작 쉘에 등록하면 콘솔창 열 때마다 마인드 다잡을 수 있습니다.
https://www.npmjs.com/package/devwords

유튜브 자막(youtube transcript) 가시죠.
사용 방법은 간단합니다.

pnpm i youtube-transcript
package.json 에서 `"type": "module"` 추가하면 동작합니다.

```js
import { YoutubeTranscript } from 'youtube-transcript';

YoutubeTranscript.fetchTranscript('videoId or URL').then(console.log);
```

결과는 json으로 잘 나옵니다.
```js
  {
    text: '라우터로 되어 있는데 그거를 이제',
    duration: 5.32,
    offset: 219.04,
    lang: 'ko'
  },
```

offset은 시작 시간으로 초입니다.
이걸 사용하는 모듈을 만들어서 텍스트만 추출하겠습니다.

```js
import { YoutubeTranscript } from "youtube-transcript";

test("getTextOnly", async () => {
  const videoId = "vSIb2sPdu9U";
  const transcript = await YoutubeTranscript.fetchTranscript(videoId);
  expect(transcript).not.toBeNull();
  const fullText = getTextOnly(transcript);
  expect(fullText).toContain("인데");
});

function getTextOnly(transcript) {
  return transcript.map((item) => item.text).join(" ");
}
```

테스트 코드는 완성이 되었고, 제 서비스에 이식하겠습니다.
ㄷㄱㄷㄱㄷㄱ

[object Object],
이게 머선 일인지
뜬금

거의 다 되었어요.
로컬에서는 테스트가 마친 것 같고, 서버에 배포해 보겠습니다.
오늘은 특별히 자화자찬 풀리퀘스트 날려야 할 것 같습니다.
🎉

보시는 분들
github.com/kenu/odevtube 오뎁튜브 star 눌러 주시면 감사합니다.


server 좀 정리해야겠네요 ㅠㅠ

now underconstruction🚧

이제 서버는 동작합니다만, transcript 이 씨방새를 어찌해야 하나요

