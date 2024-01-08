# *Block scope & Function scope의 차이*

- Block scope는 기본적으로 {BRACES}로 감싸진 것을 의미합니다. 예를들어, 조건문(if,else if,else) 반복문(for,while,do-while) 함수(function,=>{}) 객체리터럴,클래스,try-catch 가 있습니다. 그리고 Block scope는 let과 const과 연관이 있는데, 기존에 var로 변수를 선언하던 scope 문제를 해결하는데 아주 좋은 방법입니다. 그 이유는, var는 fucntion scope이기 때문에, 함수 안의 다른 블록들안에서 var로 선언된 변수들은 그 블록을 감싸고 있는 함수에서 hoisting되는 문제가 있어, 변수를 참조하고 호출 되는 시점에 문제가 생길수 있습니다.

- Function scope는 다른 블록들은 신경쓰지 않고 오로지 그 함수의 범위를 말하는 겁니다. 그런데, var로 선언하는 변수가 function scope의 범위를 갖게 되는데, 앞서 말한 것 처럼, 다른 블록에도 영향을 줄수 있기 때문에, 권장되는 방법은 아닙니다.
