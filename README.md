# **Втора лабораториска вежба по Софтверско инженерство**

## Бојан Робев, 185028

### -Група на код: 3

### -Слика од CFG:

![Screenshot_3](https://user-images.githubusercontent.com/61628838/84572009-80c0b000-ad97-11ea-886f-d75b1d6d6651.png)

### -Цикломатска комплексност:
21 Јазел

29 Ребра

10 Региони

E-N+2=29-21+2=10

P+1=9+1=10.

Цикломатската комплексност е : E - N + 2 или P + 1 или број на Региони = 10

### -Тест случаеви според everyBranch: 
6

### -Тест случаеви според MultipleConditions: 
12

### -Објаснување на напишаните unit tests:

а) Од everyBranch:
-Првите два теста ( A, B, T ; A, C, D, T ) се за да се тестираат exceptions, односно runtimeException, потоа следниот тест (A, C, E, F, T) е кога password-от и usernamed-от се исти, без разлика од големината на буквите, а тестот (  A, C, E, G, H, T ) е за тестирање на големината на password-от во случај кога е помал од 8. Потоа тестот ( A, C, E, G, I, J, K, Q, K, M, O, J.1, R, T ) е за поминување на сите гранки помеѓу if-овите ( кога нема да влезат во if-от во сите 3 if-a, односно се false ) и на крај тестот ( A, C, E, G, I, J, K, Q, L, M, N, O, P, J.1, S, T ) е за поминување на гранките кога if-овите се точни ( сите 3 ).

b) Од multipleCondition:
-Првите четири теста се во врска со следниот if: (user.getUsername()==null || user.getPassword()==null) и ги разгледувам сите можни комбинации на исходите, односно кога (username = null, password = null ), (username = null, password != null ),
(username != null, password = null ) и (username != null, password != null ).
-Потоа следните 8 теста се за следниот if: (!digit || !upper || !special) и исто како предходните тестови и овде ги разледувам сите можни комбинации каде што ги има 2^3 односно 8.
