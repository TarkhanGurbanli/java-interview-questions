# Java Interview Questions

# Java Müsahibə Sualları və Cavabları

Bu sənəd Java proqramlaşdırma dilinə aid müsahibə suallarını və onların ətraflı cavablarını əhatə edir. İlk mövzu **Core Java** (Əsas Java) ilə bağlıdır və burada ən çox soruşulan suallar və onların dəqiq, detallı cavabları yer alır.

## Mündəricat
- [Core Java](#core-java)

## Core Java

### 1. Java nədir və onun əsas xüsusiyyətləri hansılardır?

**Cavab:**

Java, Sun Microsystems tərəfindən 1995-ci ildə buraxılmış yüksək səviyyəli, obyekt-orientasiyalı (object-oriented) proqramlaşdırma dilidir. Java platformadan asılı olmayaraq işləyir, yəni bir dəfə yazılan kod müxtəlif cihazlarda və əməliyyat sistemlərində dəyişiklik etmədən işləyə bilər. Bu, **WORA** (Write Once, Run Anywhere - Bir dəfə yaz, hər yerdə işlət) prinsipi ilə təmin olunur.

Java-nın əsas xüsusiyyətləri:

- **Platform Independence (Platformadan Asılı Olmama):** Java kodu **JVM** (Java Virtual Machine - Java Virtual Maşını) üzərində işləyir. Kod **bytecode** (baytkod) şəklində çevrilir və bu baytkod hər hansı bir cihazda JVM vasitəsilə icra olunur.
- **Object-Oriented (Obyekt-Orientasiyalı):** Java, **OOP** (Object-Oriented Programming - Obyekt-Orientasiyalı Proqramlaşdırma) prinsiplərinə əsaslanır. Buraya **encapsulation** (kapsulyasiya - məlumatların gizlədilməsi), **inheritance** (mirasalma), **polymorphism** (çoxformalıq) və **abstraction** (abstraksiya) daxildir.
- **Robustness (Möhkəmlik):** Java, **exception handling** (istisna idarəetmə) və **garbage collection** (zibil toplama - istifadə olunmayan obyektlərin avtomatik silinməsi) kimi mexanizmlərlə səhvlərə qarşı davamlıdır.
- **Security (Təhlükəsizlik):** Java-da **sandbox** (qum qutusu) mühiti və **bytecode verifier** (baytkod yoxlayıcısı) kimi mexanizmlər zərərli kodların icrasını məhdudlaşdırır.
- **Multithreading (Çoxluq):** Java, **threads** (axınlar) vasitəsilə eyni anda birdən çox tapşırığın icrasını dəstəkləyir.

### 2. JVM, JRE və JDK arasındakı fərq nədir?

**Cavab:**

- **JVM (Java Virtual Machine - Java Virtual Maşını):** Java proqramlarının işləməsi üçün virtual mühit təmin edən mühərrikdir. Java kodu **bytecode** şəklində JVM-ə göndərilir və JVM bu kodu maşın dilinə çevirərək icra edir. JVM platformaya xasdır, yəni Windows, Linux və ya Mac üçün fərqli JVM-lər mövcuddur.
- **JRE (Java Runtime Environment - Java İşləmə Mühiti):** JRE, Java proqramlarını işlətmək üçün lazım olan mühitdir. Buraya JVM və Java-nın standart kitabxanaları (**core libraries**) daxildir. Əgər sadəcə Java proqramlarını işlətmək istəyirsinizsə, JRE kifayətdir.
- **JDK (Java Development Kit - Java Tərtibat Dəsti):** JDK, Java proqramlarını yazmaq və inkişaf etdirmək üçün lazım olan alətlər toplusudur. JDK, JRE-ni və əlavə olaraq **compiler** (kompilyator - kodu baytkoda çevirən alət), **debugger** (səhv axtaran alət) və digər inkişaf alətlərini ehtiva edir.

**Qısa fərq:** JDK = JRE + inkişaf alətləri, JRE = JVM + kitabxanalar.

### 3. Java-da **public static void main(String[] args)** metodunun rolu nədir?

**Cavab:**

**public static void main(String[] args)** metodu Java proqramının giriş nöqtəsidir (entry point). Java proqramı işə düşəndə JVM bu metodu axtarır və icrasına buradan başlayır.

- **public:** Metodun hər yerdən çağırıla bilməsi üçün **access modifier** (giriş tənzimləyicisi) kimi istifadə olunur. JVM metodun çağırılması üçün buna ehtiyac duyur.
- **static:** Bu açar söz metodun **class** (sinif) səviyyəsində olduğunu göstərir, yəni obyekt yaratmadan birbaşa çağırıla bilər. JVM proqramı başlatarkən obyekt yaratmır, buna görə metod static olmalıdır.
- **void:** Metodun heç bir dəyər qaytarmadığını göstərir.
- **main:** Metodun adıdır və JVM tərəfindən tanınan standart addır.
- **String[] args:** Komanda xəttindən gələn arqumentləri qəbul edən parametrdir. **String[]** massivdir və proqrama xarici məlumat ötürmək üçün istifadə olunur.

Məsələn:
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Salam, Dünya!");
    }
}
```
Bu kod icra olunduqda, JVM `main` metodunu tapır və "Salam, Dünya!" mesajını çap edir.

### 4. **Garbage Collection** (Zibil Toplama) nədir və Java-da necə işləyir?

**Cavab:**

**Garbage Collection (Zibil Toplama)** Java-da istifadə olunmayan obyektlərin yaddaşdan avtomatik təmizlənməsi prosesidir. Bu, proqramçıların yaddaşı əl ilə idarə etməsinə ehtiyacı aradan qaldırır və yaddaş sızması (memory leak) problemlərini azaldır.

**Necə işləyir?**

- Java-da obyektlər **heap** (yığın) yaddaşında saxlanılır. Heap, **young generation** (gənc nəsil) və **old generation** (köhnə nəsil) kimi bölmələrə ayrılır.
- **Garbage Collector (Zibil Toplayıcı)** müntəzəm olaraq heap yaddaşını skan edir və **unreachable** (əlçatan olmayan) obyektləri aşkarlayır. Əlçatan olmayan obyektlər, heç bir **reference** (istinad) ilə bağlı olmayan obyektlərdir.
- **Mark-and-Sweep** alqoritmi istifadə olunur:
  1. **Mark (İşarələmə):** GC bütün əlçatan obyektləri işarələyir.
  2. **Sweep (Təmizləmə):** İşarələnməmiş obyektlər yaddaşdan silinir.
- **Minor GC** gənc nəsil üzərində, **Major GC** isə köhnə nəsil üzərində işləyir.

**Məsələn:**
```java
public class Test {
    public static void main(String[] args) {
        Object obj = new Object(); // Obyekt yaradılır
        obj = null; // Obyektə istinad kəsilir
        System.gc(); // GC-ni çağırmaq üçün təklif (zəmanət verilmir)
    }
}
```
Yuxarıdakı kodda `obj` null olduqdan sonra obyekt əlçatan olmaz və GC tərəfindən silinə bilər.

### 5. **Inheritance** (Mirasalma) nədir və Java-da necə istifadə olunur?

**Cavab:**

**Inheritance (Mirasalma)** OOP-nin əsas prinsiplərindən biridir və bir sinfin (subclass - alt sinif) başqa sinfin (superclass - üst sinif) xüsusiyyətlərini və metodlarını miras almasına imkan verir. Bu, kodun təkrar istifadəsini (reusability) və iyerarxik struktur qurmağı asanlaşdırır.

**Java-da istifadəsi:**

- **extends** açar sözü ilə mirasalma təyin olunur.
- Alt sinif üst sinfin **public** və **protected** üzvlərinə (metod və dəyişənlərə) daxil ola bilər.
- Java-da bir sinif yalnız bir sinfdən miras ala bilər (**single inheritance** - tək mirasalma).

**Məsələn:**
```java
class Animal {
    void eat() {
        System.out.println("Heyvan yemək yeyir.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("İt hürür.");
    }
}

public class Test {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Miras alınmış metod
        dog.bark(); // Öz metodu
    }
}
```
**Nəticə:**
```
Heyvan yemək yeyir.
İt hürür.
```

**Vacib qeyd:** Java-da **multiple inheritance** (çoxlu mirasalma) siniflər üçün dəstəklənmir, lakin **interface** (interfeys) vasitəsilə bu funksionallıq əldə oluna bilər.

---

**Qeyd:** Daha çox sual və cavab əlavə etmək istəyirsinizsə, xahiş edirəm sayını və ya xüsusi mövzuları dəqiqləşdirin. Məsələn, **Collections**, **Multithreading**, **Exception Handling** kimi mövzulara keçmək olar.
