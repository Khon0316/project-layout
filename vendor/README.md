# `/vendor`

애플리케이션 종속성(수동으로 또는 [`Go Modules`](https://github.com/golang/go/wiki/Modules) 같은 새롭게 내장된 종속성 관리 도구에 의해 관리됨)
`go mod vendor` 명령은 `/vendor` 폴더를 만들게 됩니다.
`-mod=vendor` 옵션이 기본값인 Go 1.14 를 사용하지 않는다면 `go build` 명령에 해당 옵션이 필요할 수도 있습니다.

라이브러리를 빌딩 중이라면 애플리케이션 종속성 폴더를 커밋하지 마세요.

Go [`1.13`](https://golang.org/doc/go1.13#modules)부터 모듈 프록시 기능을 활성화 되었습니다(기본 프록시 서버로 [`https://proxy.golang.org`](https://proxy.golang.org) 사용). 
이 기능이 여러분의 요구와 제약사항에 부합하는지 확인하려면 [`여기`](https://blog.golang.org/module-mirror-launch)를 읽어 보세요.
만약 부합한다면 `vendor` 디렉토리는 전혀 필요하지 않습니다.
