# `/cmd`

프로젝트를 위한 메인 애플리케이션들.

각 애플리케이션의 디렉토리 이름은 원하는 실행파일의 이름과 동일해야 합니다(예, `/cmd/myapp`).
애플리케이션 디렉토리에 많은 코드를 두지 마세요.
다른 프로젝트에서 임포트되고 사용되는 것을 고려한다면 코드는 `/pkg` 디렉토리에 있어야 합니다.
재사용이 불가하거나 재사용을 원치 않는 코드는 `/internal` 디렉토리에 두세요.
다른 사람들이 어떻게 사용할지 모르니, 확실히 의도를 밝혀주세요.
일반적으로 `/internal`과 `/pkg`폴더에서 코드를 임포트하고 호출하는 짧은 `main` 함수를 작성합니다.

예제들:

* https://github.com/heptio/ark/tree/master/cmd (just a really small `main` function with everything else in packages)
* https://github.com/moby/moby/tree/master/cmd
* https://github.com/prometheus/prometheus/tree/master/cmd
* https://github.com/influxdata/influxdb/tree/master/cmd
* https://github.com/kubernetes/kubernetes/tree/master/cmd
* https://github.com/satellity/satellity/tree/master/cmd/satellity
* https://github.com/dapr/dapr/tree/master/cmd

