# `/internal`

비공개(private) 애플리케이션 / 라이브러리 코드.

다른 애플리케이션이나 라이브러리에 임포트되길 원하는지 않는 코드들입니다.
Go 컴파일러 자체에서 강제되는 레이아웃 패턴입니다.
더 자세한 사항은 Go 1.4 [`release notes`](https://golang.org/doc/go1.4#internalpackages)을 참고하세요.
`internal`는 최상위 레벨 디렉토리에만 적용되는 것은 아닙니다.
프로젝트 트리의 어느 레벨에서든 하나 이상의 `internal` 디렉토리를 적용할 수 있습니다.
공유할 것과 공유하지 않을 코드를 나누기 위해 인터널 패키지에 구조를 더 추가할 수 있습니다.
이 패턴은 (특히, 작은 규모의 프로젝트에서는) 필수는 아닙니다만, 의도된 패키지 사용을 보여주는 좋은 시각적 단서 입니다. 
실제 애플리케이션 코드를 `/internal/app`(예시, `/internal/app/myapp`)에 위치 시킬 수 있고 이 앱들이 공유하는 코드는  `/internal/pkg`(예시, `/internal/pkg/myprivlib`) 디렉토리에 위치 시킬 수 있습니다.

예제들:

* https://github.com/hashicorp/terraform/tree/master/internal
* https://github.com/influxdata/influxdb/tree/master/internal
* https://github.com/perkeep/perkeep/tree/master/internal
* https://github.com/jaegertracing/jaeger/tree/master/internal
* https://github.com/moby/moby/tree/master/internal
* https://github.com/satellity/satellity/tree/master/internal
