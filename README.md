Kodlar:

Değişkenler

```dart
void main() {
var name = 'Ahmet';
var age = 19;
var height = 1.80;
var isStudent = true;
var languages = ['Python', 'Dart', 'Java', 'C#'];
var friends = {'Ahmet': 19, 'Mehmet': 20, 'Ali': 21, 'Veli': 22, 'Ayşe': 23};

  print('Hello world: ${name}!');
  print('Age: ${age}');
  print('Height: ${height}');
  print('Is Student: ${isStudent}');
  print('Languages: ${languages}');
  print('Friends: ${friends}');
}
```

Veri Tipleri

```dart
int num1 = 100;
double num2 = 100.1;
// hem int hemde float tipleri "num"un alt türleridir.
num num3 = 50;
num  num4 = 50.4;

print("Num 1 is $num1");
print("Num 2 is $num2");  
print("Num 3 is $num3");  
print("Num 4 is $num4");  
print("Sum is $sum");
```

Ön Ek İşleçleri

```dart
void main() {
  var sayi = 10;
  
  print (++sayi); // 11 -> ön ek işleç - Önce arttırıp sonra yazdırır.
  print(sayi++); // 11 -> son ek işleç - Önce yazdırıp sonra arttırır.
  print(sayi); // 12 - Sadece yazdırır.
  
  print(sayi--); // 12 - Önce yazdırır sonra çıkartır.
  print(--sayi); // 10 - Önce çıkartır sonra yazdırır.

  }
```

İki string birleştirme

```dart
var name = "Ahmet";
var surnname = "Birkan";

print(name + " " + surname)
```

Listeden eleman silme

```dart
void main() {
  var list = [10, 11, 12, 13, 14];
  print("List before removing element : ${list}");
  list.removeAt(3);
  print("List after removing element : ${list}");
}
```