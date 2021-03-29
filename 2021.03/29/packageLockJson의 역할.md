# package-lock.json의 역할

package-lock.json 은 npm 을 사용하여 node_modules 구조나 package.json 이 수정되고 생성될 때 
당시 의존성에 대한 정확하고 구체적인 정보를 품고 자동으로 생성됩니다. (package.json에는 버전이 range로 명시되기때문)
package-lock.json이 있으면 npm install 을 할때 package-lock.json을 사용하게 된다.

만약 A와 B가 같이 작업을 하는데 A가 먼저 작업을 끝내고 node_module 과 package-lock.json 을 제외하고 git에 push 를 한후 
B가 pull 을 받아서 npm install 을 하였는데 의존성 트리의 일부 버전이 다르게 설치되었으면
A가 작업을 했던것에서 B가 오류가 생길수 있다.

package-lock.json이 있으면 모든 의존성 트리의 버전이 동일하게 설치되므로 같은 환경에서 개발하게 된다.