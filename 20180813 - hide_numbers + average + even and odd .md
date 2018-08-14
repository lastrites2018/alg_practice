- 전화번호 가리기 문제

풀었으나 정규표현식을 사용하면 훨씬 깔끔하고 훌륭하게 풀 수 있다.

기본적인 사용법 정도는 익히도록 하자. 

```javascript
다른 사람 풀이 (정규표현식 사용)


function hide_numbers(s) {
  return s.replace(/\d(?=\d{4})/g, "*");
}

정규표현식 간단 배우기
자바스크립트에서는 정규식을 /.../로 묶어준다. (출처 https://blog.outsider.ne.kr/141)
var pattern = /rules/;

                             
^ : 시작표시(매칭이 처음부터 되어야 함)
$ : 끝표시(문자열 끝에 매칭되어야 함)
[] : 문자열 set
      [ab][a-z][0-9] 라고 써주면 첫글자는 a또는 b이고 그 다음에 a~z가 나오고 그 뒤에 0~9가 나온다는 뜻..
[]안에서 ^쓰면 그 문자가 아닌것들
* : 0번 이상 반복
+ : 1번 이상 반복
? : 0 또는 1회
{} : 횟수 표시
[a]{2}이면 aa이고 [a]{2,}이면 a가 2개 이상인거 [a]{2, 4}이면 aa, aaa, aaaa 이다.
\d : 숫자, [0-9]와 같음
\D : 숫자가 아닌 것들 [^0-9]와 같음
| : Or의 뜻
{} : 그룹을 묶어 준다.
. : 뉴라인(\n)제외한 한 문자 (진짜 .을 찍기 위해선 \.으로 표시해야 한다.)
               
                             
옵션 /rules/ig 와 같이 써준다.

g : 글로벌의 뜻. 전역 매칭을 한다. 처음부터가 아닌 전체에서 정규식이 맞는걸 찾는다. 
i : case Insensitive, 대소문자 구별안함
m : Multiline
```

https://regex101.com/r/hL4vY1/1 정규표현식 번역기

https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/%EC%A0%95%EA%B7%9C%EC%8B%9D



- 평균 구하기

```javascript
다른 사람 풀이
es6 reduce는 이렇게 깔끔하게 풀 수 있다.
function average(array){
  return array.reduce((a, b) => a + b) / array.length;
}

내 풀이
생각해 볼 개선점 : 무의미한 함수명을 좀 더 유의미한 함수명으로

function solution(arr) {
    var sum = arr.reduce(function(a, b){return a+b;});    
    return sum / arr.length;
}
```



- 짝수와 홀수

```javascript
다른 사람 풀이
function evenOrOdd(num) {
  return num % 2 ? "Odd" : "Even";
}


내 풀이 
개선점 : 함수명 수정하기
function solution(num) {
    if (num % 2 === 0) {
        return "Even";
    } else {
        return "Odd";
    }
}

```



```javascript
자바스크립트 
반올림 : Math.round(number);
올림 : Math.ceil(number);
버림 : Math.floor(number)

```

