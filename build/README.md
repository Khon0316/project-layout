# `/build`

패키징과 CI(Continuous Integration).

클라우드(AMI), 컨테이너(Docker), OS (deb, rpm, pkg) 패키지 설정들과 스크립트를 `/build/package` 디렉토리에 두세요.

CI (travis, circle, drone) 설정과 스크립트는 `/build/ci` 디렉토리에 두세요.
어떤 CI 도구들(예, Travis CI)들은 설정파일의 위치에 대해 매우 까다로운 편입니다.
(가능하면) `/build/ci` 디렉토리에 설정 파일들을 위치 시키고 CI 도구가 원하는 곳에 파일을 링크 시켜 보세요.


예제들:

* https://github.com/cockroachdb/cockroach/tree/master/build
