```java
public class HelloWorld {

  public static void main(String[] args) {
    System.out.println("Hello World");
    playFarm(); // 동물농장
  }

  private static void playFarm() {
    // 호랑이가 농장에? 출현
    Tiger tiger = new Tiger();
    tiger.setLegs(4);
    tiger.setName("호랭");
    // 치킨은 진리
    Chicken chicken = new Chicken();
    chicken.setLegs(2);
    chicken.setName("교촌삐약");
    chicken.setWings(2);

    print(tiger);
    print(chicken);

  }

  private static void print(Animal animal) {
    System.out.println(animal.getInfo());
  }

}

```

related: https://okdevtv.com/mib/java/inheritance

