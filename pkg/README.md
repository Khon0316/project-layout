# `/pkg`

외부 애플리케이션에 의해 사용이 가능한 라이브러리 코드(예시, `/pkg/mypubliclib`).

다른 프로젝트들은 잘 동작하기를 기대하면서 이 라이브러리들을 임포트 할 것입니다. 그래서 여기에 무엇인가를 추가할 때는 신중해야 합니다. :-) 프라이빗 패키지를 임포트 불가하도록 하기위한 방법은 Go에 의새 강제 되는 `internal` 디렉토리입니다.
`/pkg`은 다른 이들이 사용하기에  이 디렉토리에 코드는 안전하다는 커뮤니테이션을 명시적으로 할 수 있는 좋은 방법입니다.

Travis Jeffery의 [`I'll take pkg over internal`](https://travisjeffery.com/b/2019/11/i-ll-take-pkg-over-internal/) 블로그 포스트는  `pkg`와 `internal` 디렉토리의 좋은 개요와 사용에 대한 이해를 제공합니다.

프로젝트 루트 디렉토리에 Go 가 아닌 컴포넌트와 디렉토리를 많이 포함하고 있을 때 다양한 Go 툴들을 쉽게 실행할 수 있도록 코드를 한곳에 그룹핑 해 주는 방법을 제공한다(이 영상들에서 언급한것 처럼: [`Best Practices for Industrial Programming`](https://www.youtube.com/watch?v=PTE4VJIdHPg) from GopherCon EU 2018, [GopherCon 2018: Kat Zien - How Do You Structure Your Go Apps](https://www.youtube.com/watch?v=oL6JBUk6tj0) 그리고 [GoLab 2018 - Massimiliano Pippi - Project layout patterns in Go](https://www.youtube.com/watch?v=3gQa1LWwuzk)).

이 레이아웃 패턴을 사용하는 유명한 Go 리포지토리를 보려면 [`/pkg`](pkg/README.md)를 참고하세요.
이 패턴을 일반적이지만, 보편적으로 받아들여 지는 것은 아니며 일부 Go 커뮤니티에서는 추천하지 않기도 합니다.


앱 프로젝트가 정말 작거나 중첩 레벨을 추가하는 것이 별로 가치가 없거나(또는 정말 원치 않는다면 :-)) 이 패턴을 사용하지 않아도 괜찮습니다.
프로젝트가 충분히 커져서 루트 디렉토리가 정말 붐빌 때(특히, Go가 아닌 컴포넌트가 많을 때)를 고려해 보세요. 

예제들:

* https://github.com/prometheus/prometheus/tree/master/pkg
* https://github.com/jaegertracing/jaeger/tree/master/pkg
* https://github.com/istio/istio/tree/master/pkg
* https://github.com/GoogleContainerTools/kaniko
* https://github.com/google/gvisor/tree/master/pkg
* https://github.com/google/syzkaller/tree/master/pkg
* https://github.com/perkeep/perkeep/tree/master/pkg
* https://github.com/minio/minio/tree/master/pkg
* https://github.com/heptio/ark/tree/master/pkg
* https://github.com/argoproj/argo/tree/master/pkg
* https://github.com/heptio/sonobuoy/tree/master/pkg
* https://github.com/helm/helm/tree/master/pkg
* https://github.com/kubernetes/kubernetes/tree/master/pkg
* https://github.com/kubernetes/kops/tree/master/pkg
* https://github.com/moby/moby/tree/master/pkg
* https://github.com/grafana/grafana/tree/master/pkg
* https://github.com/influxdata/influxdb/tree/master/pkg
* https://github.com/cockroachdb/cockroach/tree/master/pkg
* https://github.com/derekparker/delve/tree/master/pkg
* https://github.com/etcd-io/etcd/tree/master/pkg
* https://github.com/oklog/oklog/tree/master/pkg
* https://github.com/flynn/flynn/tree/master/pkg
* https://github.com/jesseduffield/lazygit/tree/master/pkg
* https://github.com/gopasspw/gopass/tree/master/pkg
* https://github.com/sosedoff/pgweb/tree/master/pkg
* https://github.com/GoogleContainerTools/skaffold/tree/master/pkg
* https://github.com/knative/serving/tree/master/pkg
* https://github.com/grafana/loki/tree/master/pkg
* https://github.com/bloomberg/goldpinger/tree/master/pkg
* https://github.com/crossplaneio/crossplane/tree/master/pkg
* https://github.com/Ne0nd0g/merlin/tree/master/pkg
* https://github.com/jenkins-x/jx/tree/master/pkg
* https://github.com/DataDog/datadog-agent/tree/master/pkg
* https://github.com/dapr/dapr/tree/master/pkg
* https://github.com/cortexproject/cortex/tree/master/pkg
* https://github.com/dexidp/dex/tree/master/pkg
* https://github.com/pusher/oauth2_proxy/tree/master/pkg
* https://github.com/pdfcpu/pdfcpu/tree/master/pkg
* https://github.com/weaveworks/kured/pkg
* https://github.com/weaveworks/footloose/pkg
* https://github.com/weaveworks/ignite/pkg
* https://github.com/tmrts/boilr/tree/master/pkg
