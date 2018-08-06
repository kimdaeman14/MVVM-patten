# MVVM-patten


MVC patten 같은경우에는 
컨트롤러가 모델에 접근할때   let student = stdent() 처럼 만들고 student.---해서 하잖아.

근데 MVVM 같은 경우에는 그런거야. 옵저빙하고 바인딩이란게 있어.뭐냐면
모델에 값이 바뀌면 vm(뷰모델)에서 그걸 옵저빙하고 있다가 그걸 뷰에 바인딩해줘서 아무런 액션이나 뭘 안해줘도 자동으로 값이 바뀌게 하는거야. 
그러려면 뷰모델에서는 옵저빙할수있는 로직이 미리 있어야겠고, 그걸 바인딩해서 맵핑해주는 로직도 있어야 될거야. 
그러니까 접근하는 방법 자체가 다른거지 MVC랑은 




MVC 구조는 분명 장점이 많지만 반대로 한계도 존재합니다. 가장 대표적인 것이 Model에 넣기도 애매하고, View에도 넣기 애매한 코드들은 모두 Controller에 들어가게 되어 Controller가 비대하진다는 점입니다. 이를 'Massive View Controller'의 문제라고도 합니다. MVC의 앞자를 따 풍자한 것이기도 합니다.

예를 들면, 날짜 데이터를 각 국가별 양식으로 포맷하는 코드는 Model과 View 양쪽 어디에도 넣기 좀 애매합니다. 비즈니스 로직이나 데이터라고 보기도 어렵고, UI라고 보기도 어렵기 때문입니다. 결국 이와 같은 Formatting을 담당하는 코드들은 Controller에 들어가게 되어 Controller를 비대하게 만듭니다. 이 'Massive View Controller' 문제를 해결하기 위해 MVVM 패턴이 대안으로 제시되고 있습니다.
MVVM이란?
MVVM은 Model-View-View Model의 약자로 MVC에 View Model을 추가한 것입니다. 새로 추가된 View Model은 Controller를 대신해 Formatting을 비롯한 코드들은 다루게 됩니다. 이에 따라 Controller 부담이 경감됩니다. 프로그래밍 언어에 따라 View Model이 아예 Controller를 대체하기도 하지만 iOS의 View Model은 Data Binding 부분이 다소 취약하여 Controller를 완전히 없앨 수는 없습니다. 


iOS에서의 MVVM은 MVC와 아주 큰 차이는 없습니다. MVVM의 주요 특징은 다음과 같습 니다.

    · Controller는 더 이상 Model에게 말을 걸 수 없습니다. View Model을 통합니다.
    · Model과 View Model이 하나의 짝을 이루고, View와 Controller가 짝을 이루는 구조가 됩니다.
    · View Model은 Presentation Logic을 다루게 됩니다. 하지만 UI는 다루지 않습니다. (UIKit import 금지) 

 
 
