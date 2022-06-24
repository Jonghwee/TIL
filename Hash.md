Hash는 Key 와 Value로 이루어진 자료 구조이다.
Hash를 사용하지 않고 배열을 사용하여 자료를 다룬다고 가정한다면 

int[] phonebook = new int[5];
phonebook[0];

와 같이 정수로만 접근이 가능했었다.
위와 같이 전화번호부로 상황을 가정했을 땐 친구의 이름을 알더라도 이름으로 친구의 전화번호를 알 수가 없는 것이다.
String name = "minsu";
phonebook[name] => error

이렇게 배열의 형태에서 값을 찾을 때는 for문을 사용해서 0부터 n까지 값을 찾아보고 내가 원하는 값을 꺼내와야하는 매우 번거로운 과정을 거쳐야했다.

하지만 Hash를 사용하면 String 타입이나 다른 데이터 타입으로 자료구조에 접근하고 데이터를 관리하는 것이 가능해진다.

HashMap을 만들고 HashMap.put("A", true); 을 입력하면
HashMap["A"] = true; 가 성립하게 된다.

그리고 "A"에 해당하는 Value를 가져올 땐 Hashmap.get("A"); 을 사용하면 되고 
hashmap["A"]으로도 간단하게 가져올 수도 있다.

단, A라는 Key가 존재하지 않을 때는 값을 불러올 때 error가 뜨게 된다.
이럴 때 getOrDefault를 사용하면 존재하지 않는 Key를 입력했을 때 하나의 함수 내에서 예외처리를 하게 된다.
만약 C라는 Key값이 존재하지 않을 때,

hashmap.getOrDefault("C", false);

를 사용하면 hashmap.get("C") = false; 라고 예외처리를 하게 되는 것이다.