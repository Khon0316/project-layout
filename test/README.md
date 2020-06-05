# `/test`

추가적인 외부 테스트 앱과 테스트 데이터.
`/test`는 원하는대로 자유롭게 구조화 해도 됩니다. 
큰 프로젝트에서는 데이터 서브 디릭토리를 만들기도 합니다.
예를 들면, Go가 디렉토리 내부 내용을 무시 하는 `/test/data` 또는 `/test/testdata` 를 만들 수 있습니다. 
Go는 "." 또는 "_"ㅣ 로 시작하는 디렉토리와 파일 또한 무시합니다. 그래서 테스트 데이터 디렉토리 이름을 좀더 유연하게 정할 수 있습니다.

예제들:

* https://github.com/openshift/origin/tree/master/test (test data is in the `/testdata` subdirectory)


