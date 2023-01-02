# 생성자(Initialization)

- 생성자 : 클래스, 구조체, 열거형에서 새 인스턴스를 사용하기 전 설정과 초기화를 수행하는 과정

클래스 및 구조체의 저장 프로퍼티는 인스턴스가 생성될 때 반드시 어떠한 값이 존재하여야 하므로 초기화를 수행한다.<br>
```swift
class Friend {
  var name: String?
  var age = 15  //프로퍼티가 항상 동일한 초기값을 사용하는 경우 default값을 설정
  
  init(_ name: String){
    self.name = name
    print("생성자 이름 : \(self.name)")
  }
}
```
옵셔널 타입으로 선언된 프로퍼티는 자동으로 nil값으로 초기화된다.<br>
상수 프로퍼티의 경우 해당 클래스의 생성자를 통해서만 수정할 수 있고, 값이 할당되면 그때부터는 값을 수정할 수 없다.