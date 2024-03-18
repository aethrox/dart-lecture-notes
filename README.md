Temel Terimler ve Tanım:
###### Flutter nedir ?
> ##### farklı mobil platformlarda (Ör: iOS ve Android) çalışabilen yerel uygulamalar üretebilen bir araçtır.
<br>
- lib: dart dosyasının bulunduğu klasör <br>
- proje oluşturma : flutter create appName  <br>
- proje çalıştırma : flutter run
- test klasörü : projeleri test etmek için kullanılır

<br>

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
void main() {
int num1 = 100;
double num2 = 100.1;
// hem int hemde float tipleri "num"un alt türleridir.
num num3 = 50;
num  num4 = 50.4;

print("Num 1 is $num1");
print("Num 2 is $num2");  
print("Num 3 is $num3");  
print("Num 4 is $num4");
}
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
void main() {
  var name = "Ahmet";
  var surnname = "Birkan";

  print(name + " " + surname)

  }

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

Liste içerisindeki ilk öğeyi bulmak

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];

  // İlk çift sayıyı bul
  int firstEvenNumber = numbers.firstWhere((number) => number % 2 == 0);

  print(firstEvenNumber); // 2

  // 4'ten büyük ilk sayıyı bul
  int firstNumberGreaterThan4 = numbers.firstWhere((number) => number > 4);

  print(firstNumberGreaterThan4); // 5

  // Eşleşen bir öğe yoksa orElse fonksiyonunu çalıştır
  String? firstLetter = numbers.firstWhere((number) => number.isLetter, orElse: () => "Sayısal bir listede harf bulunamadı");

    // String tipinin önüne gelen "?" işaret değişkenin null değeri alabileceğininde anlamınada gelir.

  print(firstLetter); // Sayısal bir listede harf bulunamadı
}
```

Listeye eleman ekleme

```dart
void main() {
  var weekend = {"cumartesi", "pazar"};

  days.add("pazartesi"); // günler değişkenine pazartesi yi ekler

  days.addAll(weekday); // haftaiçi dizisinde ki elemanları "günler dizisine" ekler
  days.addAll(weekend); // haftasonu dizisinde ki elemanları "günler dizisine" ekler
  }
```

Liste de ki elemana erişmek ve silmek

```dart
void main() {
  print(weekend.elementAt(0)); // küme de ki elementlere erişmek için "elementAt()" kullanılır
  weekend.removeAt(2); // haftalar içerisinde ki 2. elemanı siler
}
```

Liste de ki elemanı arama

```dart
var find = "cumartesi";
  if (days.contains(find)) { // günler içerisinde "cumartesi" var mı yok mu kontrol eder.
    print("$find kümesinde yer alıyor.");
```

4. Obje ifadelerinde key ve value değeri alma

```dart
void main() {
  var elementler = {"H": "helyum", "Li" : "lityum"};
  var simgeler = elementler.keys; // key değerini verir
  var isimler = elementler.value; // value değerini verir
  print(simgeler);
}
```

5. Uygulama -1

```dart
enum cinsiyetler {disi, erkek};

class Hayvan {
  int _yas;
  
  cinsiyetler cinsiyet;
  
  Hayvan(this._yas, this.cinsiyet);

  Hayvan.isimli({required yas, this.cinsiyet = cinsiyetler.erkek}) : _yas = yas;

  set yasBelirle(int yas) {
    _yas = yas;
  }

  int get yasOgren {
    return (_yas);
  }

  besle() {
    print("yedim");
  }

  reporla() {
    print("$_yas" "yaşındayım", "Cinsiyetim : $cinsiyet");
  }
}
```

6. Uygulama 1 Devamı :

```dart
import './hayvan.dart';

void main() {
  var kus = Hayvan(2, cinsiyetler.disi);
  
  kus.besle(); // yedim
  kus.reporla(); // 2 yaşındayım cinsiyetim : cinsiyetler.disi

  var kedi.yasBelirle = 3;
  print(kedi.cinsiyet); // cinsiyetler.erkek
  print(kedi.yasOgren); // 3
  
  kedi.raporla() // 3 yaşındayım, cinsiyetim: cinsiyetler.erkek

}
```
