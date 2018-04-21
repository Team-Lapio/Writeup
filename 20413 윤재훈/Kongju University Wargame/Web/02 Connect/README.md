# Connect (Web)

웹 두 번째 문제인 `Connect` 문제이다.

![Image](https://github.com/JaehunYoon/Writeup/blob/Draft/20413%20%EC%9C%A4%EC%9E%AC%ED%9B%88/Kongju%20University%20Wargame/Web/02%20Connect/Image/01%20Index.PNG)

다음은 `Connect` 페이지에 접속하게 되면 가장 먼저 뜨는 html 페이지이다.

```
CONNECT
-------
Referer : wantconnection
User-Agent : Iwant!!!!
```

다음과 같은 형태로 페이지에 표시되고 있는데,

이를 보면 아마 `Go` 버튼을 눌러 이동한 페이지의 `Referer`, `User-Agent` 값을 임의로 지정하면 문제가 풀릴 것이라고 짐작할 수 있다.

![Image](https://github.com/JaehunYoon/Writeup/blob/Draft/20413%20%EC%9C%A4%EC%9E%AC%ED%9B%88/Kongju%20University%20Wargame/Web/02%20Connect/Image/02%20connection.PNG)

다음은 `Go` 버튼을 눌러서 이동한 페이지이다.

```
CONNECTION
----------
Nop!
```

위와 같은 형태로 표시되어 있는 것을 보면 문제에서 요구하는 `Referer`, `User-Agent` 값으로 번경해주지 않아, `Nop!`을 출력하고 있다고 보았다.

![Image](https://github.com/JaehunYoon/Writeup/blob/Draft/20413%20%EC%9C%A4%EC%9E%AC%ED%9B%88/Kongju%20University%20Wargame/Web/02%20Connect/Image/03%20fiddler%20open.PNG)

문제에서 요구하는 `Referer`, `User-Agent` 값을 설정해주기 위해서 웹 프록시 툴인 `Fiddler 4`를 이용할 것이다.

![Image](https://github.com/JaehunYoon/Writeup/blob/Draft/20413%20%EC%9C%A4%EC%9E%AC%ED%9B%88/Kongju%20University%20Wargame/Web/02%20Connect/Image/04%20change%20values.PNG)

다음과 같이 `Unlock for Editing`으로 문제에서 요구하는 값을 충족시켜주기 위해 수정을 한 후, `Replay`를 해준다.

![Image](https://github.com/JaehunYoon/Writeup/blob/Draft/20413%20%EC%9C%A4%EC%9E%AC%ED%9B%88/Kongju%20University%20Wargame/Web/02%20Connect/Image/05%20flag.PNG)

`Replay`를 눌러 요구한 값을 충족시킨 후 적용한 새 페이지의 소스 코드를 잘 살펴보면, `flag` 값이 출력된 것을 확인할 수 있다.

**FLAG : flag is {Us3r_Ag3nt_@nd_R3f3r3r}**