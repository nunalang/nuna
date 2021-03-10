# nuna
(우리의 가상) 누나 언어 v0.3

### 스택
스택은 스택 번호, 값들으로 이뤄져야 합니다
값은 정수입니다

만약 오류가 난 경우에는 그 자리에서 오류를 알려주고 프로그램이 작동을 중단해야 합니다

### 키워드
* `눈`, `누`는 값이 `1`인 스택을 만듭니다 (예외, 뒤에 `.`가 있으면 `.`의 길이의 수만큼을 값으로 합니다)
* `난`, `나`는 현재 스택에 `1`을 곱합니다 (예외, 뒤에 `.`가 있으면 `.`의 길이의 수만큼 곱합니다)
* `주`는 현재 스택에 `1`을 뺍니다 (예외, 뒤에 `.`가 있으면 `.`의 길이의 수만큼 뺍니다)
* `거`는 현재 스택에 `1`을 더합니다 (예외, 뒤에 `.`가 있으면 `.`의 길이의 수만큼 더합니다)
* `헤`는 현재 스택을 `POP`합니다.
* `으`은 앞의 스택의 값입니다. `.` 대신 사용 할 수 있습니다
* `응`는 현재 스택 앞의 내용과 현재 스택의 내용을 뺍니다 (현재 스택 앞의 스택은 삭제 됩니다)
* `흐`는 `2^(뒤에 있는 점 개수)`이고 마지막에는 무조건 `읏`으로 끝납니다
* `💕`는 현재 스택 앞의 내용과 현재 스택의 내용을 합칩니다 (현재 스택 앞의 스택은 삭제 됩니다)
* `!`는 스택을 UTF-8 인코딩으로 문자 출력(stdout)를 합니다

`눈` `누`, `난`, `나`, `주`, `거`, `.`, `헤`, `으`, `응`, `흐`, `읏`, `💕`, `!`가 아닌 다른 문자들은 문법 오류입니다

없는 스택에 접근할 경우 그 값은 `0`으로 간주합니다

`POP`은 스택의 마지막 값을 출력 없이 삭제하는 것을 의미합니다

만약 키워드 뒤에 `.`가 없다면 숫자가 `0`이 아닌 `1`로 간주합니다

#### 예제
```
눈나..흐.....읏..나주..거....흐...읏...
누..나..나...흐....읏..나주..거....💕
눈나.....나..흐...읏나.....주거...💕
누나..흐..읏나.......주..거......응읏..!

눈나..으흐읏
누으나.....주..흐....읏나....응
누나.....나..주...읏나......응!
```
* @pmh-only님이 제작하셨습니다
* 출력 결과: 누나

#### 구현체
[C++로 제작한 nuna interpreter by hui1601](https://github.com/hui1601/nuna-interpreter)

[Python으로 제작한 nuna interpreter by pl-Steve28-lq](https://github.com/pl-Steve28-lq/PyNuna)

[Node.js로 제작한 nuna interpreter by franknoh](https://github.com/franknoh/nuna-interpreter)

#### 주의
이 언어의 작가는 현재 누나가 없으며 (미래에도 없을 예정), 이 언어는 미니멀리즘을 추구합니다

##### latest release
* 3월 7일 16:40(24h)
