## REPL

콘솔에서 node 라고 치면 그대로 콘솔로 사용가능

## console

console.time(레이블) - console.timeEnd(레이블) : 이 사이의 시간 측정
console.log(내용) - 평범한 로그를 표시, 콤마로 여러내용 동시처리 가능
console.error(에러 내용) - 에러를 콘솔에 표시
console.table(배열) - 배열의 요소로 객체 리터럴을 넣으면 테이블형식으로 나옴
console.dir(객체, 옵션) - 객체를 콘솔에 표시할때 사용, (obj, {colors: ture, depth: 2}) 형식으로 넣으며 옵션으로 색과 깊이를 지정 (default depth = 2)
console.trace(레이블) - 에러 위치 추적

## timer

setTimeout(콜백함수, 밀리초) - 밀리초 이후 콜백 실행
setInterval(콜백함수, 밀리초) - 밀리초 마다 콜백 실행
setImmediate(콜백함수) - 콜백함수 즉시실행 setTimeout(콜백,0) 과 거의 같지만 setTimeout0은 사용하지 않는것을 권장

clearTimout(아이디) - setTimeout 취소
clearInterval(아이디) - setInterval 취소
clearImmediate(아이디) - setImmediate 취소

## __filename, __dirname

__filename - 현재파일의 경로와 파일명
__dirname - 현재파일의 경로

## process.nextTick(콜백)

timer와 axios 보다 먼저 실행됨
promise 와 같은 우선순위
마이크로태스크 큐에 배치
