# Core Java Müsahibə Sualları

Bu sənəd **Core Java** ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar Java-nın əsas mövzularını başdan sona əhatə edir.

## Mövzular
- [Core Java](#core-java)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
- [Kafka və Kafka Streams](#kafka-və-kafka-streams)
- [Liquibase](#liquibase)
- [GitHub](#github)
- [Docker](#docker)
- [Redis](#redis)

## Mündəricat
- [Ümumi Suallar](#ümumi-suallar)
- [OOP Prinsipləri](#oop-prinsipləri)
- [Data Tipləri və Dəyişənlər](#data-tipləri-və-dəyişənlər)
- [Exception Handling](#exception-handling)
- [Collections Framework](#collections-framework)
- [Multithreading](#multithreading)
- [String və StringBuilder](#string-və-stringbuilder)
- [Java I/O](#java-io)
- [Generics](#generics)
- [Lambda İfadələri və Stream API](#lambda-ifadələri-və-stream-api)
- [Digər Mövzular](#digər-mövzular)

## Core Java

## Ümumi Suallar
**1. Java nədir və onun əsas xüsusiyyətləri hansılardır?**

**Cavab:**

`Java`, `James Gosling` və Sun Microsystems tərəfindən 1995-ci ildə yaradılmış yüksək səviyyəli, obyekt yönümlü (object-oriented), platformadan asılı olmayan (platform-independent) proqramlaşdırma dilidir. Java, "Write Once, Run Anywhere" (WORA) prinsipi ilə tanınır, yəni bir dəfə yazılan kod müxtəlif platformalarda (Windows, Linux, macOS və s.) dəyişiklik etmədən işləyə bilər. Bu, Java-nın bytecode və Java `Virtual Machine (JVM)` vasitəsilə mümkün olur. Java həmçinin server tətbiqləri, mobil tətbiqlər (Android), veb tətbiqləri və böyük miqyaslı sistemlər kimi müxtəlif sahələrdə geniş istifadə olunur.

**Əsas Xüsusiyyətlər:**

- **Platformadan Asılı Olmama (Platform Independence):** Java kodu JVM-də işləyən bytecode-a çevrilir, bu da onu istənilən platformada icra edilə bilər.
- **Obyekt Yönümlü Proqramlaşdırma (OOP):** Java, encapsulation, inheritance, polymorphism kimi OOP prinsiplərini dəstəkləyir.
- **Sadəlik (Simplicity):** Java sintaksisi C++-a bənzəyir, lakin daha sadədir, çünki pointerlər və ya çoxlu mirasalma kimi mürəkkəb xüsusiyyətlər yoxdur.
- **Təhlükəsizlik (Security):** Java-nın daxili təhlükəsizlik mexanizmləri (məsələn, sandbox mühiti) zərərli kodların icrasını məhdudlaşdırır.
- **Yaddaş İdarəetməsi (Memory Management):** Java-da Garbage Collection avtomatik olaraq istifadə olunmayan obyektləri təmizləyir.
- **Multithreading (Çoxaxınlılıq):** Java, eyni anda birdən çox tapşırığın icrasını dəstəkləyir.
- **Robustluq (Robustness):** Java-nın tip təhlükəsizliyi (type safety), istisna idarəetməsi (exception handling) və avtomatik yaddaş idarəetməsi səhvləri minimuma endirir.
- **Zəngin API:** Java geniş kitabxana dəsti ilə (Java API) şəbəkə, fayl əməliyyatları, GUI və s. üçün dəstək təmin edir.
- **Yüksək Performans:** Just-In-Time (JIT) kompilyatoru ilə Java kodu yerli maşın koduna çevrilərək yüksək performans təmin edir.
- **Çoxsaylı Platformalar:** Java desktop, veb, mobil və server tətbiqləri üçün uyğundur.

---

**2. JVM, JRE və JDK arasındakı fərq nədir?**

**Cavab:**

****JVM, JRE və JDK Java-nın işləməsi üçün zəruri olan üç əsas komponentdir, lakin onların funksiyaları və istifadə sahələri fərqlidir:****

- JVM (Java Virtual Machine - Java Virtual Maşını):
  - JVM Java proqramlarını icra etmək üçün virtual mühit təmin edən icra mühərrikidir.
  - Java kodunun bytecode-unu maşın dilinə çevirir və həmin platformada icra edir.
  - Əsas komponentləri: `Class Loader`, `Bytecode Verifier`, `Interpreter`, `JIT Compiler` və `Garbage Collector`.
  - JVM platformaya xasdır (Windows, Linux və s. üçün fərqli JVM-lər var).
  - Məqsədi: Platformadan asılı olmayaraq Java kodunun icrasını təmin etmək.
 
- JRE (Java Runtime Environment - Java İcra Mühiti):
  - JRE, Java proqramlarını işə salmaq üçün lazım olan mühitdir.
  - JVM-i və Java-nın əsas kitabxanalarını (Java Class Library) ehtiva edir.
  - JRE yalnız icra üçün lazımdır, yəni Java proqramlarını inkişaf etdirmək üçün kifayət deyil.
  - Məqsədi: Java tətbiqlərinin icrasını təmin etmək (son istifadəçilər üçün).

- JDK (Java Development Kit - Java İnkişaf Dəsti):
  - JDK, Java tətbiqləri inkişaf etdirmək və icra etmək üçün tam alətlər dəstidir.
  - JRE-ni (yəni JVM və kitabxanaları) və əlavə inkişaf alətlərini (javac, javadoc, jar və s.) ehtiva edir.
  - Məqsədi: Java proqramlarının yazılması, kompilyasiyası və icrası üçün bütün zəruri alətləri təmin etmək.

- Fərqlər:
  - JVM yalnız icra mühərrikidir, JRE isə JVM-i və icra üçün lazım olan kitabxanaları ehtiva edir.
  - JDK JRE-ni və inkişaf alətlərini ehtiva edir, yəni daha genişdir.
  - Son istifadəçi yalnız JRE-yə ehtiyac duyur, geliştirici isə JDK-ya.

---

**3. **public static void main(String[] args)** metodunun rolu nədir?**

**Cavab:**

`public static void main(String[] args)` Java proqramının giriş nöqtəsi (entry point) olan xüsusi metoddur. JVM Java proqramını işə salarkən ilk olaraq bu metodu axtarır və icrasına buradan başlayır. Bu metod olmadan Java proqramı icra oluna bilməz (standalone tətbiqlər üçün).

- **Metodun Komponentləri:**
  - public: Metod JVM tərəfindən xaricdən çağırıldığı üçün ictimai (public) olmalıdır.
  - static: Metod sinifə aid olduğu üçün obyekt yaratmadan çağırıla bilər.
  - void: Metod heç bir dəyər qaytarmır.
  - main: JVM-in axtardığı metodun adı dəqiq olaraq "main" olmalıdır.
  - String[] args: Komanda xəttindən arqumentləri qəbul etmək üçün istifadə olunur.
 
- **Rolu:**
  - Java proqramının icrasına başlama nöqtəsidir.
  - Komanda xəttindən ötürülən arqumentləri (args) qəbul edərək proqramın davranışını fərdiləşdirməyə imkan verir.
  - Proqramın əsas məntiqi buradan başlayır və ya digər metodlara yönləndirilir.

**Kod Nümunəsi:**

```java
public class MainExample {
    // JVM-in proqramı başlatdığı giriş nöqtəsi
    public static void main(String[] args) {
        // Arqumentləri konsola yazdırır
        System.out.println("Proqrama ötürülən arqumentlər:");
        for (String arg : args) {
            System.out.println(arg);
        }
        // Əsas proqram məntiqi burada yerləşə bilər
        System.out.println("Proqram başladı!");
    }
}
```

- **Nəzəri İzahat:**
  - `main` metodunun düzgün təyin olunması (imza, yəni signature) JVM-in proqramı tapa bilməsi üçün vacibdir. Yanlış imza (məsələn, `public void main()` və ya `static int main()`) istifadə edilərsə, JVM main metodunu tapmaz və `NoSuchMethodError` xətası atar. Arqumentlər `(args)` isə proqramın dinamik konfiqurasiyası üçün faydalıdır, məsələn, fayl yollarını və ya parametrləri ötürmək üçün.

---

**4. **Garbage Collection** (Zibil Toplama) nədir?**

**Cavab:**

`Garbage Collection` (Zibil Toplama) Java-da avtomatik yaddaş idarəetmə mexanizmidir. Bu mexanizm, proqram tərəfindən artıq istifadə olunmayan obyektləri (heap yaddaşında yer tutan) aşkar edir və onların tutduğu yaddaşı azad edir. Bu, geliştiricilərin əl ilə yaddaş idarəetməsi (məsələn, C++-da `free()` funksiyası ilə) yükünü azaldır və yaddaş sızması (memory leak) kimi problemləri minimuma endirir.

- **Necə İşləyir:**
  - **Marking (İşarələmə):** Garbage Collector heap-dəki bütün obyektləri skan edir və hələ də istinad edilən (reachable) obyektləri işarələyir.
  - **Sweeping (Təmizləmə):** İşarələnməmiş (unreachable) obyektlər yaddaşdan silinir.
  - **Compacting (Sıxışdırma):** Boş qalan yaddaş sahələri birləşdirilərək fraqmentasiya azalır (bəzi GC alqoritmlərində).

- **Əsas Xüsusiyyətlər:**
  - **Avtomatikdir:** Geliştiricinin əl ilə yaddaş azad etməsinə ehtiyac yoxdur.
  - **Heap Yaddaşında İşləyir:** Yalnız heap-dəki obyektlərə tətbiq olunur, stack yaddaşı GC tərəfindən idarə olunmur.
  - **Fərqli Alqoritmlər:** Java-da müxtəlif GC alqoritmləri var (məsələn, Serial GC, Parallel GC, G1 GC, ZGC).
  - **Performans Təsiri:** GC proqramın performansına təsir edə bilər, buna görə optimallaşdırma vacibdir.

- **Əsas GC Alqoritmləri:**
  - **Serial GC:** Tək axınlı, kiçik tətbiqlər üçün uyğundur.
  - **Parallel GC:** Çox axınlı, yüksək ötürmə qabiliyyəti (throughput) üçün optimallaşdırılıb.
  - **G1 GC:** Böyük heap-lər üçün, aşağı gecikmə (low latency) təmin edir.
  - **ZGC:** Ultra aşağı gecikməli, müasir tətbiqlər üçün nəzərdə tutulub.
 
```java
public class GarbageCollectionExample {
    public static void main(String[] args) {
        // Yeni obyektlər yaradılır, heap yaddaşında yer tutur
        String str1 = new String("Test1");
        String str2 = new String("Test2");

        // str1-ə istinad silinir, obyekt unreachable olur
        str1 = null;

        // Garbage Collector-u əl ilə çağırmaq (təklifdir, zəmanətli deyil)
        System.gc();

        // Proqramın davam etdiyini göstərmək üçün
        System.out.println("Proqram işləyir: " + str2);
    }
}
```

- **Nəzəri İzahat:** `System.gc()` GC-ni çağırmaq üçün təklifdir, lakin JVM onun nə vaxt işə düşəcəyinə özü qərar verir. Garbage Collection Java-nın robustluğunu artırır, lakin performans kritik tətbiqlərdə GC alqoritmini (məsələn, G1 və ya ZGC) seçmək və konfiqurasiya etmək vacibdir. Həmçinin, zəif istinadlar (WeakReference) kimi mexanizmlər GC ilə işləyərkən faydalıdır.

---

**5. Java-da **bytecode** nədir və necə işləyir?**

**Cavab:**

Bytecode Java proqramının javac (Java Compiler) tərəfindən kompilyasiya edildikdən sonra yaranan ara nəticədir. Bu, platformadan asılı olmayan, aşağı səviyyəli, maşın oxuna bilən təlimatlar toplusudur. Bytecode `.class` fayllarında saxlanılır və JVM tərəfindən icra edilir.

- **Necə İşləyir:**
  - **Kompilyasiya:** Java mənbə kodu (`.java` faylı) `javac` tərəfindən bytecode-a (`.class` faylı) çevrilir.
    **İcra:** JVM bytecode-u oxuyur və onu hədəf platformanın maşın dilinə çevirir (Interpreter və ya JIT Compiler vasitəsilə).
  - **Platformadan Asılı Olmama:** Bytecode platformaya xas deyil, bu da Java-nın "Write Once, Run Anywhere" prinsipini təmin edir.
  - **Bytecode Verifier:** JVM `bytecode`-u icra etməzdən əvvəl onun təhlükəsizliyini və düzgünlüyünü yoxlayır (məsələn, tip təhlükəsizliyi).

- **Bytecode-un Strukturu:**
  - **Magic Number:** `.class` faylının başlanğıcını göstərir (0xCAFEBABE).
  - **Constant Pool:** Sabitlər və istinadlar (metodlar, siniflər və s.).
  - **Method Area:** Metodların təlimatları və digər metadata.

- **Nəzəri İzahat:**
  - Bytecode JVM-in platformadan asılı olmamasını təmin edən əsas elementdir. `javac` kodu `bytecode`-a çevirir, `JVM` isə bu `bytecode`-u hədəf platformaya uyğun maşın koduna çevirir. `JIT Compiler` bytecode-u optimallaşdıraraq performansı artırır. Bytecode-un təhlükəsizliyi isə `Bytecode Verifier` ilə yoxlanılır ki, bu da Java-nın təhlükəsizliyini gücləndirir.

---

**6. Java-nın **WORA** (Write Once, Run Anywhere) prinsipi nə deməkdir?**

**Cavab:**

`WORA` (`Write Once, Run Anywhere` - Bir dəfə yaz, hər yerdə işlət) Java-nın əsas prinsiplərindən biridir. Bu prinsip, Java ilə yazılmış bir proqramın bir platformada (məsələn, Windows) yazıldıqdan sonra heç bir dəyişiklik etmədən digər platformalarda (məsələn, Linux, macOS) işləyə biləcəyini ifadə edir. Bu, Java-nın platformadan asılı olmama xüsusiyyəti sayəsində mümkündür.

- **WORA-nın Əsas Mexanizmi:**
  - **Java kodu javac (Java Compiler)** tərəfindən bytecode-a çevrilir. Bytecode platformadan asılı olmayan ara təlimatlar toplusudur.
  - **JVM (Java Virtual Machine)** bytecode-u hədəf platformanın maşın dilinə çevirərək icra edir. Hər platforma üçün fərqli JVM olduğu üçün eyni bytecode fərqli platformalarda işləyə bilir.
  - **Java-nın standart kitabxanaları (Java API)** platformadan asılı olan funksiyaları (məsələn, fayl əməliyyatları, şəbəkə əlaqələri) abstraqlaşdırır, bu da kodu portativ edir.

---


**7. Java-da **platform independence** (platformadan asılı olmama) necə təmin olunur?**

**Cavab:**
Java-nın platformadan asılı olmama xüsusiyyəti, proqramın bir platformada yazıldıqdan sonra digər platformalarda dəyişiklik etmədən işləməsini təmin edir. Bu, WORA prinsipinin əsasını təşkil edir və aşağıdakı mexanizmlərlə həyata keçirilir:

- **Bytecode:**
  - Java kodu javac tərəfindən platformadan asılı olmayan bytecode-a çevrilir.
  - Bytecode, .class fayllarında saxlanılır və JVM tərəfindən oxunur.
  - Bytecode-un strukturu hər platformada eynidir, bu da portativliyi təmin edir.
- **JVM (Java Virtual Machine):**
  - JVM platformaya xas bir mühitdir və bytecode-u həmin platformanın maşın dilinə çevirir.
  - Hər platforma üçün xüsusi JVM (Windows JVM, Linux JVM və s.) mövcuddur.
  - JVM-in Interpreter və JIT Compiler komponentləri bytecode-u icra edir.
- **Java API (Standart Kitabxanalar):**
  - Java-nın standart kitabxanaları (məsələn, java.io, java.net) platformaya xas funksiyaları abstraqlaşdırır.
  - Məsələn, fayl əməliyyatları üçün java.io.File sinfi platforma fərqlərini gizlədir.
- **Bytecode Verifier:**
  - JVM bytecode-u icra etməzdən əvvəl onun düzgün və təhlükəsiz olduğunu yoxlayır.
  - Bu, platformalar arası uyğunluğu və təhlükəsizliyi təmin edir.
- **Standartlaşdırılmış Spesifikasiyalar:**
  - Java-nın spesifikasiyaları (JLS - Java Language Specification) bütün platformalarda eyni şəkildə tətbiq olunur.

---

**8. **ClassLoader** (Sinif Yükləyicisi) nədir və necə işləyir?**

**Cavab:**

`ClassLoader` (Sinif Yükləyicisi) Java-da sinifləri (.class faylları) və resursları (məsələn, .jar faylları) yaddaşa yükləyən JVM-in bir komponentidir. ClassLoader sinif fayllarını tapır, onların bytecode-unu oxuyur və JVM-in icra edə biləcəyi formada təqdim edir.

- **Əsas Vəzifələri:**
  - **Yükləmə (Loading):** `.class` fayllarını diskdən, şəbəkədən və ya digər mənbələrdən yaddaşa yükləyir.
  - **Bağlama (Linking):** Sinifin düzgünlüyünü yoxlayır (Bytecode Verifier), yaddaşı ayırır və statik dəyişənləri ilkinləşdirir.
  - **İlkinləşdirmə (Initialization):** Statik blokları və statik dəyişənləri icra edir.

- **ClassLoader-ın İşləmə Mexanizmi:**
  - **Delegation Model (Vəkalət Modeli):**
    - `ClassLoader` sinifləri yükləməzdən əvvəl yuxarı səviyyəli (parent) ClassLoader-a sorğu göndərir.
    - Əgər `parent ClassLoader` sinifi tapa bilməzsə, özü yükləməyə cəhd edir.
    - Bu model sinif təkrarlanmasını (class duplication) və təhlükəsizlik problemlərini azaldır.
  - **ClassLoader Növləri:**
    - **Bootstrap ClassLoader:** Java-nın əsas siniflərini (rt.jar-dakı siniflər, məsələn, java.lang.*) yükləyir. C/C++ ilə yazılmışdır.
    - **Extension ClassLoader:** JRE-nin genişləndirilmə siniflərini (ext qovluğundakı .jar faylları) yükləyir.
    - **System/Application ClassLoader:** Tətbiqin classpath-dəki sinifləri və resursları yükləyir.
  - **Təhlükəsizlik:**
    - `ClassLoader` siniflərin təhlükəsizliyini yoxlayır (məsələn, zərərli kodun yüklənməsinin qarşısını alır).
    - `Namespace` mexanizmi ilə sinif təkrarlanmasını önləyir.
   
**Kod Nümunəsi:**

```java
public class CustomClassLoaderExample {
    public static void main(String[] args) {
        // Cari ClassLoader-ı əldə etmək
        ClassLoader classLoader = CustomClassLoaderExample.class.getClassLoader();
        System.out.println("Cari ClassLoader: " + classLoader);

        // Parent ClassLoader-ı əldə etmək
        System.out.println("Parent ClassLoader: " + classLoader.getParent());
    }
}
```

**Xüsusi ClassLoader Nümunəsi:**

```java
import java.io.*;
import java.nio.file.Files;

public class CustomClassLoader extends ClassLoader {
    @Override
    protected Class<?> findClass(String name) throws ClassNotFoundException {
        try {
            // .class faylını oxumaq
            String fileName = name.replace('.', '/') + ".class";
            byte[] data = Files.readAllBytes(new File(fileName).toPath());
            // Bytecode-dan sinif yaratmaq
            return defineClass(name, data, 0, data.length);
        } catch (IOException e) {
            throw new ClassNotFoundException("Sinif tapılmadı: " + name, e);
        }
    }

    public static void main(String[] args) throws Exception {
        // Xüsusi ClassLoader ilə sinif yükləmək
        CustomClassLoader loader = new CustomClassLoader();
        Class<?> clazz = loader.loadClass("com.example.MyClass");
        System.out.println("Yüklənmiş sinif: " + clazz.getName());
    }
}
```

**Nəzəri İzahat:** ClassLoader Java-nın dinamik sinif yükləmə qabiliyyətini təmin edir. Vəkalət modeli təhlükəsizliyi və səmərəliliyi artırır, çünki siniflər yalnız bir dəfə yüklənir. Xüsusi ClassLoader-lar isə plagin sistemləri və ya dinamik yükləmə tələb edən tətbiqlərdə istifadə olunur (məsələn, Java EE serverləri).

---

**9. Java-da **memory management** (yaddaş idarəetməsi) necə həyata keçirilir?**

**Cavab:**

Java-da yaddaş idarəetməsi avtomatik olaraq `Garbage Collector (GC)` və JVM-in yaddaş strukturları (`Heap və Stack`) vasitəsilə həyata keçirilir. Bu, geliştiricilərin əl ilə yaddaş ayırma və azad etmə yükünü azaldır, yaddaş sızması (memory leak) və digər səhvləri minimuma endirir.

**Yaddaş İdarəetməsinin Əsas Komponentləri:**

- **Yaddaş Bölgələri:**
  - **`Heap`:** Obyektlər və onların instans dəyişənləri heap yaddaşında saxlanılır. Heap, Garbage Collector tərəfindən idarə olunur.
  - **`Stack`:** Metod çağırışları, lokal dəyişənlər və istinadlar (references) stack yaddaşında saxlanılır. Stack avtomatik idarə olunur (LIFO - Last In, First Out).
  - **`Metaspace`:** Sinif metadata (sinif strukturunun təsviri) saxlanılır (Java 8-dən sonra PermGen-in yerini almışdır).
- **Garbage Collection:**
  - GC istifadə olunmayan (unreachable) obyektləri heap-dən təmizləyir.
  - Mark-and-Sweep: Obyektləri işarələyir və istifadə olunmayanları silir.
  - Generational GC: Heap gənc (Young Generation) və köhnə (Old Generation) nəsillərə bölünür. Gənc nəsildə tez-tez təmizləmə aparılır.
- **Yaddaş Optimallaşdırması:**
  - JIT Compiler: Bytecode-u optimallaşdırılmış maşın koduna çevirir.
  - Memory Pools: Eden Space, Survivor Space, Tenured Space kimi bölmələr heap-i effektiv idarə edir.
  - GC Alqoritmləri: Serial, Parallel, G1, ZGC kimi alqoritmlər performans və gecikmə tələblərinə uyğun seçilir.
- **Əsas Xüsusiyyətlər:**
  - **Avtomatik Yaddaş Azad Etmə:** Geliştiricilər yaddaşı əl ilə azad etmir, GC bunu avtomatik edir.
  - **Təhlükəsizlik:** Yanlış yaddaş idarəetməsi nəticəsində yaranan səhvlər (məsələn, dangling pointers) qarşısı alınır.
  - **Tunable GC:** Geliştiricilər JVM parametrləri (məsələn, `-Xmx`, `-Xms`) ilə GC-ni optimallaşdıra bilər.

**Kod Nümunəsi:**

```java
public class MemoryManagementExample {
    public static void main(String[] args) {
        // Heap-də obyektlər yaradılır
        for (int i = 0; i < 1000; i++) {
            String str = new String("Test" + i); // Yeni obyektlər heap-də saxlanılır
        }
        // Stack-də lokal dəyişən
        int localVar = 10;
        System.out.println("Lokal dəyişən: " + localVar);

        // GC-ni təklif et (zəmanətli deyil)
        System.gc();
        System.out.println("Garbage Collector çağırıldı!");
    }
}
```

**Nəzəri İzahat:** Java-da yaddaş idarəetməsi avtomatik və təhlükəsizdir, lakin performans kritik tətbiqlərdə GC alqoritmini və heap ölçüsünü düzgün konfiqurasiya etmək vacibdir. Heap və Stack-in fərqli funksiyaları yaddaşın səmərəli istifadəsini təmin edir.

---

**10. **Heap** və **Stack** yaddaş bölgələri arasındakı fərq nədir?**

**Cavab:**

Java-da yaddaş iki əsas bölgəyə bölünür: `Heap` və `Stack`. Bu bölgələr fərqli məqsədlər üçün istifadə olunur və fərqli idarəetmə mexanizmlərinə malikdir.

- **Heap Yaddaş:**
  - **Təyinat:** Obyektlər, instans dəyişənləri və sinif üzvləri heap-də saxlanılır.
  - **İdarəetmə:** Garbage Collector tərəfindən avtomatik idarə olunur.
  - **Ömür:** Obyektlər istinad edildiyi müddətcə yaşayır, istinadlar itəndə GC tərəfindən təmizlənir.
  - **Struktur:** Heap, Young Generation (Eden, Survivor) və Old Generation kimi bölmələrə ayrılır.
  - **Xüsusiyyətlər:**
    - Böyük həcmdə yaddaş saxlaya bilər.
    - Dinamik olaraq böyüyür (-Xmx parametri ilə məhdudlaşdırılır).
    - Çox axınlı mühitlərdə paylaşılan yaddaştır.

- **Stack Yaddaş:**
  - **Təyinat:** Metod çağırışları, lokal dəyişənlər və istinadlar (references) stack-də saxlanılır.
  - **İdarəetmə:** LIFO (Last In, First Out) prinsipi ilə avtomatik idarə olunur.
  - **Ömür:** Metod başa çatdıqda stack-dəki müvafiq çərçivə (stack frame) avtomatik silinir.
  - **Struktur:** Hər axın (thread) öz stack-ınə malikdir, bu da izolyasiyanı təmin edir.
  - **Xüsusiyyətlər:**
    - Daha kiçik ölçüdədir və sabitdir.
    - Çox sürətli işləyir, çünki sadə LIFO strukturuna malikdir.
    - Hər axın üçün ayrı stack yaddaşı ayrılır.

**Əsas Fərqlər:**

| Xüsusiyyət            | Heap                              | Stack                               |
|-----------------------|-----------------------------------|-------------------------------------|
| **Saxlanılan Məlumat** | Obyektlər, instans dəyişənləri   | Lokal dəyişənlər, metod çağırışları |
| **İdarəetmə**         | Garbage Collector                | Avtomatik (LIFO)                     |
| **Ömür**              | İstinad olunduğu müddətcə        | Metodun ömrü ilə məhdudlaşır         |
| **Paylaşım**          | Bütün axınlar tərəfindən paylaşılır | Axına xasdır                      |
| **Performans**        | Daha yavaş (GC səbəbindən)       | Daha sürətli                         |

**Kod Nümunəsi:**

```java
public class HeapAndStackExample {
    // Heap-də saxlanılan instans dəyişəni
    private String instanceVar = "Heap-də saxlanılır";

    public static void main(String[] args) {
        // Stack-də saxlanılan lokal dəyişən
        int localVar = 42;

        // Heap-də yeni obyekt yaradılır, istinad stack-də saxlanılır
        HeapAndStackExample obj = new HeapAndStackExample();

        // Metod çağırışı stack-də yeni çərçivə yaradır
        obj.printValues(localVar);
    }

    public void printValues(int param) {
        // param stack-də saxlanılır
        System.out.println("Lokal dəyişən (Stack): " + param);
        // instanceVar heap-də saxlanılır
        System.out.println("İnstans dəyişəni (Heap): " + instanceVar);
    }
}
```

**Çıxış (Output):**

```text
Lokal dəyişən (Stack): 42
İnstans dəyişəni (Heap): Heap-də saxlanılır
```

**Nəzəri İzahat:** `Heap` və `Stack` fərqli məqsədlər üçün optimallaşdırılmışdır. Heap böyük və dinamik obyektlər üçün, Stack isə sürətli və qısa ömürlü metod çağırışları üçün istifadə olunur. Garbage Collection heap-i idarə edərkən, Stack avtomatik təmizlənir, bu da Java-nın yaddaş idarəetməsini səmərəli edir.

---

11. Java-da **package** (paket) nədir və nə üçün istifadə olunur?

**Cavab:**

Package Java-da sinifləri, interfeysləri və digər resursları mütəşəkkil şəkildə qruplaşdırmaq üçün istifadə olunan bir mexanizmdir. Paketlər, böyük layihələrdə kodun idarə olunmasını asanlaşdırır və ad çakışmalarının qarşısını alır.

- **Nə üçün istifadə olunur?**
  - **Təşkilatlanma:** Sinifləri məntiqi qruplara ayırır (məsələn, `java.util`, `java.io`).
  - **Ad çakışmalarının qarşısını almaq:** Eyni adlı siniflər fərqli paketlərdə ola bilər.
  - **Giriş nəzarəti:** Paketlər giriş tənzimləyiciləri ilə siniflərə və ya metodlara girişi məhdudlaşdıra bilər.
  - **Yenidən istifadə:** Paketlər modullaşdırmanı təmin edir, bu da kodun təkrar istifadəsini asanlaşdırır.

**Kod Nümunəsi:**

```java
// Paket yaratmaq və istifadə etmək
package com.example.myapp; // Paket adı

public class MyClass {
    public void sayHello() {
        System.out.println("Salam, bu MyClass sinifidir!");
    }
}
```

- **Şərh:**
  - `package com.example.myapp;` - Bu sətir sinifi com.example.myapp paketində yerləşdirir.
  - Paket adları adətən tərs domen adlandırma qaydasından istifadə edir (məsələn, `com.şirkətadı.layihəadı`).

---

12. **import** açar sözü nə üçün lazımdır?

**Cavab:**

mport açar sözü Java-da başqa paketlərdə olan sinifləri, interfeysləri və ya statik üzvləri cari faylda istifadə etmək üçün gətirməyə imkan verir. Bu, tam kvalifikasiya olunmuş adlar (fully qualified names) yazmaq əvəzinə kodun qısa və oxunaqlı olmasına kömək edir.

- **Nə üçün lazımdır?**
  - **Kodun qısaldılması:** java.util.ArrayList kimi uzun adları təkrar yazmağa ehtiyac qalmır.
  - **Oxunaqlılıq:** Kod daha təmiz və anlaşıqlı olur.
  - **Modulluğun dəstəklənməsi:** Fərqli paketlərdən resursları asanlıqla istifadə etməyə imkan verir.

**Kod Nümunəsi**

```java
// import açar sözünün istifadəsi
import java.util.ArrayList; // ArrayList sinifini idxal edir
import java.util.List; // List interfeysini idxal edir

public class ImportExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>(); // Tam ad yazmağa ehtiyac yoxdur
        list.add("Element 1");
        System.out.println(list);
    }
}
```

- **Şərh:**
  - `import java.util.ArrayList;` - ArrayList sinifini idxal edir ki, tam ad (java.util.ArrayList) yazılmasın.
  - Əgər `import` istifadə edilməsə, hər dəfə tam ad yazılmalı olacaq.

---

13. Java-da **access modifiers** (giriş tənzimləyiciləri) hansılardır?

**Access modifiers** Java-da siniflərin, metodların, dəyişənlərin və konstruktorların giriş səviyyəsini təyin etmək üçün istifadə olunur. Onlar kapsulyasiyanı təmin edir və məlumatların təhlükəsizliyini artırır.

- **Giriş tənzimləyiciləri:**
  - **`public`:** Üzv hər yerdən əlçatan olur.
  - **`protected`:** Üzv eyni paketdə və ya miras alan siniflərdə əlçatandır.
  - **`default`:** (paket-səviyyəli, heç bir tənzimləyici göstərilməzsə): Üzv yalnız eyni paketdə əlçatandır.
  - **`private`:** Üzv yalnız eyni sinif daxilində əlçatandır.

**Kod Nümunəsi**

```java
package com.example;

public class AccessModifiers {
    public int publicVar = 1; // Hər yerdən əlçatan
    protected int protectedVar = 2; // Eyni paket və ya miras alan siniflərdə əlçatan
    int defaultVar = 3; // Yalnız eyni paketdə əlçatan
    private int privateVar = 4; // Yalnız bu sinifdə əlçatan

    public void display() {
        System.out.println("Public: " + publicVar);
        System.out.println("Protected: " + protectedVar);
        System.out.println("Default: " + defaultVar);
        System.out.println("Private: " + privateVar);
    }
}

class Test {
    public static void main(String[] args) {
        AccessModifiers obj = new AccessModifiers();
        obj.display();
        // obj.privateVar = 5; // Xəta: privateVar-a xaricdən giriş yoxdur
    }
}
```

- **Şərh:**
  - `publicVar` hər yerdən əlçatandır.
  - `protectedVar` eyni paketdə və ya miras alan siniflərdə istifadə oluna bilər.
  - `defaultVar` yalnız eyni paketdə əlçatandır.
  - `privateVar` yalnız AccessModifiers sinifində əlçatandır.

---

**14. **static** açar sözü nə üçün istifadə olunur?**

**`static`** açar sözü sinifə aid olan üzvləri (dəyişənlər, metodlar, bloklar və ya daxili siniflər) təyin etmək üçün istifadə olunur. Statik üzvlər sinifin nümunəsi (obyekti) yaradılmadan istifadə edilə bilər.

- **Nə üçün istifadə olunur?**
  - **Sinif səviyyəsində resurslar:** Statik üzvlər bütün obyektlər tərəfindən paylaşılır.
  - **Yaddaşın səmərəli istifadəsi:** Statik dəyişənlər yalnız bir dəfə yaddaşda saxlanılır.
  - **Utility metodlar:** Sinifə aid ümumi funksiyalar üçün istifadə olunur (məsələn, Math.sqrt()).

Kod Nümunəsi

```java
public class StaticExample {
    static int count = 0; // Statik dəyişən, bütün obyektlər tərəfindən paylaşılır

    StaticExample() {
        count++; // Hər yeni obyekt yaradıldığında count artır
    }

    static void displayCount() { // Statik metod
        System.out.println("Obyektlərin sayı: " + count);
    }

    public static void main(String[] args) {
        StaticExample obj1 = new StaticExample();
        StaticExample obj2 = new StaticExample();
        StaticExample.displayCount(); // Statik metod sinif adı ilə çağırılır
    }
}
```

- **Şərh:**
  - `static` int count bütün obyektlər üçün ortaqdır.
  - `static void displayCount()` sinif adı ilə çağırılır, obyekt yaratmağa ehtiyac yoxdur.
  - Statik metodlar yalnız statik dəyişənlərə və ya metodlara daxil ola bilər.

---

15. **this** açar sözünün məqsədi nədir?

**`this`** açar sözü cari obyektə istinad etmək üçün istifadə olunur. O, sinifin dəyişənlərini və metodlarını eyni adlı parametr və ya yerli dəyişənlərdən fərqləndirmək üçün faydalıdır.

- **Məqsədləri:**
  - Dəyişən çakışmalarını həll etmək: Sinif dəyişəni ilə parametr arasında fərq qoymaq.
  - Konstruktor çağırışı: Bir konstruktor daxilində digər konstruktoru çağırmaq.
  - Cari obyektə istinad: Metodlara və ya obyektlərə cari obyekti ötürmək.

Kod Nümunəsi

```java
public class ThisExample {
    int number;

    ThisExample(int number) {
        this.number = number; // Sinif dəyişəni ilə parametri fərqləndirir
    }

    void display() {
        System.out.println("Number: " + this.number); // Cari obyektin number dəyişəni
    }

    public static void main(String[] args) {
        ThisExample obj = new ThisExample(42);
        obj.display();
    }
}
```

- **Şərh:**
  - `this.number = number;` - this sinifin number dəyişəninə istinad edir, parametrə deyil.
  - `this` istifadə edilməsə, parametr sinif dəyişənini əvəz edər və yanlış nəticə alınar.

---

**16. **super** açar sözü nə üçün istifadə olunur?**

**`super`** açar sözü miras alınan sinifin (superclass) üzvlərinə (dəyişənlər, metodlar və konstruktorlar) daxil olmaq üçün istifadə olunur.

- **Məqsədləri:**
  - **Superclass konstruktorunu çağırmaq:** Alt sinifdən ana sinifin konstruktoruna müraciət.
  - **Superclass metodlarına daxil olmaq:** Superclass-da müəyyən edilmiş metodları çağırmaq.
  - **Superclass dəyişənlərinə daxil olmaq:** Eyni adlı dəyişənləri fərqləndirmək.

Kod Nümunəsi

```java
class Animal {
    String name = "Animal";

    Animal() {
        System.out.println("Animal konstruktoru");
    }

    void sound() {
        System.out.println("Animal səsi");
    }
}

class Dog extends Animal {
    String name = "Dog";

    Dog() {
        super(); // Animal sinifinin konstruktorunu çağırır
        System.out.println("Dog konstruktoru");
    }

    void display() {
        System.out.println("Dog name: " + name); // Cari sinifin name dəyişəni
        System.out.println("Animal name: " + super.name); // Superclass-ın name dəyişəni
        super.sound(); // Superclass-ın sound metodu
    }
}

public class SuperExample {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.display();
    }
}
```

- **Şərh:**
  - `super()` - Ana sinifin konstruktorunu çağırır.
  - `super.name` - Ana sinifin name dəyişəninə istinad edir.
  - `super.sound()` - Ana sinifin sound metodunu çağırır.

---

**19. Java-da **boxing** və **unboxing** nədir?**

**Boxing** primitiv verilənlər tipini (məsələn, `int`, `double`) onların müvafiq `wrapper` sinifinə (`Integer`, `Double`) çevirmə prosesidir. Unboxing isə əksinə, wrapper sinifindən primitiv tipə çevirmədir.

- **Boxing:**
  - Primitiv tip wrapper sinifinə "qablaşdırılır".
  - Məsələn, `int` → `Integer`.

- **Unboxing:**
  - Wrapper sinifi primitiv tipə "açılır".
  - Məsələn, `Integer` → `int`.

Kod Nümunəsi

```java
public class BoxingUnboxing {
    public static void main(String[] args) {
        // Boxing: int → Integer
        int primitiveInt = 42;
        Integer wrapperInt = primitiveInt; // Avtomatik boxing
        System.out.println("Boxing: " + wrapperInt);

        // Unboxing: Integer → int
        Integer wrapperInt2 = 100;
        int primitiveInt2 = wrapperInt2; // Avtomatik unboxing
        System.out.println("Unboxing: " + primitiveInt2);
    }
}
```

- **Şərh:**
  - `Integer wrapperInt = primitiveInt;` - int dəyəri Integer obyektinə çevrilir (boxing).
  - `int primitiveInt2 = wrapperInt2;` - Integer obyektindən int dəyəri alınır (unboxing).

---

**20. **autoboxing** və **auto-unboxing** necə işləyir?**

`Autoboxing` və `auto-unboxing` Java-da primitiv tiplər və onların wrapper sinifləri arasında avtomatik çevrilmə prosesləridir. Bu mexanizmlər Java 5-də təqdim edilib və kod yazımını asanlaşdırır.

- **Autoboxing:**
  - Primitiv tipin avtomatik olaraq wrapper sinifinə çevrilməsi.
  - Məsələn, `int` dəyəri Integer obyektinə çevrilir.

- **Auto-unboxing:**
  - Wrapper sinifinin avtomatik olaraq primitiv tipə çevrilməsi.
  - Məsələn, `Integer` obyektindən int dəyəri alınır.

**Kod Nümunəsi**

```java
import java.util.ArrayList;

public class AutoBoxingExample {
    public static void main(String[] args) {
        // Autoboxing
        ArrayList<Integer> list = new ArrayList<>();
        list.add(42); // int → Integer (autoboxing)
        System.out.println("List: " + list);

        // Auto-unboxing
        Integer wrapperInt = 100;
        int sum = wrapperInt + 50; // Integer → int (auto-unboxing)
        System.out.println("Sum: " + sum);
    }
}
```

- **Şərh:**
  - `list.add(42); - 42 (int)` avtomatik olaraq Integer obyektinə çevrilir (autoboxing).
  - `int sum = wrapperInt + 50;` - wrapperInt (Integer) avtomatik olaraq int tipinə çevrilir (auto-unboxing).
  - Bu proseslər Java kompilyatoru tərəfindən avtomatik idarə olunur.

---

## OOP Prinsipləri
21. **Inheritance** (Mirasalma) nədir?
22. Java-da **multiple inheritance** (çoxlu mirasalma) niyə dəstəklənmir?
23. **Polymorphism** (Çoxformalıq) nədir və növləri hansılardır?
24. **Method Overloading** (Metodun yenidən yüklənməsi) nədir?
25. **Method Overriding** (Metodun yenidən təyin olunması) nədir?
26. **Encapsulation** (Kapsulyasiya) nədir?
27. **Abstraction** (Abstraksiya) nədir?
28. **Abstract Class** (Abstrakt Sinif) ilə **Interface** (İnterfeys) arasındakı fərq nədir?
29. Java-da **interface** nə üçün istifadə olunur?
30. **default** metodlar interfeysdə nə üçün təqdim olunub?
31. **static** metodlar interfeysdə necə istifadə olunur?
32. **final** açar sözü siniflərdə nə üçün istifadə olunur?
33. **super()** və **this()** konstruktor çağırışlarının fərqi nədir?
34. **covariant return type** (kovariant qaytarma tipi) nədir?
35. **method hiding** (metod gizlətmə) nədir?
36. Java-da **composition** (kompozisiya) ilə **inheritance** (mirasalma) arasındakı fərq nədir?
37. **has-a** və **is-a** əlaqələri nə deməkdir?
38. **tight coupling** və **loose coupling** nədir?
39. Java-da **inner class** (daxili sinif) nədir?
40. **anonymous class** (anonim sinif) nədir və nə üçün istifadə olunur?

## Data Tipləri və Dəyişənlər
41. Java-da **primitive** və **reference** tipləri arasındakı fərq nədir?
42. **int** və **Integer** arasındakı fərq nədir?
43. Java-da **default** dəyərlər hansılardır?
44. **final** açar sözü dəyişənlərdə necə istifadə olunur?
45. **volatile** açar sözü nə üçün istifadə olunur?
46. **transient** açar sözü nədir?
47. Java-da **enum** nədir və necə istifadə olunur?
48. **var** açar sözü nədir və Java-da necə işləyir?
49. Java-da **type casting** (tip çevirmə) nədir?
50. **widening** və **narrowing** çevirmələri nədir?
51. **instanceof** operatoru nə üçün istifadə olunur?
52. Java-da **wrapper classes** (sarma sinifləri) nədir?
53. **null** dəyəri nə deməkdir?
54. Java-da **array** (massiv) necə təyin olunur?
55. **multidimensional array** (çoxölçülü massiv) nədir?
56. **variable shadowing** (dəyişən kölgələnməsi) nədir?
57. **static variable** (statik dəyişən) ilə **instance variable** (nümunə dəyişəni) arasındakı fərq nədir?
58. Java-da **constant** (sabit) necə təyin olunur?
59. **Unicode** Java-da necə dəstəklənir?
60. Java-da **short-circuit evaluation** (qısa dövrə qiymətləndirmə) nədir?

## Exception Handling
61. **Exception** (İstisna) nədir?
62. **Checked** və **Unchecked** istisnalar arasındakı fərq nədir?
63. **Error** və **Exception** arasındakı fərq nədir?
64. **try-catch** bloku necə işləyir?
65. **finally** bloku nə üçün istifadə olunur?
66. **try-with-resources** nədir?
67. **throws** açar sözü nə üçün istifadə olunur?
68. **throw** açar sözü nədir?
69. Java-da **custom exception** (xüsusi istisna) necə yaradılır?
70. **multi-catch** bloku nədir?
71. **NullPointerException** nədir və nə üçün baş verir?
72. **ArithmeticException** nədir?
73. **ClassCastException** nə vaxt baş verir?
74. **StackOverflowError** nədir?
75. **OutOfMemoryError** nədir?
76. Java-da **exception propagation** (istisna yayılması) necə işləyir?
77. **try** bloku daxilində **return** ifadəsi olduqda **finally** bloku icra olunurmu?
78. **exception chaining** (istisna zənciri) nədir?
79. Java-da **suppressed exceptions** (basıldırılmış istisnalar) nədir?
80. **try-with-resources** ilə **AutoCloseable** interfeysi arasındakı əlaqə nədir?

## Collections Framework
81. **Collections Framework** (Kolleksiyalar Çərçivəsi) nədir?
82. **List**, **Set** və **Map** interfeysləri nədir?
83. **ArrayList** və **LinkedList** arasındakı fərq nədir?
84. **HashSet** və **TreeSet** arasındakı fərq nədir?
85. **HashMap** və **TreeMap** arasındakı fərq nədir?
86. **ConcurrentHashMap** nədir?
87. **Iterator** və **ListIterator** arasındakı fərq nədir?
88. **forEach** metodu necə işləyir?
89. **Comparable** və **Comparator** arasındakı fərq nədir?
90. **Collections.sort()** metodu necə işləyir?
91. **fail-fast** və **fail-safe** iteratorlar nədir?
92. **Vector** və **ArrayList** arasındakı fərq nədir?
93. **Hashtable** və **HashMap** arasındakı fərq nədir?
94. **PriorityQueue** nədir və necə işləyir?
95. **Deque** interfeysi nədir?
96. **CopyOnWriteArrayList** nədir?
97. **Collections.synchronizedList()** nə üçün istifadə olunur?
98. **WeakHashMap** nədir?
99. **IdentityHashMap** nədir?
100. **EnumSet** və **EnumMap** nədir?

## Multithreading
101. **Thread** (Axın) nədir?
102. **Thread** sinfi ilə **Runnable** interfeysi arasındakı fərq nədir?
103. **synchronized** açar sözü nə üçün istifadə olunur?
104. **Thread lifecycle** (axın həyat dövrü) hansı mərhələlərdən ibarətdir?
105. **start()** və **run()** metodları arasındakı fərq nədir?
106. **Thread.sleep()** və **Thread.yield()** arasındakı fərq nədir?
107. **wait()**, **notify()** və **notifyAll()** metodları nədir?
108. **Deadlock** (bloklanma) nədir və necə qarşısı alınır?
109. **Thread Pool** (Axın Hovuzu) nədir?
110. **ExecutorService** nədir?
111. **Callable** və **Runnable** arasındakı fərq nədir?
112. **Future** obyekti nədir?
113. **ReentrantLock** nədir və **synchronized** ilə fərqi nədir?
114. **ThreadLocal** nədir?
115. **volatile** açar sözü thread-lərdə necə istifadə olunur?
116. **race condition** (yarış vəziyyəti) nədir?
117. **thread safety** (axın təhlükəsizliyi) necə təmin olunur?
118. **CountDownLatch** nədir?
119. **CyclicBarrier** nədir?
120. **Semaphore** nədir?

## String və StringBuilder
121. **String** nə üçün **immutable** (dəyişilməz)dir?
122. **StringBuilder** və **StringBuffer** arasındakı fərq nədir?
123. **String Pool** (Sətir Hovuzu) nədir?
124. **String** obyektləri necə müqayisə edilir?
125. **equals()** və **==** operatoru arasındakı fərq nədir?
126. **String.format()** metodu nə üçün istifadə olunur?
127. **String.join()** metodu nədir?
128. **String.intern()** metodu nə edir?
129. **String** sinfində **substring()** metodu necə işləyir?
130. **String** sinfində **replace()** və **replaceAll()** arasındakı fərq nədir?

## Java I/O
131. **InputStream** və **OutputStream** nədir?
132. **Reader** və **Writer** sinifləri nə üçün istifadə olunur?
133. **BufferedReader** və **BufferedWriter** nədir?
134. **FileInputStream** və **FileOutputStream** necə istifadə olunur?
135. **Serializable** interfeysi nədir?
136. **transient** açar sözü serializasiyada necə istifadə olunur?
137. **ObjectInputStream** və **ObjectOutputStream** nədir?
138. **Path** və **Files** sinifləri nədir?
139. **NIO** və **IO** arasındakı fərq nədir?
140. **FileChannel** nədir?

## Generics
141. **Generics** (Ümumiləşdirmə) nədir?
142. **Type Safety** (Tip Təhlükəsizliyi) generics ilə necə təmin olunur?
143. **Wildcard** (<?>**) generics-də nədir?
144. **Bounded Type Parameters** (Məhdud Tip Parametrləri) nədir?
145. **Generic Method** (Ümumi Metod) necə yazılır?
146. **Type Erasure** (Tip Silinməsi) nədir?
147. **Raw Type** (Xam Tip) nədir və niyə istifadə edilməməlidir?
148. **Generic Class** (Ümumi Sinif) necə təyin olunur?
149. **Generic Interface** (Ümumi İnterfeys) nədir?
150. **PECS** (Producer Extends, Consumer Super) prinsipi nədir?

## Lambda İfadələri və Stream API
151. **Lambda Expressions** (Lambda İfadələri) nədir?
152. **Functional Interface** (Funksional İnterfeys) nədir?
153. **Stream API** nədir?
154. **stream()** və **parallelStream()** arasındakı fərq nədir?
155. **filter()**, **map()** və **reduce()** metodları nədir?
156. **Collectors** sinfi nə üçün istifadə olunur?
157. **Optional** sinfi nədir?
158. **forEach()** və **forEachOrdered()** arasındakı fərq nədir?
159. **Stream** ilə **Collection** arasındakı fərq nədir?
160. **Intermediate** və **Terminal** əməliyyatlar nədir?

## Digər Mövzular
161. **Annotations** (Annotasiyalar) nədir?
162. **@Override** annotasiyasının rolu nədir?
163. **Reflection API** nədir?
164. **Class** sinfi nə üçün istifadə olunur?
165. **Proxy** sinfi nədir?
166. **Java-da **enum** ilə **switch** ifadəsi necə istifadə olunur?
167. **record** sinfi nədir?
168. **sealed** siniflər nədir?
169. **pattern matching** Java-da necə işləyir?
170. **text blocks** nədir?
171. **@Deprecated** annotasiyası nə üçün istifadə olunur?
172. **@SuppressWarnings** annotasiyasının məqsədi nədir?
173. **Java-da **varargs** (dəyişkən sayda arqumentlər) nədir?
174. **strictfp** açar sözü nə üçün istifadə olunur?
175. **assert** açar sözü nədir və necə istifadə olunur?
176. **Java-da **clone()** metodu necə işləyir?
177. **Cloneable** interfeysi nədir?
178. **Object** sinfinin əsas metodları hansılardır?
179. **hashCode()** və **equals()** metodları arasındakı əlaqə nədir?
180. **toString()** metodunun məqsədi nədir?
181. **finalize()** metodu nədir və niyə istifadə edilməməlidir?
182. **Java-da **immutable** sinif necə yaradılır?
183. **marker interface** (işarələyici interfeys) nədir?
184. **System.out.println()** necə işləyir?
185. **Java-da **bitwise** operatorlar nədir?
186. **instance initializer block** (nümunə ilkinləşdirmə bloku) nədir?
187. **static initializer block** (statik ilkinləşdirmə bloku) nədir?
188. **Java-da **nested classes** (iç-içə siniflər) hansı növlərə bölünür?
189. **local inner class** (lokal daxili sinif) nədir?
190. **static nested class** (statik iç-içə sinif) nədir?
191. **Java-da **functional programming** (funksional proqramlaşdırma) necə dəstəklənir?
192. **method reference** (metod istinadı) nədir?
193. **constructor reference** (konstruktor istinadı) nədir?
194. **Java-da **try-catch** bloku olmadan istisnalar necə idarə oluna bilər?
195. **Java-da **stack trace** (yığın izi) nədir?
196. **System.gc()** metodunun rolu nədir?
197. **Runtime** sinfi nə üçün istifadə olunur?
198. **Java-da **memory leak** (yaddaş sızması) nədir və necə qarşısı alınır?
199. **WeakReference** və **SoftReference** nədir?
200. **PhantomReference** nədir?
201. **Java-da **atomic** əməliyyatlar nədir?
202. **AtomicInteger** və **AtomicLong** sinifləri nə üçün istifadə olunur?
203. **synchronized** blok ilə **synchronized** metod arasındakı fərq nədir?
204. **Lock** interfeysi nədir?
205. **ReadWriteLock** nədir?
206. **StampedLock** nədir və necə istifadə olunur?
207. **Java-da **thread priority** (axın prioriteti) nədir?
208. **ThreadGroup** nədir?
209. **ForkJoinPool** nədir?
210. **CompletableFuture** nədir və necə istifadə olunur?
211. **Java-da **parallel processing** (paralel emal) necə həyata keçirilir?
212. **Stream API**-da **flatMap()** metodu nədir?
213. **Stream API**-da **peek()** metodu nə üçün istifadə olunur?
214. **Optional** sinfində **orElse()** və **orElseGet()** arasındakı fərq nədir?
215. **Java-da **default methods** ilə **multiple inheritance** necə simulyasiya olunur?
216. **Java-da **record** sinfi ilə **POJO** sinfi arasındakı fərq nədir?
217. **sealed** siniflər ilə **final** siniflər arasındakı fərq nədir?
218. **Java-da **switch expressions** (keçid ifadələri) nədir?
219. **instanceof** ilə **pattern matching** necə işləyir?
220. **Java-da **text blocks** ilə adi **String** literalı arasındakı fərq nədir?
221. **Java-da **record** sinfi ilə **enum** sinfi arasındakı fərq nədir?
222. **Java-da **var** ilə **dynamic typing** (dinamik tipləşdirmə) eynidirmi?
223. **Java-da **deep copy** və **shallow copy** arasındakı fərq nədir?
224. **Object** sinfinin **wait()** metodunun istifadə şərtləri nələrdir?
225. **Java-da **thread interruption** (axın kəsilməsi) necə işləyir?
226. **InterruptedException** nədir və nə üçün baş verir?
227. **Java-da **daemon thread** (demon axın) nədir?
228. **Thread.UncaughtExceptionHandler** nədir?
229. **Java-da **thread dump** (axın yığını) nədir və necə alınır?
230. **Java-da **heap dump** (yığın yığını) nədir?
231. **Java-da **JIT Compiler** (Just-In-Time Kompilyator) nədir?
232. **Java-da **metaspace** nədir və **PermGen** ilə fərqi nədir?
233. **Java-da **class file** (sinif faylı) strukturu necədir?
234. **Java-da **constant pool** (sabit hovuz) nədir?
235. **Java-da **reflection** ilə **introspection** arasındakı fərq nədir?
236. **Field** və **Method** sinifləri **Reflection API**-da nə üçün istifadə olunur?
237. **Java-da **dynamic proxy** (dinamik proksi) nədir?
238. **Java-da **annotation processing** (annotasiya emalı) necə işləyir?
239. **Java-da **custom annotation** (xüsusi annotasiya) necə yaradılır?
240. **RetentionPolicy** nədir və annotasiyalarda necə istifadə olunur?
241. **Java-da **stack** və **heap** yaddaşının ölçüsü necə təyin olunur?
242. **Java-da **OutOfMemoryError** növləri hansılardır?
243. **Java-da **String** sinfinin **hashCode()** metodu necə işləyir?
244. **Java-da **immutable** obyektlərin yaddaş idarəetməsində rolu nədir?
245. **Java-da **String** ilə **StringBuilder** performans baxımından necə fərqlənir?
246. **Java-da **intern()** metodunun performansa təsiri nədir?
247. **Java-da **String** sinfinin **split()** metodu necə işləyir?
248. **Java-da **regex** (requlyar ifadələr) necə istifadə olunur?
249. **Pattern** və **Matcher** sinifləri nə üçün istifadə olunur?
250. **Java-da **Files** sinfinin **walk()** metodu nədir?
251. **Java-da **NIO.2** ilə **Path** manipulyasiyası necə aparılır?
252. **Java-da **WatchService** nədir və necə istifadə olunur?
253. **Java-da **ByteBuffer** nədir?
254. **Java-da **Selector** və **SelectionKey** nədir?
255. **Java-da **AsynchronousFileChannel** nədir?
256. **Java-da **serialVersionUID** nədir və niyə vacibdir?
257. **Java-da **Externalizable** interfeysi nədir?
258. **Java-da **serialization** ilə **deserialization** arasındakı fərq nədir?
259. **Java-da **transient** ilə **volatile** arasındakı fərq nədir?
260. **Java-da **Collections.emptyList()** və **Collections.singletonList()** nədir?
261. **Java-da **Collections.unmodifiableList()** nə üçün istifadə olunur?
262. **Java-da **List.of()** və **Arrays.asList()** arasındakı fərq nədir?
263. **Java-da **Map.of()** metodu nədir?
264. **Java-da **Set.of()** metodu nədir?
265. **Java-da **ConcurrentSkipListMap** nədir?
266. **Java-da **ConcurrentSkipListSet** nədir?
267. **Java-da **BlockingQueue** nədir?
268. **ArrayBlockingQueue** və **LinkedBlockingQueue** arasındakı fərq nədir?
269. **Java-da **DelayQueue** nədir?
270. **Java-da **SynchronousQueue** nədir?
271. **Java-da **Executor** və **ExecutorService** arasındakı fərq nədir?
272. **Java-da **ScheduledExecutorService** nədir?
273. **Java-da **ThreadFactory** nədir?
274. **Java-da **RejectedExecutionHandler** nədir?
275. **Java-da **ThreadPoolExecutor** necə konfiqurasiya olunur?
276. **Java-da **work-stealing** alqoritmi nədir?
277. **Java-da **parallel stream** ilə **ForkJoinPool** arasındakı əlaqə nədir?
278. **Java-da **Spliterator** nədir?
279. **Java-da **Stream** ilə **parallel processing** performansı necə optimallaşdırılır?
280. **Java-da **Optional** sinfinin **ifPresent()** metodu nədir?
281. **Java-da **Optional** sinfinin **orElseThrow()** metodu nədir?
282. **Java-da **Stream API**-da **short-circuiting** nədir?
283. **Java-da **Collectors.groupingBy()** metodu necə işləyir?
284. **Java-da **Collectors.partitioningBy()** metodu nədir?
285. **Java-da **Stream API**-da **sorted()** metodu necə istifadə olunur?
286. **Java-da **Stream API**-da **distinct()** metodu necə işləyir?
287. **Java-da **Stream API**-da **limit()** və **skip()** metodları nədir?
288. **Java-da **Predicate** funksional interfeysi nədir?
289. **Java-da **Consumer** funksional interfeysi nədir?
290. **Java-da **Supplier** funksional interfeysi nədir?
291. **Java-da **Function** funksional interfeysi nədir?
292. **Java-da **BiFunction** nədir?
293. **Java-da **UnaryOperator** və **BinaryOperator** nədir?
294. **Java-da **andThen()** və **compose()** metodları nədir?
295. **Java-da **lambda** ifadələri ilə **closure** necə işləyir?
296. **Java-da **effectively final** dəyişənlər nədir?
297. **Java-da **local variable type inference** (lokal dəyişən tip çıxarımı) necə işləyir?
298. **Java-da **var** açar sözünün məhdudiyyətləri nələrdir?
299. **Java-da **switch** ifadəsində **arrow syntax** (ox sintaksisi) nədir?
300. **Java-da **instanceof** ilə **pattern variable** (nümunə dəyişəni) necə istifadə olunur?

---

# Java və Hibernate Müsahibə Sualları

Bu sənəd Java və Hibernate ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar Core Java və Hibernate-ın əsas mövzularını başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
  - [Ümumi Suallar](#hibernate-ümumi-suallar)
  - [Konfiqurasiya və Arxitektura](#konfiqurasiya-və-arxitektura)
  - [Mapping və Əlaqələr](#mapping-və-əlaqələr)
  - [HQL və Criteria API](#hql-və-criteria-api)
  - [Caching](#caching)
  - [Transaction Management](#transaction-management)
  - [Performance Optimization](#performance-optimization)
  - [JPA ilə Əlaqə](#jpa-ilə-əlaqə)
  - [Digər Mövzular](#hibernate-digər-mövzular)

## Hibernate

### Hibernate Ümumi Suallar
1. **Hibernate** nədir və nə üçün istifadə olunur?
2. **ORM** (Object-Relational Mapping - Obyekt-Relyasiya Xəritələşdirmə) nədir?
3. Hibernate-ın **JDBC** ilə müqayisədə üstünlükləri nələrdir?
4. Hibernate-ın əsas komponentləri hansılardır?
5. Hibernate-ın digər **ORM** alətləri ilə fərqi nədir?
6. Hibernate-ın tarixi və inkişafı haqqında nə bilirsiniz?
7. Hibernate-ın əsas xüsusiyyətləri hansılardır?
8. Hibernate-ın hansı verilənlər bazalarını dəstəkləyir?
9. Hibernate-ın açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?
10. Hibernate-ın istifadəsində hansı çətinliklər ola bilər?

### Konfiqurasiya və Arxitektura
11. **SessionFactory** (Sessiya Fabriki) nədir və necə istifadə olunur?
12. **Session** (Sessiya) nədir və onun rolu nədir?
13. **Configuration** (Konfiqurasiya) obyekti nə üçün istifadə olunur?
14. Hibernate-da **hibernate.cfg.xml** faylının məqsədi nədir?
15. Hibernate-da **hibernate.properties** faylı necə istifadə olunur?
16. **SessionFactory** ilə **Session** arasındakı fərq nədir?
17. Hibernate-da **dialect** (dialekt) nədir və niyə vacibdir?
18. Hibernate-da **connection pool** (əlaqə hovuzu) necə konfiqurasiya olunur?
19. Hibernate-da **thread safety** (axın təhlükəsizliyi) necə təmin olunur?
20. **SessionFactory** thread-safe-dirmi?
21. **Session** obyekti thread-safe-dirmi?
22. Hibernate-da **mapping** (xəritələşdirmə) necə təyin olunur?
23. **Annotation-based** (annotasiya əsaslı) və **XML-based** (XML əsaslı) konfiqurasiya arasındakı fərq nədir?
24. Hibernate-da **JNDI** (Java Naming and Directory Interface) ilə inteqrasiya necə aparılır?
25. Hibernate-da **SchemaUpdate** (Sxem Yeniləməsi) aləti nədir?
26. Hibernate-da **auto schema generation** (avtomatik sxem yaradılması) necə işləyir?
27. Hibernate-da **Transaction** (Tranzaksiya) obyekti nədir?
28. Hibernate-da **Query** (Sorğu) obyekti nədir?
29. Hibernate-da **Criteria** (Kriteriya) obyekti nədir?
30. Hibernate-da **bootstrap** (başlanğıc yükləmə) prosesi necə işləyir?

### Mapping və Əlaqələr
31. Hibernate-da **entity** (varlıq) nədir?
32. **@Entity** annotasiyasının rolu nədir?
33. **@Table** annotasiyası nə üçün istifadə olunur?
34. **@Id** annotasiyası nədir və necə istifadə olunur?
35. **@GeneratedValue** annotasiyası ilə hansı strategiyalar dəstəklənir?
36. **@Column** annotasiyasının məqsədi nədir?
37. Hibernate-da **one-to-one** (bir-bir) əlaqə necə xəritələşdirilir?
38. Hibernate-da **one-to-many** (bir-çox) əlaqə necə təyin olunur?
39. Hibernate-da **many-to-one** (çox-bir) əlaqə necə konfiqurasiya olunur?
40. Hibernate-da **many-to-many** (çox-çox) əlaqə necə yaradılır?
41. **@JoinColumn** annotasiyası nədir?
42. **@JoinTable** annotasiyası nə üçün istifadə olunur?
43. **Unidirectional** (biristiqamətli) və **bidirectional** (ikistiqamətli) əlaqələr arasındakı fərq nədir?
44. Hibernate-da **inheritance mapping** (mirasalma xəritələşdirmə) strategiyaları hansılardır?
45. **Single Table** (Tək Cədvəl) strategiyası nədir?
46. **Table per Class** (Hər Sinif üçün Cədvəl) strategiyası nədir?
47. **Joined** strategiyası nədir?
48. **@DiscriminatorColumn** və **@DiscriminatorValue** annotasiyaları nə üçün istifadə olunur?
49. Hibernate-da **composite key** (mürəkkəb açar) necə təyin olunur?
50. **@Embedded** və **@Embeddable** annotasiyaları nədir?
51. Hibernate-da **lazy loading** (tənbəl yükləmə) nədir?
52. **Eager loading** (həvəsli yükləmə) ilə **lazy loading** arasındakı fərq nədir?
53. **@Fetch** annotasiyası nə üçün istifadə olunur?
54. **FetchType.LAZY** və **FetchType.EAGER** arasındakı fərq nədir?
55. Hibernate-da **cascade** (kaskad) nədir və hansı növləri var?
56. **@Cascade** annotasiyası nədir?
57. Hibernate-da **orphanRemoval** (sahibsiz silinmə) nədir?
58. **@OneToMany** ilə **mappedBy** atributunun rolu nədir?
59. Hibernate-da **polymorphic queries** (çoxformalı sorğular) necə işləyir?
60. Hibernate-da **association** (əlaqə) idarəetməsi necə aparılır?

### HQL və Criteria API
61. **HQL** (Hibernate Query Language - Hibernate Sorğu Dili) nədir?
62. HQL ilə SQL arasındakı fərq nədir?
63. HQL-də **named queries** (adlandırılmış sorğular) nədir?
64. **@NamedQuery** annotasiyası necə istifadə olunur?
65. **@NamedNativeQuery** nədir?
66. HQL-də **parameter binding** (parametr bağlama) necə aparılır?
67. HQL-də **aggregate functions** (toplama funksiyaları) hansılardır?
68. HQL-də **join** əməliyyatları necə həyata keçirilir?
69. **Criteria API** nədir və nə üçün istifadə olunur?
70. **CriteriaQuery** ilə **HQL** arasındakı fərq nədir?
71. **Restrictions** sinfi Criteria API-da nə üçün istifadə olunur?
72. **Projections** Criteria API-da nədir?
73. Criteria API-da **dynamic queries** (dinamik sorğular) necə yaradılır?
74. **QueryDSL** ilə Hibernate-ın Criteria API-sı arasındakı fərq nədir?
75. Hibernate-da **pagination** (səhifələmə) necə həyata keçirilir?
76. HQL-də **subquery** (alt sorğu) necə yazılır?
77. Hibernate-da **stored procedure** (saxlanılan prosedur) necə çağırılır?
78. HQL-də **bulk update** (toplu yeniləmə) necə aparılır?
79. HQL-də **bulk delete** (toplu silmə) necə həyata keçirilir?
80. Hibernate-da **SQL injection** (SQL inyeksiyası) necə qarşısı alınır?

### Caching
81. Hibernate-da **first-level cache** (birinci səviyyəli keş) nədir?
82. **Second-level cache** (ikinci səviyyəli keş) nədir?
83. **First-level cache** ilə **second-level cache** arasındakı fərq nədir?
84. Hibernate-da **query cache** (sorğu keşi) nədir?
85. **EHCache** Hibernate-da necə konfiqurasiya olunur?
86. **Second-level cache** necə aktivləşdirilir?
87. Hibernate-da **cache provider** (keş təminatçısı) nədir?
88. **CacheMode** növləri hansılardır?
89. **@Cache** annotasiyası nə üçün istifadə olunur?
90. Hibernate-da **cache eviction** (keş boşaldılması) necə işləyir?
91. **Dirty checking** (dəyişiklik yoxlaması) caching ilə necə əlaqəlidir?
92. Hibernate-da **cache concurrency strategies** (keş paralelliyi strategiyaları) hansılardır?
93. **Transactional** keş strategiyası nədir?
94. **Read-write** keş strategiyası nədir?
95. **Nonstrict-read-write** keş strategiyası nədir?
96. **Read-only** keş strategiyası nədir?
97. Hibernate-da **cache invalidation** (keş etibarsızlaşdırma) necə aparılır?
98. **Second-level cache** performansına təsir edən amillər nələrdir?
99. Hibernate-da **stateless session** (vəziyyətsiz sessiya) caching-ə necə təsir edir?
100. Hibernate-da **cache** istifadəsinin riskləri nələrdir?

### Transaction Management
101. Hibernate-da **transaction** (tranzaksiya) nədir?
102. **Transaction management** (tranzaksiya idarəetməsi) Hibernate-da necə həyata keçirilir?
103. **@Transactional** annotasiyasının rolu nədir?
104. **JTA** (Java Transaction API) ilə Hibernate inteqrasiyası necə aparılır?
105. **ACID** xüsusiyyətləri Hibernate-da necə təmin olunur?
106. Hibernate-da **rollback** (geri qaytarma) necə işləyir?
107. **Transaction isolation levels** (tranzaksiya izolyasiya səviyyələri) hansılardır?
108. Hibernate-da **optimistic locking** (optimistik kilidləmə) nədir?
109. **Pessimistic locking** (pessimistik kilidləmə) nədir?
110. **@Version** annotasiyası necə istifadə olunur?
111. Hibernate-da **dirty checking** (dəyişiklik yoxlaması) necə işləyir?
112. **Transaction propagation** (tranzaksiya yayılması) növləri nələrdir?
113. Hibernate-da **savepoint** (saxlama nöqtəsi) necə istifadə olunur?
114. **Transaction timeout** (tranzaksiya vaxtaşımı) necə təyin olunur?
115. Hibernate-da **nested transactions** (iç-içə tranzaksiyalar) dəstəklənirmi?
116. **Session.flush()** metodu tranzaksiyalara necə təsir edir?
117. **Session.clear()** metodu caching və tranzaksiyalara necə təsir edir?
118. Hibernate-da **read-only transaction** (yalnız oxuma tranzaksiyası) necə təyin olunur?
119. **TransactionFactory** nədir?
120. Hibernate-da **distributed transactions** (paylanmış tranzaksiyalar) necə idarə olunur?

### Performance Optimization
121. Hibernate-da **N+1 SELECT** problemi nədir?
122. **N+1 SELECT** probleminin qarşısını necə almaq olar?
123. **Batch processing** (toplu emal) Hibernate-da necə həyata keçirilir?
124. **@BatchSize** annotasiyası nə üçün istifadə olunur?
125. Hibernate-da **fetching strategies** (yükləmə strategiyaları) hansılardır?
126. **Entity Graph** (Varlıq Qrafiki) nədir və necə istifadə olunur?
127. **@NamedEntityGraph** annotasiyası nədir?
128. Hibernate-da **lazy initialization exception** (tənbəl ilkinləşdirmə istisnası) nədir?
129. Hibernate-da **query optimization** (sorğu optimallaşdırması) necə aparılır?
130. **StatelessSession** nədir və performans baxımından necə istifadə olunur?
131. Hibernate-da **bulk operations** (toplu əməliyyatlar) performansına təsir edən amillər nələrdir?
132. **Second-level cache** performans optimallaşdırmasında necə istifadə olunur?
133. Hibernate-da **SQL logging** (SQL qeydləri) necə aktivləşdirilir?
134. **Show SQL** parametri nə üçün istifadə olunur?
135. Hibernate-da **indexing** (indeksləmə) performans baxımından necə təsir edir?
136. **Query hints** (sorğu ipucları) Hibernate-da necə istifadə olunur?
137. Hibernate-da **read-only entities** (yalnız oxuma varlıqları) necə təyin olunur?
138. **Projection queries** (proyeksiya sorğuları) performans baxımından nə üçün faydalıdır?
139. Hibernate-da **database connection optimization** (verilənlər bazası əlaqəsi optimallaşdırması) necə aparılır?
140. Hibernate-da **large datasets** (böyük məlumat dəstləri) ilə işləyərkən hansı strategiyalar istifadə olunur?

### JPA ilə Əlaqə
141. **JPA** (Java Persistence API) nədir?
142. Hibernate ilə **JPA** arasındakı fərq nədir?
143. Hibernate-ın **JPA provider** (JPA təminatçısı) kimi rolu nədir?
144. **EntityManager** nədir və necə istifadə olunur?
145. **Persistence Context** (Davamlılıq Konteksti) nədir?
146. **EntityManagerFactory** ilə **SessionFactory** arasındakı fərq nədir?
147. **@PersistenceContext** annotasiyası nə üçün istifadə olunur?
148. JPA-da **merge()** və **persist()** metodları arasındakı fərq nədir?
149. JPA-da **detach()** metodu nə edir?
150. JPA-da **flush()** metodu necə işləyir?
151. Hibernate-da **JPQL** (Java Persistence Query Language) nədir?
152. **JPQL** ilə **HQL** arasındakı fərq nədir?
153. JPA-da **entity lifecycle** (varlıq həyat dövrü) hansı mərhələlərdən ibarətdir?
154. **@EntityListeners** annotasiyası nədir?
155. JPA-da **locking** (kilidləmə) mexanizmləri hansılardır?
156. JPA-da **named queries** (adlandırılmış sorğular) necə təyin olunur?
157. Hibernate-da **JPA annotations** ilə **Hibernate-specific annotations** arasındakı fərq nədir?
158. JPA-da **entity relationships** (varlıq əlaqələri) necə idarə olunur?
159. JPA-da **criteria queries** (kriteriya sorğuları) necə yaradılır?
160. Hibernate-da **JPA** ilə **Spring Data JPA** inteqrasiyası necə aparılır?

### Hibernate Digər Mövzular
161. Hibernate-da **interceptor** (araya daxil olan) nədir?
162. **Hibernate Event Listeners** (Hibernate Hadisə Dinləyiciləri) nədir?
163. Hibernate-da **filters** (süzgəclər) necə istifadə olunur?
164. **@Filter** və **@FilterDef** annotasiyaları nədir?
165. Hibernate-da **auditing** (audit etmə) necə həyata keçirilir?
166. **Hibernate Envers** nədir?
167. Hibernate-da **dynamic mapping** (dinamik xəritələşdirmə) necə aparılır?
168. **@TypeDef** annotasiyası nə üçün istifadə olunur?
169. Hibernate-da **custom types** (xüsusi tiplər) necə təyin olunur?
170. **UserType** interfeysi nədir?
171. Hibernate-da **bytecode enhancement** (baytkod təkmilləşdirmə) nədir?
172. Hibernate-da **validation** (doğrulama) necə həyata keçirilir?
173. **Bean Validation** Hibernate ilə necə inteqrasiya olunur?
174. **@Valid** annotasiyası nədir?
175. Hibernate-da **statistics** (statistika) necə əldə olunur?
176. **SessionFactory.getStatistics()** metodu nə üçün istifadə olunur?
177. Hibernate-da **logging** (qeydiyyat) necə konfiqurasiya olunur?
178. Hibernate-da **multi-tenancy** (çoxkirayəçilik) necə dəstəklənir?
179. **Schema-based multi-tenancy** (sxem əsaslı çoxkirayəçilik) nədir?
180. **Discriminator-based multi-tenancy** (ayırıcı əsaslı çoxkirayəçilik) nədir?
181. Hibernate-da **connection provider** (əlaqə təminatçısı) nədir?
182. Hibernate-da **dialect resolver** (dialekt həlledicisi) nədir?
183. Hibernate-da **schema validation** (sxem doğrulaması) necə aparılır?
184. **Hibernate Tools** nədir?
185. Hibernate-da **reverse engineering** (əks mühəndislik) necə həyata keçirilir?
186. Hibernate-da **integration testing** (inteqrasiya testləri) necə aparılır?
187. **Hibernate Search** nədir?
188. **Hibernate OGM** (Object Grid Mapping) nədir?
189. Hibernate-da **NoSQL** verilənlər bazaları ilə inteqrasiya necə aparılır?
190. Hibernate-da **sharding** (bölüşdürmə) necə dəstəklənir?
191. **Hibernate Validator** nədir?
192. Hibernate-da **batch fetching** (toplu yükləmə) necə konfiqurasiya olunur?
193. Hibernate-da **connection release modes** (əlaqə buraxma rejimləri) hansılardır?
194. **Session.lock()** və **Session.merge()** metodları arasındakı fərq nədir?
195. Hibernate-da **load()** və **get()** metodları arasındakı fərq nədir?
196. **Transient**, **Persistent** və **Detached** vəziyyətləri nədir?
197. Hibernate-da **immutable entity** (dəyişilməz varlıq) necə təyin olunur?
198. Hibernate-da **soft delete** (yumşaq silmə) necə həyata keçirilir?
199. Hibernate-da **event system** (hadisə sistemi) necə işləyir?
200. Hibernate-da **Spring Framework** ilə inteqrasiya necə aparılır?

---

# Spring Boot Müsahibə Sualları

Bu sənəd Java, Hibernate və Spring Boot ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar Core Java, Hibernate və Spring Boot-un əsas və qabaqcıl mövzularını başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
  - [Ümumi Suallar](#spring-boot-ümumi-suallar)
  - [Arxitektura və Konfiqurasiya](#arxitektura-və-konfiqurasiya)
  - [REST API və Web](#rest-api-və-web)
  - [Spring Data və JPA](#spring-data-və-jpa)
  - [Security](#security)
  - [Testing](#testing)
  - [Microservices](#microservices)
  - [Performance və Optimization](#performance-və-optimization)
  - [Actuator və Monitoring](#actuator-və-monitoring)
  - [Digər Mövzular](#spring-boot-digər-mövzular)

## Spring Boot

### Spring Boot Ümumi Suallar
1. **Spring Boot** nədir və nə üçün istifadə olunur?
2. **Spring Framework** ilə **Spring Boot** arasındakı fərq nədir?
3. Spring Boot-un əsas xüsusiyyətləri hansılardır?
4. **Auto-configuration** (Avtomatik konfiqurasiya) Spring Boot-da nədir?
5. Spring Boot-un digər Java framework-ləri ilə müqayisədə üstünlükləri nələrdir?
6. Spring Boot-un **starter dependencies** (başlanğıc asılılıqlar) nədir?
7. **Spring Initializr** nədir və necə istifadə olunur?
8. Spring Boot-un **embedded server** (daxili server) mexanizmi necə işləyir?
9. Spring Boot-da **Tomcat**, **Jetty** və **Undertow** serverləri arasındakı fərq nədir?
10. Spring Boot-un açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?
11. Spring Boot-un hansı layihə növləri üçün uyğun olduğunu düşünürsünüz?
12. **Spring Boot CLI** nədir və necə istifadə olunur?
13. Spring Boot-un inkişaf tarixi haqqında nə bilirsiniz?
14. Spring Boot ilə **monolith** ( monolitik) və **microservices** (mikroservis) arxitekturaları arasındakı fərq nədir?
15. Spring Boot-da **dependency injection** (asılılıq yeridilməsi) necə işləyir?

### Arxitektura və Konfiqurasiya
16. **Spring Boot Application** necə işə salınır?
17. **@SpringBootApplication** annotasiyasının daxilində hansı annotasiyalar var?
18. **@EnableAutoConfiguration** annotasiyasının rolu nədir?
19. **@ComponentScan** annotasiyası nə üçün istifadə olunur?
20. **@Configuration** annotasiyası nədir?
21. **application.properties** və **application.yml** faylları arasındakı fərq nədir?
22. Spring Boot-da **profiles** (profillər) necə istifadə olunur?
23. **@Profile** annotasiyası nə üçün istifadə olunur?
24. Spring Boot-da **externalized configuration** (xarici konfiqurasiya) necə həyata keçirilir?
25. **@Value** annotasiyası ilə xassələrə (properties) necə daxil olunur?
26. **@ConfigurationProperties** annotasiyası nədir?
27. Spring Boot-da **custom properties** (xüsusi xassələr) necə təyin olunur?
28. **Spring Boot Starter** necə yaradılır?
29. **@Bean** annotasiyası nə üçün istifadə olunur?
30. Spring Boot-da **conditional beans** (şərtli bean-lər) necə təyin olunur?
31. **@ConditionalOnProperty** annotasiyası nədir?
32. **@ConditionalOnClass** və **@ConditionalOnMissingClass** annotasiyaları nədir?
33. Spring Boot-da **banner** (başlıq) necə fərdiləşdirilir?
34. **Spring Boot Actuator** nədir və necə konfiqurasiya olunur?
35. Spring Boot-da **logging** (qeydiyyat) necə konfiqurasiya olunur?
36. **Logback**, **Log4j2** və **SLF4J** arasındakı fərq nədir?
37. Spring Boot-da **log levels** (qeyd səviyyələri) necə təyin olunur?
38. **@PropertySource** annotasiyası nə üçün istifadə olunur?
39. Spring Boot-da **environment** (mühit) obyekti nədir?
40. **SpringApplication** sinfi nə üçün istifadə olunur?
41. Spring Boot-da **application context** (tətbiq konteksti) necə işləyir?
42. **ApplicationRunner** və **CommandLineRunner** arasındakı fərq nədir?
43. Spring Boot-da **graceful shutdown** (nəzakətli dayandırma) necə həyata keçirilir?
44. **Spring Boot DevTools** nədir və necə istifadə olunur?
45. Spring Boot-da **hot swapping** (isti dəyişmə) necə işləyir?

### REST API və Web
46. Spring Boot-da **REST API** necə yaradılır?
47. **@RestController** annotasiyası nədir?
48. **@Controller** ilə **@RestController** arasındakı fərq nədir?
49. **@RequestMapping** annotasiyasının rolu nədir?
50. **@GetMapping**, **@PostMapping**, **@PutMapping** və **@DeleteMapping** annotasiyaları nədir?
51. **@PathVariable** ilə **@RequestParam** arasındakı fərq nədir?
52. **@RequestBody** annotasiyası nə üçün istifadə olunur?
53. **@ResponseBody** annotasiyasının məqsədi nədir?
54. Spring Boot-da **HTTP status codes** (HTTP status kodları) necə idarə olunur?
55. **ResponseEntity** sinfi nə üçün istifadə olunur?
56. Spring Boot-da **exception handling** (istisna idarəetmə) REST API-lərdə necə həyata keçirilir?
57. **@ExceptionHandler** annotasiyası nədir?
58. **@ControllerAdvice** annotasiyasının rolu nədir?
59. Spring Boot-da **global exception handling** (qlobal istisna idarəetmə) necə təyin olunur?
60. **@ResponseStatus** annotasiyası nə üçün istifadə olunur?
61. Spring Boot-da **CORS** (Cross-Origin Resource Sharing) necə konfiqurasiya olunur?
62. **WebMvcConfigurer** nədir və necə istifadə olunur?
63. Spring Boot-da **content negotiation** (məzmun razılaşması) necə işləyir?
64. **Jackson** ilə JSON serializasiyası necə fərdiləşdirilir?
65. **@JsonProperty** annotasiyası nədir?
66. **@JsonIgnore** və **@JsonInclude** annotasiyaları nə üçün istifadə olunur?
67. Spring Boot-da **HATEOAS** (Hypermedia as the Engine of Application State) necə həyata keçirilir?
68. **@RestControllerAdvice** annotasiyası nədir?
69. Spring Boot-da **file upload** (fayl yükləmə) necə həyata keçirilir?
70. Spring Boot-da **multipart requests** (çoxhissəli sorğular) necə idarə olunur?
71. **Spring WebFlux** nədir və Spring Boot ilə necə istifadə olunur?
72. **Reactive programming** (reaktiv proqramlaşdırma) Spring Boot-da necə dəstəklənir?
73. **Mono** və **Flux** sinifləri nədir?
74. **WebClient** ilə **RestTemplate** arasındakı fərq nədir?
75. Spring Boot-da **server-sent events** (server tərəfindən göndərilən hadisələr) necə həyata keçirilir?
76. **Spring MVC** ilə **Spring WebFlux** arasındakı fərq nədir?
77. Spring Boot-da **interceptors** (araya daxil olanlar) necə təyin olunur?
78. **HandlerInterceptor** nədir?
79. Spring Boot-da **custom HTTP headers** (xüsusi HTTP başlıqları) necə əlavə olunur?
80. Spring Boot-da **REST versioning** (REST versiyalaşdırma) necə aparılır?

### Spring Data və JPA
81. **Spring Data JPA** nədir?
82. **Spring Data** ilə Hibernate arasındakı əlaqə nədir?
83. **@Repository** annotasiyasının rolu nədir?
84. **JpaRepository** ilə **CrudRepository** arasındakı fərq nədir?
85. Spring Data-da **custom repository** (xüsusi anbar) necə yaradılır?
86. **@Query** annotasiyası ilə JPQL sorğuları necə yazılır?
87. **@Param** annotasiyası nə üçün istifadə olunur?
88. Spring Data-da **native queries** (yerli sorğular) necə təyin olunur?
89. **Spring Data Specifications** nədir və necə istifadə olunur?
90. **@Entity** və **@Table** annotasiyaları Spring Data-da necə istifadə olunur?
91. Spring Data-da **pagination** (səhifələmə) necə həyata keçirilir?
92. **Pageable** və **Slice** sinifləri nədir?
93. Spring Data-da **sorting** (sıralama) necə təyin olunur?
94. **@Transactional** annotasiyası Spring Data-da necə işləyir?
95. Spring Data-da **optimistic locking** (optimistik kilidləmə) necə həyata keçirilir?
96. **@Version** annotasiyası Spring Data-da nə üçün istifadə olunur?
97. Spring Data-da **entity relationships** (varlıq əlaqələri) necə idarə olunur?
98. **@OneToMany**, **@ManyToOne** və **@ManyToMany** annotasiyaları necə istifadə olunur?
99. Spring Data-da **lazy loading** (tənbəl yükləmə) necə konfiqurasiya olunur?
100. **EntityManager** Spring Data ilə necə istifadə olunur?
101. Spring Data-da **auditing** (audit etmə) necə həyata keçirilir?
102. **@CreatedDate** və **@LastModifiedDate** annotasiyaları nədir?
103. Spring Data-da **soft delete** (yumşaq silmə) necə təyin olunur?
104. **Spring Data JDBC** ilə **Spring Data JPA** arasındakı fərq nədir?
105. Spring Data-da **projections** (proyeksiyalar) necə istifadə olunur?
106. **Spring Data MongoDB** nədir və necə işləyir?
107. **@Document** annotasiyası nədir?
108. **Spring Data Redis** necə istifadə olunur?
109. Spring Data-da **custom queries** (xüsusi sorğular) necə yazılır?
110. Spring Data-da **transaction management** (tranzaksiya idarəetmə) necə həyata keçirilir?

### Security
111. **Spring Security** nədir və Spring Boot ilə necə inteqrasiya olunur?
112. **@EnableWebSecurity** annotasiyasının rolu nədir?
113. Spring Security-də **authentication** (autentifikasiya) necə işləyir?
114. Spring Security-də **authorization** (səlahiyyətləndirmə) necə təyin olunur?
115. **SecurityFilterChain** nədir?
116. **@Secured** və **@PreAuthorize** annotasiyaları arasındakı fərq nədir?
117. Spring Security-də **role-based access control** (rol əsaslı giriş nəzarəti) necə həyata keçirilir?
118. **@AuthenticationPrincipal** annotasiyası nədir?
119. Spring Security-də **JWT** (JSON Web Token) necə istifadə olunur?
120. **OAuth2** Spring Boot ilə necə konfiqurasiya olunur?
121. **OpenID Connect** ilə **OAuth2** arasındakı fərq nədir?
122. Spring Security-də **CSRF** (Cross-Site Request Forgery) qoruması necə aktivləşdirilir?
123. Spring Security-də **CORS** necə idarə olunur?
124. **PasswordEncoder** nədir və hansı alqoritmlər dəstəklənir?
125. **BCrypt** ilə **Argon2** şifrələmə alqoritmləri arasındakı fərq nədir?
126. Spring Security-də **remember-me** funksionallığı necə həyata keçirilir?
127. **SecurityContext** nədir və necə istifadə olunur?
128. Spring Security-də **method-level security** (metod səviyyəsində təhlükəsizlik) necə təyin olunur?
129. **@PostAuthorize** annotasiyası nə üçün istifadə olunur?
130. Spring Security-də **custom authentication provider** (xüsusi autentifikasiya təminatçısı) necə yaradılır?
131. Spring Security-də **LDAP** inteqrasiyası necə aparılır?
132. Spring Security-də **SAML** necə konfiqurasiya olunur?
133. **Spring Security OAuth** ilə **Spring Authorization Server** arasındakı fərq nədir?
134. Spring Security-də **session management** (sessiya idarəetmə) necə həyata keçirilir?
135. Spring Security-də **stateless authentication** (vəziyyətsiz autentifikasiya) necə təyin olunur?

### Testing
136. **Spring Boot Test** nədir və necə istifadə olunur?
137. **@SpringBootTest** annotasiyasının rolu nədir?
138. **@WebMvcTest** ilə **@DataJpaTest** arasındakı fərq nədir?
139. **@MockBean** və **@SpyBean** annotasiyaları nədir?
140. **Mockito** Spring Boot ilə necə istifadə olunur?
141. **@Test** annotasiyası nə üçün istifadə olunur?
142. Spring Boot-da **integration testing** (inteqrasiya testləri) necə aparılır?
143. **TestRestTemplate** nədir və necə istifadə olunur?
144. **@AutoConfigureMockMvc** annotasiyası nədir?
145. Spring Boot-da **unit testing** (vahid testləri) necə həyata keçirilir?
146. **@Transactional** annotasiyası testlərdə necə istifadə olunur?
147. Spring Boot-da **test profiles** (test profilləri) necə təyin olunur?
148. **@DirtiesContext** annotasiyası nə üçün istifadə olunur?
149. Spring Boot-da **embedded database** (daxili verilənlər bazası) testlərdə necə istifadə olunur?
150. **H2 Database** Spring Boot testlərində necə konfiqurasiya olunur?
151. **Testcontainers** Spring Boot ilə necə istifadə olunur?
152. **@RestClientTest** annotasiyası nədir?
153. Spring Boot-da **performance testing** (performans testləri) necə aparılır?
154. **JMeter** ilə Spring Boot tətbiqləri necə test edilir?
155. Spring Boot-da **security testing** (təhlükəsizlik testləri) necə həyata keçirilir?
156. **@ActiveProfiles** annotasiyası testlərdə necə istifadə olunur?

### Microservices
157. Spring Boot ilə **microservices** (mikroservis) arxitekturası necə qurulur?
158. **Spring Cloud** nədir və Spring Boot ilə necə inteqrasiya olunur?
159. **Eureka** ilə **service discovery** (xidmət kəşfi) necə həyata keçirilir?
160. **@EnableEurekaClient** annotasiyasının rolu nədir?
161. **Spring Cloud Config** nədir və necə konfiqurasiya olunur?
162. **Spring Cloud Gateway** nədir?
163. **API Gateway** ilə **Load Balancer** arasındakı fərq nədir?
164. **Spring Cloud LoadBalancer** necə istifadə olunur?
165. **Spring Cloud OpenFeign** ilə REST müştəriləri necə yaradılır?
166. **@FeignClient** annotasiyası nədir?
167. **Spring Cloud Circuit Breaker** nədir?
168. **Resilience4j** ilə **circuit breaker** necə konfiqurasiya olunur?
169. **Spring Cloud Sleuth** nədir və necə istifadə olunur?
170. **Distributed tracing** (paylanmış izləmə) Spring Boot-da necə həyata keçirilir?
171. **Zipkin** ilə Spring Boot inteqrasiyası necə aparılır?
172. **Spring Cloud Bus** nədir?
173. **Spring Cloud Stream** nədir və necə istifadə olunur?
174. **Kafka** ilə Spring Boot inteqrasiyası necə həyata keçirilir?
175. **RabbitMQ** ilə Spring Boot inteqrasiyası necə aparılır?
176. **Spring Cloud Task** nədir?
177. **Spring Batch** ilə Spring Boot-da toplu emal necə həyata keçirilir?
178. **Spring Cloud Data Flow** nədir?
179. **Event-driven architecture** (hadisə yönümlü arxitektura) Spring Boot-da necə qurulur?
180. **CQRS** (Command Query Responsibility Segregation) Spring Boot ilə necə həyata keçirilir?

### Performance və Optimization
181. Spring Boot-da **performance tuning** (performans tənzimləmə) necə aparılır?
182. **Spring Boot Actuator** ilə performans monitorinqi necə həyata keçirilir?
183. Spring Boot-da **connection pooling** (əlaqə hovuzu) necə optimallaşdırılır?
184. **HikariCP** ilə Spring Boot inteqrasiyası necə aparılır?
185. Spring Boot-da **caching** (keşləmə) necə həyata keçirilir?
186. **@Cacheable** annotasiyası nədir?
187. **Spring Cache** ilə **EhCache** necə istifadə olunur?
188. **Spring Cache** ilə **Redis** necə konfiqurasiya olunur?
189. Spring Boot-da **lazy initialization** (tənbəl ilkinləşdirmə) necə aktivləşdirilir?
190. Spring Boot-da **thread pool** (axın hovuzu) necə konfiqurasiya olunur?
191. **TaskExecutor** nədir və necə istifadə olunur?
192. Spring Boot-da **async processing** (asinxron emal) necə həyata keçirilir?
193. **@Async** annotasiyası nədir?
194. Spring Boot-da **database query optimization** (verilənlər bazası sorğu optimallaşdırması) necə aparılır?
195. **N+1 SELECT** problemi Spring Boot-da necə həll olunur?
196. **Entity Graph** Spring Data ilə necə istifadə olunur?
197. Spring Boot-da **batch processing** (toplu emal) necə optimallaşdırılır?
198. **Spring Boot Metrics** ilə performans necə ölçülür?
199. **Micrometer** ilə Spring Boot inteqrasiyası necə aparılır?
200. Spring Boot-da **memory management** (yaddaş idarəetmə) necə optimallaşdırılır?

### Actuator və Monitoring
201. **Spring Boot Actuator** nədir?
202. **Actuator endpoints** (Aktuator uç nöqtələri) hansılardır?
203. **/health** endpoint-i necə fərdiləşdirilir?
204. **/metrics** endpoint-i ilə hansı məlumatlar əldə olunur?
205. **/info** endpoint-i necə konfiqurasiya olunur?
206. **@Endpoint** annotasiyası ilə xüsusi actuator endpoint-i necə yaradılır?
207. Spring Boot Actuator ilə **Prometheus** inteqrasiyası necə aparılır?
208. **Grafana** ilə Spring Boot monitorinqi necə qurulur?
209. **Spring Boot Admin** nədir və necə istifadə olunur?
210. **Actuator** ilə **JMX** (Java Management Extensions) necə istifadə olunur?
211. **/loggers** endpoint-i necə istifadə olunur?
212. **/heapdump** endpoint-i nə üçün istifadə olunur?
213. **/threaddump** endpoint-i ilə hansı məlumatlar əldə olunur?
214. Spring Boot Actuator ilə **custom health indicators** (xüsusi sağlamlıq göstəriciləri) necə yaradılır?
215. **Actuator** təhlükəsizliyi necə təmin olunur?

### Spring Boot Digər Mövzular
216. **Spring Boot** ilə **WebSocket** necə həyata keçirilir?
217. **@EnableWebSocket** annotasiyasının rolu nədir?
218. **STOMP** protokolu Spring Boot-da necə istifadə olunur?
219. **Spring Integration** nədir və Spring Boot ilə necé inteqrasiya olunur?
220. **Spring Session** nədir və necə konfiqurasiya olunur?
221. **Spring Boot** ilə **Redis** sessiya idarəetməsi necə həyata keçirilir?
222. **Spring Boot** ilə **GraphQL** necə istifadə olunur?
223. **@GraphQLQuery** annotasiyası nədir?
224. **Spring Boot** ilə **gRPC** necə inteqrasiya olunur?
225. **Spring Boot** ilə **Apache Camel** necə istifadə olunur?
226. **Spring Boot** ilə **JMS** (Java Message Service) necə konfiqurasiya olunur?
227. **ActiveMQ** ilə Spring Boot inteqrasiyası necə aparılır?
228. **Spring Boot** ilə **email sending** (e-poçt göndərmə) necé həyata keçirilir?
229. **Spring Boot** ilə **scheduled tasks** (planlaşdırılmış tapşırıqlar) necə təyin olunur?
230. **@Scheduled** annotasiyası nədir?
231. **Spring Boot** ilə **Quartz Scheduler** necə inteqrasiya olunur?
232. **Spring Boot** ilə **file processing** (fayl emalı) necə həyata keçirilir?
233. **Spring Boot** ilə **PDF generation** (PDF yaradılması) necə aparılır?
234. **Spring Boot** ilə **Excel processing** (Excel emalı) necə həyata keçirilir?
235. **Spring Boot** ilə **Apache POI** necə istifadə olunur?
236. **Spring Boot** ilə ** internationalization** (beynəlxalqləşdirmə) necə həyata keçirilir?
237. **MessageSource** nədir və necə istifadə olunur?
238. **Spring Boot** ilə **validation** (doğrulama) necə həyata keçirilir?
239. **@Valid** və **@Validated** annotasiyaları arasındakı fərq nədir?
240. **Spring Boot** ilə **custom validators** (xüsusi doğrulayıcılar) necə yaradılır?
241. **Spring Boot** ilé **Swagger** necə inteqrasiya olunur?
242. **@OpenAPIDefinition** annotasiyası nədir?
243. **Spring Boot** ilə **OpenAPI** spesifikasiyası necə yaradılır?
244. **Spring Boot** ilé **API documentation** (API sənədləşdirmə) necə aparılır?
245. **Spring Boot** ilə **Flyway** necə istifadə olunur?
246. **Liquibase** ilə Spring Boot inteqrasiyası necə aparılır?
247. **Spring Boot** ilé **database migration** (verilənlər bazası miqrasiyası) necə həyata keçirilir?
248. **Spring Boot** ilə **JDBC Template** necə istifadə olunur?
249. **Spring Boot** ilə **MyBatis** necé inteqrasiya olunur?
250. **Spring Boot** ilə **NoSQL** verilənlər bazaları necə istifadə olunur?
251. **Spring Boot** ilə **Cassandra** inteqrasiyası necə aparılır?
252. **Spring Boot** ilə **Neo4j** necə istifadə olunur?
253. **Spring Boot** ilə **DynamoDB** necə konfiqurasiya olunur?
254. **Spring Boot** ilé **search engines** (axtarış mühərrikləri) necé inteqrasiya olunur?
255. **Elasticsearch** ilé Spring Boot inteqrasiyası necə aparılır?
256. **Spring Boot** ilé **Solr** necé istifadə olunur?
257. **Spring Boot** ilé **event sourcing** (hadisə mənbəyi) necé həyata keçirilir?
258. **Spring Boot** ilé **CQRS** necé inteqrasiya olunur?
259. **Spring Boot** ilé **Docker** necé istifadə olunur?
260. **Spring Boot** ilé **Kubernetes** necé inteqrasiya olunur?
261. **Spring Boot** ilé **CI/CD** (Continuous Integration/Continuous Deployment) necé qurulur?
262. **Spring Boot** ilé **Jenkins** necé istifadə olunur?
263. **Spring Boot** ilé **GitHub Actions** necé konfiqurasiya olunur?
264. **Spring Boot** ilé **cloud platforms** (bulud platformaları) necé inteqrasiya olunur?
265. **Spring Boot** ilé **AWS** (Amazon Web Services) necé istifadə olunur?
266. **Spring Boot** ilé **S3** (Simple Storage Service) necé konfiqurasiya olunur?
267. **Spring Boot** ilé **EC2** (Elastic Compute Cloud) necé istifadə olunur?
268. **Spring Boot** ilé **Lambda** funksiyaları necé yaradılır?
269. **Spring Boot** ilé **Azure** necé inteqrasiya olunur?
270. **Spring Boot** ilé **Google Cloud Platform** necé istifadə olunur?
271. **Spring Boot** ilé **Heroku** necé konfiqurasiya olunur?
272. **Spring Boot** ilé **serverless architecture** (serversiz arxitektura) necé qurulur?
273. **Spring Boot** ilé **GraalVM** necé istifadə olunur?
274. **Spring Native** nədir və necé istifadə olunur?
275. **Spring Boot** ilé **AOT** (Ahead-of-Time) kompilyasiyası necé həyata keçirilir?
276. **Spring Boot** ilé **reactive microservices** (reaktiv mikroservislər) necé qurulur?
277. **Spring Boot** ilé **gRPC** mikroservisləri necé yaradılır?
278. **Spring Boot** ilé **event-driven microservices** (hadisə yönümlü mikroservislər) necé qurulur?
279. **Spring Boot** ilé **health checks** (sağlamlıq yoxlamaları) necé fərdiləşdirilir?
280. **Spring Boot** ilé **custom metrics** (xüsusi metrikalar) necé yaradılır?
281. **Spring Boot** ilé **distributed locking** (paylanmış kilidləmə) necé həyata keçirilir?
282. **Spring Boot** ilé **ZooKeeper** necé inteqrasiya olunur?
283. **Spring Boot** ilé **Consul** necé istifadə olunur?
284. **Spring Boot** ilé **service mesh** (xidmət şəbəkəsi) necé qurulur?
285. **Spring Boot** ilé **Istio** necé inteqrasiya olunur?
286. **Spring Boot** ilé **Chaos Engineering** (xaos mühəndisliyi) necé həyata keçirilir?
287. **Spring Boot** ilé **resilience patterns** (dayanıqlılıq nümunələri) necé tətbiq olunur?
288. **Spring Boot** ilé **rate limiting** (sürət məhdudlaşdırması) necé həyata keçirilir?
289. **Spring Boot** ilé **API throttling** (API məhdudlaşdırması) necé konfiqurasiya olunur?
290. **Spring Boot** ilé **blue-green deployment** (mavi-yaşıl yerləşdirmə) necé aparılır?
291. **Spring Boot** ilé **canary deployment** (kanarya yerləşdirmə) necé həyata keçirilir?
292. **Spring Boot** ilé **A/B testing** necé qurulur?
293. **Spring Boot** ilé **feature toggles** (xüsusiyyət açarları) necé istifadə olunur?
294. **Spring Boot** ilé **log aggregation** (qeyd toplama) necé həyata keçirilir?
295. **Spring Boot** ilé **ELK Stack** (Elasticsearch, Logstash, Kibana) necé inteqrasiya olunur?
296. **Spring Boot** ilé **Prometheus** və **Grafana** ilə monitorinq necé qurulur?
297. **Spring Boot** ilé **OpenTelemetry** necé istifadə olunur?
298. **Spring Boot** ilé **distributed logging** (paylanmış qeydiyyat) necé həyata keçirilir?
299. **Spring Boot** ilé **observability** (müşahidə oluna bilmə) necé təmin olunur?
300. **Spring Boot** ilé **SRE** (Site Reliability Engineering) prinsipləri necé tətbiq olunur?

---

# Data Structures/Collections Müsahibə Sualları

Bu sənəd Java, Hibernate, Spring Boot və Data Structures/Collections ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar Core Java, Hibernate, Spring Boot və Data Structures/Collections-un əsas və qabaqcıl mövzularını başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Array və String](#array-və-string)
  - [List və Set](#list-və-set)
  - [Map](#map)
  - [Queue və Stack](#queue-və-stack)
  - [Tree və Graph](#tree-və-graph)
  - [Hashing və Performance](#hashing-və-performance)
  - [Algorithms və Collections](#algorithms-və-collections)
  - [Digər Mövzular](#digər-mövzular)

## Data Structures və Collections

### Ümumi Suallar
1. **Data Structure** (Məlumat Strukturu) nədir və niyə vacibdir?
2. **Collections Framework** (Kolleksiyalar Çərçivəsi) Java-da nədir?
3. **Collection** interfeysi ilə **Collections** sinfi arasındakı fərq nədir?
4. Java-da **List**, **Set** və **Map** interfeyslərinin əsas xüsusiyyətləri nələrdir?
5. **Data Structure** növləri hansılardır?
6. **Linear Data Structure** (Xətti Məlumat Strukturu) ilə **Non-linear Data Structure** (Qeyri-xətti Məlumat Strukturu) arasındakı fərq nədir?
7. Java-da **dynamic data structures** (dinamik məlumat strukturları) hansılardır?
8. **Time Complexity** (Vaxt Mürəkkəbliyi) və **Space Complexity** (Yer Mürəkkəbliyi) nədir?
9. Java-da **boxing** və **unboxing** Collections ilə necə əlaqəlidir?
10. **Comparable** və **Comparator** interfeysləri nədir?
11. Java-da **Iterator** nədir və necə istifadə olunur?
12. **ListIterator** ilə **Iterator** arasındakı fərq nədir?
13. **Fail-fast** və **fail-safe** iteratorlar nədir?
14. Java-da **generics** (ümumiləşdirmə) Collections ilə necə istifadə olunur?
15. **Type safety** (tip təhlükəsizliyi) Collections-da necə təmin olunur?

### Array və String
16. **Array** (Massiv) nədir və Java-da necə təyin olunur?
17. **Static Array** (Statik Massiv) ilə **Dynamic Array** (Dinamik Massiv) arasındakı fərq nədir?
18. Java-da **multidimensional array** (çoxölçülü massiv) necə işləyir?
19. **ArrayList** ilə **Array** arasındakı fərq nədir?
20. Java-da **array** ölçüsünün dəyişdirilməsi mümkündürmü?
21. **System.arraycopy()** metodu nə üçün istifadə olunur?
22. Java-da **jagged array** (qeyri-bərabər massiv) nədir?
23. **Arrays** sinfinin əsas metodları hansılardır?
24. **Arrays.sort()** metodu necə işləyir?
25. **Arrays.binarySearch()** metodu nə üçün istifadə olunur?
26. Java-da **String** sinfi məlumat strukturu kimi necə istifadə olunur?
27. **String Pool** (Sətir Hovuzu) nədir və necə işləyir?
28. **String** ilə **char array** (simvol massivi) arasındakı fərq nədir?
29. **StringBuilder** ilə **StringBuffer** performans baxımından necə fərqlənir?
30. Java-da **immutable** (dəyişilməz) String-in üstünlükləri nələrdir?

### List və Set
31. **List** (Siyahı) interfeysi nədir və hansı siniflər tərəfindən implement edilir?
32. **ArrayList** nədir və necə işləyir?
33. **LinkedList** nədir və necə işləyir?
34. **ArrayList** ilə **LinkedList** arasındakı fərq nədir?
35. **Vector** nədir və **ArrayList** ilə fərqi nədir?
36. **CopyOnWriteArrayList** nədir və nə üçün istifadə olunur?
37. Java-da **List** üzərində **synchronized** əməliyyatlar necə aparılır?
38. **Collections.synchronizedList()** metodu nə edir?
39. **List** üzərində **iteration** (təkrarlama) zamanı **ConcurrentModificationException** niyə baş verir?
40. **Set** (Dəst) interfeysi nədir və hansı siniflər tərəfindən implement edilir?
41. **HashSet** nədir və necə işləyir?
42. **LinkedHashSet** ilə **HashSet** arasındakı fərq nədir?
43. **TreeSet** nədir və necə işləyir?
44. **HashSet** ilə **TreeSet** arasındakı fərq nədir?
45. **EnumSet** nədir və nə üçün istifadə olunur?
46. Java-da **Set** üzərində **duplicate** (təkrar) elementlərin qarşısını necə almaq olar?
47. **Set** ilə **List** arasındakı əsas fərqlər nələrdir?
48. **ConcurrentSkipListSet** nədir və nə üçün istifadə olunur?
49. **List.of()** və **Set.of()** metodları nədir?
50. **Collections.unmodifiableList()** və **Collections.unmodifiableSet()** nə edir?

### Map
51. **Map** (Xəritə) interfeysi nədir və hansı siniflər tərəfindən implement edilir?
52. **HashMap** nədir və necə işləyir?
53. **LinkedHashMap** ilə **HashMap** arasındakı fərq nədir?
54. **TreeMap** nədir və necə işləyir?
55. **HashMap** ilə **TreeMap** arasındakı fərq nədir?
56. **ConcurrentHashMap** nədir və nə üçün istifadə olunur?
57. **Hashtable** ilə **HashMap** arasındakı fərq nədir?
58. **WeakHashMap** nədir və necə istifadə olunur?
59. **IdentityHashMap** nədir və nə üçün istifadə olunur?
60. **EnumMap** nədir və necə işləyir?
61. **Map.of()** metodu nədir?
62. **Collections.synchronizedMap()** metodu nə edir?
63. **HashMap**-in daxili strukturu necədir?
64. **HashMap**-də **load factor** (yükləmə faktoru) nədir?
65. **HashMap**-də **rehashing** (yenidən xəşləmə) necə baş verir?
66. **ConcurrentHashMap**-in **segmentation** (seqmentləşdirmə) mexanizmi necə işləyir?
67. **Map**-də **null** açar və dəyərlərə icazə verən siniflər hansılardır?
68. **Map.Entry** interfeysi nədir və necə istifadə olunur?
69. **HashMap**-də **collision** (toqquşma) necə idarə olunur?
70. **TreeMap**-də **Red-Black Tree** (Qırmızı-Qara Ağac) necə işləyir?

### Queue və Stack
71. **Queue** (Növbə) interfeysi nədir və hansı siniflər tərəfindən implement edilir?
72. **PriorityQueue** nədir və necə işləyir?
73. **Deque** (İkiucalı Növbə) nədir və necə istifadə olunur?
74. **ArrayDeque** ilə **LinkedList** arasındakı fərq nədir?
75. **BlockingQueue** nədir və nə üçün istifadə olunur?
76. **ArrayBlockingQueue** ilə **LinkedBlockingQueue** arasındakı fərq nədir?
77. **PriorityBlockingQueue** nədir?
78. **SynchronousQueue** nədir və necə işləyir?
79. **DelayQueue** nədir və nə üçün istifadə olunur?
80. **ConcurrentLinkedQueue** nədir?
81. **Stack** (Yığın) nədir və Java-da necə istifadə olunur?
82. **Stack** sinfi ilə **Deque** arasındakı fərq nədir?
83. Java-da **LIFO** (Last In, First Out - Son Girən, İlk Çıxan) prinsipi necə həyata keçirilir?
84. Java-da **FIFO** (First In, First Out - İlk Girən, İlk Çıxan) prinsipi necə tətbiq olunur?
85. **Queue**-də **offer()** və **add()** metodları arasındakı fərq nədir?
86. **Queue**-də **poll()** və **remove()** metodları arasındakı fərq nədir?
87. **PriorityQueue**-də elementlərin sıralanması necə təmin olunur?
88. **Deque**-də **push()** və **pop()** metodları nə üçün istifadə olunur?
89. **BlockingQueue**-də **put()** və **take()** metodları necə işləyir?
90. **Queue** ilə **List** arasındakı fərqlər nələrdir?

### Tree və Graph
91. **Tree** (Ağac) məlumat strukturu nədir?
92. **Binary Tree** (İkili Ağac) nədir?
93. **Binary Search Tree** (İkili Axtarış Ağacı) nədir və necə işləyir?
94. **AVL Tree** (AVL Ağacı) nədir?
95. **Red-Black Tree** (Qırmızı-Qara Ağac) nədir?
96. **B-Tree** (B-Ağacı) nədir və nə üçün istifadə olunur?
97. **Trie** (Prefiks Ağacı) nədir və necə işləyir?
98. **Heap** (Yığın) nədir və Java-da necə tətbiq olunur?
99. **Min-Heap** və **Max-Heap** arasındakı fərq nədir?
100. **PriorityQueue** ilə **Heap** arasındakı əlaqə nədir?
101. **Graph** (Qrafik) məlumat strukturu nədir?
102. **Directed Graph** (İstiqamətləndirilmiş Qrafik) ilə **Undirected Graph** (İstiqamətsiz Qrafik) arasındakı fərq nədir?
103. **Weighted Graph** (Çəkili Qrafik) nədir?
104. **Adjacency Matrix** (Qoşulma Matrisi) nədir?
105. **Adjacency List** (Qoşulma Siyahısı) nədir?
106. **Tree** ilə **Graph** arasındakı fərqlər nələrdir?
107. Java-da **TreeSet** və **TreeMap** ağac strukturları ilə necə əlaqəlidir?
108. **Depth-First Search** (Dərinlik Axtarışı) necə işləyir?
109. **Breadth-First Search** (Eninə Axtarış) necə işləyir?
110. **Dijkstra’s Algorithm** (Dijkstra Alqoritmi) qrafiklərdə necə istifadə olunur?

### Hashing və Performance
111. **Hashing** (Xəşləmə) nədir və Java-da necə işləyir?
112. **Hash Function** (Xəş Funksiyası) nədir?
113. **Hash Table** (Xəş Cədvəli) nədir və necə işləyir?
114. **HashMap**-də **hashCode()** metodu necə istifadə olunur?
115. **HashMap**-də **equals()** metodu ilə **hashCode()** arasındakı əlaqə nədir?
116. **Collision Resolution** (Toqquşma Həlli) üsulları hansılardır?
117. **Separate Chaining** (Ayrı Zəncirləmə) necə işləyir?
118. **Open Addressing** (Açıq Ünvanlama) nədir?
119. **Linear Probing** (Xətti Yoxlama) ilə **Quadratic Probing** (Kvadratik Yoxlama) arasındakı fərq nədir?
120. **Double Hashing** (İkiqat Xəşləmə) nədir?
121. **HashMap**-də **bucket** (səbət) strukturu necə işləyir?
122. **HashSet**-də daxili olaraq **HashMap** necə istifadə olunur?
123. **Load Factor** (Yükləmə Faktoru) ilə **Capacity** (Tutum) arasındakı əlaqə nədir?
124. **HashMap**-də **performance** (performans) necə optimallaşdırılır?
125. **ConcurrentHashMap**-də **lock-free** əməliyyatlar necə təmin olunur?
126. **WeakHashMap**-də **weak references** (zəif istinadlar) necə işləyir?
127. **HashMap**-də **null** açarların idarə olunması necə aparılır?
128. **Hashing**-də **collision** sayını azaltmaq üçün hansı üsullar istifadə olunur?
129. **HashMap**-də **treeification** (ağaclaşdırma) nə vaxt baş verir?
130. **ConcurrentHashMap**-də **read** və **write** əməliyyatlarının performansı necədir?

### Algorithms və Collections
131. **Sorting** (Sıralama) alqoritmləri Java-da Collections ilə necə istifadə olunur?
132. **Collections.sort()** metodu hansı alqoritmdən istifadə edir?
133. **TimSort** alqoritmi nədir və necə işləyir?
134. **Merge Sort** (Birləşmə Sıralaması) ilə **Quick Sort** (Sürətli Sıralama) arasındakı fərq nədir?
135. **Binary Search** (İkili Axtarış) Java-da necə tətbiq olunur?
136. **Arrays.binarySearch()** ilə **Collections.binarySearch()** arasındakı fərq nədir?
137. **Linear Search** (Xətti Axtarış) ilə **Binary Search** arasındakı fərq nədir?
138. **Collections.shuffle()** metodu necə işləyir?
139. **Collections.reverse()** metodu nə edir?
140. **Collections.fill()** metodu nə üçün istifadə olunur?
141. **Collections.copy()** metodu necə istifadə olunur?
142. **Collections.min()** və **Collections.max()** metodları necə işləyir?
143. **Collections.disjoint()** metodu nədir?
144. **Collections.frequency()** metodu nə üçün istifadə olunur?
145. **Stream API** ilə Collections üzərində axtarış necə aparılır?
146. **Stream API**-da **filter()** və **map()** ilə Data Structures necə işləyir?
147. **Parallel Stream** ilə Collections üzərində performans necə optimallaşdırılır?
148. **Spliterator** nədir və Collections ilə necə istifadə olunur?
149. **forEach()** ilə **enhanced for loop** (gücləndirilmiş for dövrü) arasındakı fərq nədir?
150. **Collections.nCopies()** metodu nə edir?

### Digər Mövzular
151. **Linked List** (Bağlı Siyahı) daxili strukturu necədir?
152. **Singly Linked List** (Tək Bağlı Siyahı) ilə **Doubly Linked List** (İkiqat Bağlı Siyahı) arasındakı fərq nədir?
153. **Circular Linked List** (Dairəvi Bağlı Siyahı) nədir?
154. **Skip List** (Atlama Siyahısı) nədir və necə işləyir?
155. **LinkedList**-də **tail** (quyruq) əlavə etmə performansı necədir?
156. **BitSet** nədir və nə üçün istifadə olunur?
157. **Bloom Filter** nədir və Java-da necə tətbiq olunur?
158. **Disjoint Set** (Ayrılmış Dəst) nədir və necə işləyir?
159. **Union-Find** alqoritmi nədir?
160. **Graph**-də **Topological Sort** (Topoloji Sıralama) necə həyata keçirilir?
161. **Kruskal’s Algorithm** (Kruskal Alqoritmi) nədir?
162. **Prim’s Algorithm** (Prim Alqoritmi) nədir?
163. **Bellman-Ford Algorithm** (Bellman-Ford Alqoritmi) necə işləyir?
164. **Floyd-Warshall Algorithm** (Floyd-Warshall Alqoritmi) nədir?
165. **Minimum Spanning Tree** (Minimum Örtük Ağacı) nədir?
166. **Shortest Path** (Ən Qısa Yol) problemi Java-da necə həll olunur?
167. **Trie**-də **prefix search** (prefiks axtarışı) necə aparılır?
168. **Heap**-də **heapify** (yığınlaşdırma) prosesi necə işləyir?
169. **Binary Heap** (İkili Yığın) ilə **Fibonacci Heap** (Fibonacci Yığını) arasındakı fərq nədir?
170. **B+-Tree** nədir və nə üçün istifadə olunur?
171. **Segment Tree** (Seqment Ağacı) nədir?
172. **Fenwick Tree** (Fenwick Ağacı) nədir?
173. **Interval Tree** (Interval Ağacı) nədir?
174. **Quad Tree** (Dördlük Ağac) nədir?
175. **KD-Tree** (K-Ölçülü Ağac) nədir?
176. **Graph**-də **cycle detection** (dövr aşkarlanması) necə aparılır?
177. **Union-Find** ilə **cycle detection** necə həyata keçirilir?
178. **Graph**-də **connected components** (bağlı komponentlər) necə tapılır?
179. **Strongly Connected Components** (Güclü Bağlı Komponentlər) necə aşkarlanır?
180. **Kosaraju’s Algorithm** (Kosaraju Alqoritmi) nədir?
181. **Tarjan’s Algorithm** (Tarjan Alqoritmi) nədir?
182. **Graph**-də **bipartite graph** (ikiqisimli qrafik) necə yoxlanılır?
183. **Graph Coloring** (Qrafik Boyama) problemi nədir?
184. **Maximum Flow** (Maksimum Axın) problemi necə həll olunur?
185. **Ford-Fulkerson Algorithm** (Ford-Fulkerson Alqoritmi) nədir?
186. **Edmonds-Karp Algorithm** (Edmonds-Karp Alqoritmi) nədir?
187. **HashMap**-də **consistent hashing** (sabit xəşləmə) necə tətbiq olunur?
188. **LRU Cache** (Son İstifadə Olunan Keş) Java-da necə tətbiq olunur?
189. **LFU Cache** (Ən Az İstifadə Olunan Keş) nədir?
190. **ConcurrentLinkedDeque** nədir və nə üçün istifadə olunur?
191. **Collections.emptyList()** və **Collections.singletonList()** nədir?
192. **List**-də **sublist** (alt siyahı) necə yaradılır?
193. **Map**-də **computeIfAbsent()** metodu nə edir?
194. **Map**-də **computeIfPresent()** metodu nə üçün istifadə olunur?
195. **Map**-də **merge()** metodu necə işləyir?
196. **TreeSet**-də **ceiling()** və **floor()** metodları nədir?
197. **TreeSet**-də **higher()** və **lower()** metodları nə üçün istifadə olunur?
198. **NavigableSet** və **SortedSet** arasındakı fərq nədir?
199. **NavigableMap** və **SortedMap** arasındakı fərq nədir?
200. **ConcurrentSkipListMap** nədir və necə işləyir?
201. **BitSet**-də **bit manipulation** (bit manipulyasiyası) necə aparılır?
202. **Bloom Filter**-də **false positive** (yanlış müsbət) nədir?
203. **HyperLogLog** nədir və necə istifadə olunur?
204. **Count-Min Sketch** nədir?
205. **Skip List**-də **search** (axtarış) performansı necədir?
206. **HashMap**-də **multi-threading** (çoxlu axın) mühitində istifadə zamanı hansı problemlər ola bilər?
207. **ConcurrentHashMap**-də **size()** metodunun dəqiqliyi necə təmin olunur?
208. **TreeMap**-də **balanced tree** (balanslaşdırılmış ağac) necə saxlanılır?
209. **PriorityQueue**-də **custom comparator** (xüsusi müqayisəçi) necə təyin olunur?
210. **Deque**-də **offerFirst()** və **offerLast()** metodları nə edir?
211. **Queue**-də **peek()** və **poll()** metodları arasındakı fərq nədir?
212. **LinkedList**-də **reverse** (tərsinə çevirmə) necə həyata keçirilir?
213. **ArrayList**-də **trimToSize()** metodu nə edir?
214. **HashSet**-də **add()** metodunun vaxt mürəkkəbliyi nədir?
215. **TreeSet**-də **add()** metodunun vaxt mürəkkəbliyi nədir?
216. **HashMap**-də **get()** metodunun vaxt mürəkkəbliyi nədir?
217. **ConcurrentHashMap**-də **putIfAbsent()** metodu nə edir?
218. **WeakHashMap**-də **garbage collection** (zibil toplama) necə təsir edir?
219. **IdentityHashMap**-də **reference equality** (istinad bərabərliyi) necə işləyir?
220. **EnumSet**-də **bit vector** (bit vektoru) necə istifadə olunur?
221. **Graph**-də **weighted shortest path** (çəkili ən qısa yol) necə tapılır?
222. **Tree**-də **in-order traversal** (sıralı keçid) necə həyata keçirilir?
223. **Tree**-də **pre-order traversal** (əvvəlcədən keçid) necə işləyir?
224. **Tree**-də **post-order traversal** (sondan keçid) necə tətbiq olunur?
225. **Binary Search Tree**-də **insert** (əlavə etmə) necə aparılır?
226. **Binary Search Tree**-də **delete** (silmə) necə həyata keçirilir?
227. **AVL Tree**-də **rotation** (fırlanma) mexanizmi necə işləyir?
228. **Red-Black Tree**-də **color flip** (rəng dəyişmə) necə aparılır?
229. **Heap**-də **insert** (əlavə etmə) və **delete** (silmə) vaxt mürəkkəbliyi nədir?
230. **Trie**-də **autocomplete** (avtomatik tamamlama) necə həyata keçirilir?
231. **Graph**-də **BFS** ilə **DFS** arasındakı fərq nədir?
232. **Graph**-də **minimum cut** (minimum kəsik) necə tapılır?
233. **HashMap**-də **hash collision** (xəş toqquşması) performansına necə təsir edir?
234. **ConcurrentHashMap**-də **striped locking** (zolaqlı kilidləmə) necə işləyir?
235. **PriorityQueue**-də **heap sort** (yığın sıralaması) necə tətbiq olunur?
236. **LinkedList**-də **cycle detection** (dövr aşkarlanması) necə aparılır?
237. **Floyd’s Cycle Detection Algorithm** (Floyd’un Dövr Aşkarlama Alqoritmi) nədir?
238. **ArrayList**-də **capacity** (tutum) artımı necə baş verir?
239. **HashMap**-də **threshold** (hədd) nədir?
240. **TreeMap**-də **self-balancing** (öz-özünə balanslaşdırma) necə təmin olunur?
241. **BitSet**-də **space efficiency** (yer səmərəliliyi) necə əldə olunur?
242. **Bloom Filter**-də **hash functions** (xəş funksiyaları) sayı necə seçilir?
243. **Skip List**-də **randomized levels** (təsadüfi səviyyələr) necə işləyir?
244. **Graph**-də **articulation points** (artikulyasiya nöqtələri) necə tapılır?
245. **Graph**-də **bridges** (körpülər) necə aşkarlanır?
246. **Binary Search Tree**-də **height** (hündürlük) necə hesablanır?
247. **AVL Tree**-də **balance factor** (balans faktoru) nədir?
248. **Heap**-də **sift up** və **sift down** prosesləri nədir?
249. **Trie**-də **space optimization** (yer optimallaşdırması) necə aparılır?
250. **Graph**-də **all-pairs shortest path** (bütün cütlərin ən qısa yolu) necə tapılır?
251. **Disjoint Set**-də **path compression** (yol sıxışdırması) necə işləyir?
252. **Union-Find**-də **rank** (səviyyə) necə istifadə olunur?
253. **Segment Tree**-də **range queries** (aralıq sorğuları) necə aparılır?
254. **Fenwick Tree**-də **prefix sum** (prefiks cəmi) necə hesablanır?
255. **Interval Tree**-də **overlap detection** (örtüşmə aşkarlanması) necə həyata keçirilir?
256. **Quad Tree**-də **spatial partitioning** (məkan bölüşdürülməsi) necə işləyir?
257. **KD-Tree**-də **nearest neighbor search** (ən yaxın qonşu axtarışı) necə aparılır?
258. **HashMap**-də **hash distribution** (xəş paylanması) necə optimallaşdırılır?
259. **ConcurrentHashMap**-də **CAS** (Compare-And-Swap) mexanizmi necə işləyir?
260. **PriorityQueue**-də **remove()** metodunun vaxt mürəkkəbliyi nədir?
261. **LinkedList**-də **merge** (birləşdirmə) necə həyata keçirilir?
262. **ArrayList**-də **ensureCapacity()** metodu nə edir?
263. **HashSet**-də **contains()** metodunun performansı necədir?
264. **TreeSet**-də **subSet()** metodu nə üçün istifadə olunur?
265. **Map**-də **forEach()** metodu necə işləyir?
266. **ConcurrentSkipListSet**-də **skip list** strukturu necə təmin olunur?
267. **BitSet**-də **logical operations** (məntiqi əməliyyatlar) necə aparılır?
268. **Bloom Filter**-də **space-time tradeoff** (yer-vaxt mübadiləsi) necə idarə olunur?
269. **HyperLogLog**-də **cardinality estimation** (əsaslılıq təxmini) necə aparılır?
270. **Count-Min Sketch**-də **frequency estimation** (tezlik təxmini) necə işləyir?
271. **Graph**-də **Eulerian Path** (Eyler Yolu) necə tapılır?
272. **Graph**-də **Hamiltonian Cycle** (Hamilton Dövrü) necə aşkarlanır?
273. **Tree**-də **lowest common ancestor** (ən aşağı ümumi ata) necə tapılır?
274. **Binary Search Tree**-də **successor** (növbəti) və **predecessor** (əvvəlki) necə tapılır?
275. **AVL Tree**-də **double rotation** (ikiqat fırlanma) nə vaxt baş verir?
276. **Red-Black Tree**-də **recoloring** (yenidən rəngləmə) necə aparılır?
277. **Heap**-də **merge** (birləşdirmə) necə həyata keçirilir?
278. **Trie**-də **suffix search** (sufiks axtarışı) necə aparılır?
279. **Graph**-də **max-flow min-cut theorem** (maksimum axın minimum kəsik teoremi) nədir?
280. **Disjoint Set**-də **connected components** (bağlı komponentlər) necə tapılır?
281. **Segment Tree**-də **lazy propagation** (tənbəl yayılma) necə işləyir?
282. **Fenwick Tree**-də **range update** (aralıq yeniləmə) necə həyata keçirilir?
283. **Interval Tree**-də **interval insertion** (interval əlavə etmə) necə aparılır?
284. **Quad Tree**-də **range queries** (aralıq sorğuları) necə işləyir?
285. **KD-Tree**-də **range search** (aralıq axtarışı) necə həyata keçirilir?
286. **HashMap**-də **hash table resizing** (xəş cədvəli ölçüsünün dəyişdirilməsi) nə vaxt baş verir?
287. **ConcurrentHashMap**-də **transfer** (köçürmə) prosesi necə işləyir?
288. **PriorityQueue**-də **custom objects** (xüsusi obyektlər) necə sıralanır?
289. **LinkedList**-də **partition** (bölüşdürmə) necə həyata keçirilir?
290. **ArrayList**-də **removeIf()** metodu necə işləyir?
291. **HashSet**-də **iterator** performansı necədir?
292. **TreeSet**-də **descendingSet()** metodu nə edir?
293. **Map**-də **replace()** metodu necə işləyir?
294. **ConcurrentSkipListMap**-də **navigable methods** (naviqasiya metodları) nədir?
295. **BitSet**-də **cardinality** (əsaslılıq) necə hesablanır?
296. **Bloom Filter**-də **optimal hash functions** (optimal xəş funksiyaları) necə seçilir?
297. **HyperLogLog**-də **merge** (birləşdirmə) necə aparılır?
298. **Count-Min Sketch**-də **error rate** (səhv dərəcəsi) necə idarə olunur?
299. **Graph**-də **clique** (tam qrafik) necə tapılır?
300. **Tree**-də **diameter** (diametr) necə hesablanır?

--- 

# Design Patterns Müsahibə Sualları

Bu sənəd Java, Hibernate, Spring Boot, Data Structures/Collections və Design Patterns ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Creational Patterns](#creational-patterns)
  - [Structural Patterns](#structural-patterns)
  - [Behavioral Patterns](#behavioral-patterns)
  - [Real-World Tətbiqlər](#real-world-tətbiqlər)
  - [Digər Mövzular](#digər-mövzular)

## Design Patterns

### Ümumi Suallar
1. **Design Pattern** (Dizayn Nümunəsi) nədir və niyə vacibdir?
2. **Gang of Four** (Dörd Nəfərlik Dəstə) kimlərdir və Design Patterns-ə töhfələri nədir?
3. **Creational Patterns** (Yaradıcı Nümunələr) nədir və hansılardır?
4. **Structural Patterns** (Struktur Nümunələr) nədir və hansılardır?
5. **Behavioral Patterns** (Davranış Nümunələri) nədir və hansılardır?
6. Java-da Design Patterns istifadəsinin üstünlükləri nələrdir?
7. Design Patterns ilə **anti-patterns** (əks-nümunələr) arasındakı fərq nədir?
8. **SOLID** prinsipləri Design Patterns ilə necə əlaqəlidir?
9. **Single Responsibility Principle** (Tək Məsuliyyət Prinsipi) Design Patterns-ə necə təsir edir?
10. **Open/Closed Principle** (Açıq/Qapalı Prinsip) Design Patterns-də necə tətbiq olunur?
11. **Liskov Substitution Principle** (Liskov Əvəzləmə Prinsipi) Design Patterns-ə necə təsir edir?
12. **Interface Segregation Principle** (İnterfeys Ayrılığı Prinsipi) nədir?
13. **Dependency Inversion Principle** (Asılılıq Tərsinə Çevirmə Prinsipi) Design Patterns-də necə istifadə olunur?
14. Design Patterns ilə **reusability** (təkrar istifadə) necə təmin olunur?
15. **Design Patterns** ilə **maintainability** (baxım asanlığı) necə artır?

### Creational Patterns
16. **Singleton Pattern** (Tək Nümunə Nümunəsi) nədir?
17. **Singleton Pattern**-də **thread safety** (axın təhlükəsizliyi) necə təmin olunur?
18. **Eager Initialization** (Həvəsli İlkinləşdirmə) ilə **Lazy Initialization** (Tənbəl İlkinləşdirmə) arasındakı fərq nədir?
19. **Double-Checked Locking** (İkiqat Yoxlamalı Kilidləmə) Singleton-da nə üçün istifadə olunur?
20. **Bill Pugh Singleton** nədir və üstünlükləri nələrdir?
21. **Singleton Pattern**-də **serialization** (seriyalaşdırma) problemi necə həll olunur?
22. **Singleton Pattern**-də **reflection** (refleksiya) ilə sındırılma necə qarşısı alınır?
23. **Factory Method Pattern** (Fabrik Metodu Nümunəsi) nədir?
24. **Factory Method Pattern** ilə **Abstract Factory Pattern** arasındakı fərq nədir?
25. **Abstract Factory Pattern** (Abstrakt Fabrik Nümunəsi) nədir?
26. **Factory Pattern**-də **dependency injection** (asılılıq yeridilməsi) necə istifadə olunur?
27. **Builder Pattern** (Qurucu Nümunə) nədir?
28. **Builder Pattern** ilə **Fluent Interface** (Axıcı İnterfeys) arasındakı əlaqə nədir?
29. **Builder Pattern**-də **immutable objects** (dəyişilməz obyektlər) necə yaradılır?
30. **Prototype Pattern** (Prototip Nümunəsi) nədir?
31. **Prototype Pattern**-də **deep copy** (dərin kopya) ilə **shallow copy** (səthi kopya) arasındakı fərq nədir?
32. **Object Pool Pattern** (Obyekt Hovuzu Nümunəsi) nədir?
33. **Object Pool Pattern** ilə **Singleton Pattern** arasındakı fərq nədir?
34. Java-da **Cloneable** interfeysi Prototype Pattern ilə necə istifadə olunur?
35. **Factory Pattern** Spring Framework-də necə tətbiq olunur?
36. **Builder Pattern** Java-da **StringBuilder** ilə necə əlaqəlidir?
37. **Singleton Pattern** Java-da **Runtime** sinfində necə istifadə olunur?
38. **Abstract Factory Pattern** GUI tətbiqlərində necə tətbiq olunur?
39. **Prototype Pattern** Java-da **serialization** ilə necə istifadə olunur?
40. **Creational Patterns** hansı problemləri həll edir?

### Structural Patterns
41. **Adapter Pattern** (Adapter Nümunəsi) nədir?
42. **Adapter Pattern** ilə **Bridge Pattern** arasındakı fərq nədir?
43. **Bridge Pattern** (Körpü Nümunəsi) nədir?
44. **Composite Pattern** (Kompozit Nümunəsi) nədir?
45. **Decorator Pattern** (Dekorator Nümunəsi) nədir?
46. **Facade Pattern** (Fasad Nümunəsi) nədir?
47. **Flyweight Pattern** (Yüngül Çəki Nümunəsi) nədir?
48. **Proxy Pattern** (Vəkil Nümunəsi) nədir?
49. **Adapter Pattern** Java-da **legacy code** (köhnə kod) ilə necə istifadə olunur?
50. **Bridge Pattern** JDBC-də necə tətbiq olunur?
51. **Composite Pattern** GUI komponentlərində necə istifadə olunur?
52. **Decorator Pattern** Java-da **InputStream** sinfində necə tətbiq olunur?
53. **Facade Pattern** Spring Framework-də necə istifadə olunur?
54. **Flyweight Pattern** Java-da **String Pool** ilə necə əlaqəlidir?
55. **Proxy Pattern** Spring-də **AOP** (Aspect-Oriented Programming) ilə necə tətbiq olunur?
56. **Dynamic Proxy** (Dinamik Vəkil) Java-da necə yaradılır?
57. **Adapter Pattern** ilə **Wrapper** (Sarma) arasındakı fərq nədir?
58. **Composite Pattern** ilə **Decorator Pattern** arasındakı fərq nədir?
59. **Facade Pattern** ilə **Mediator Pattern** arasındakı fərq nədir?
60. **Flyweight Pattern** ilə **Object Pool Pattern** arasındakı fərq nədir?
61. **Proxy Pattern** ilə **Decorator Pattern** arasındakı fərq nədir?
62. **Structural Patterns** hansı problemləri həll edir?
63. **Adapter Pattern** Java-da **Collections** ilə necə istifadə olunur?
64. **Bridge Pattern** ilə **abstraction** (abstraksiya) necə təmin olunur?
65. **Composite Pattern** ilə **tree structure** (ağac strukturu) necə yaradılır?
66. **Decorator Pattern** ilə **open-closed principle** (açıq-qapalı prinsip) necə tətbiq olunur?
67. **Facade Pattern** ilə **complexity** (mürəkkəblik) necə azaldılır?
68. **Flyweight Pattern** ilə **memory optimization** (yaddaş optimallaşdırması) necə təmin olunur?
69. **Proxy Pattern** ilə **lazy loading** (tənbəl yükləmə) necə həyata keçirilir?
70. **Structural Patterns** Java-da **inheritance** (mirasalma) ilə necə əlaqəlidir?

### Behavioral Patterns
71. **Chain of Responsibility Pattern** (Məsuliyyət Zənciri Nümunəsi) nədir?
72. **Command Pattern** (Əmr Nümunəsi) nədir?
73. **Interpreter Pattern** (Tərcüməçi Nümunəsi) nədir?
74. **Iterator Pattern** (Təkrarlayıcı Nümunəsi) nədir?
75. **Mediator Pattern** (Vasitəçi Nümunəsi) nədir?
76. **Memento Pattern** (Xatirə Nümunəsi) nədir?
77. **Observer Pattern** (Müşahidəçi Nümunəsi) nədir?
78. **State Pattern** (Vəziyyət Nümunəsi) nədir?
79. **Strategy Pattern** (Strategiya Nümunəsi) nədir?
80. **Template Method Pattern** (Şablon Metod Nümunəsi) nədir?
81. **Visitor Pattern** (Ziyarətçi Nümunəsi) nədir?
82. **Chain of Responsibility Pattern** Java-da **logging** (qeydiyyat) sistemlərində necə tətbiq olunur?
83. **Command Pattern** ilə **undo/redo** (geri al/təkrar et) funksionallığı necə həyata keçirilir?
84. **Interpreter Pattern** SQL parser-lərdə necə istifadə olunur?
85. **Iterator Pattern** Java-da **Collections Framework** ilə necə tətbiq olunur?
86. **Mediator Pattern** ilə **loose coupling** (zəif bağlılıq) necə təmin olunur?
87. **Memento Pattern** ilə **serialization** (seriyalaşdırma) arasındakı fərq nədir?
88. **Observer Pattern** Java-da **event listeners** (hadisə dinləyiciləri) ilə necə tətbiq olunur?
89. **State Pattern** ilə **finite state machine** (sonlu vəziyyət maşını) necə yaradılır?
90. **Strategy Pattern** ilə **open-closed principle** (açıq-qapalı prinsip) necə tətbiq olunur?
91. **Template Method Pattern** Java-da **Abstract Class** ilə necə istifadə olunur?
92. **Visitor Pattern** ilə **double dispatch** (ikiqat göndəriş) necə həyata keçirilir?
93. **Chain of Responsibility Pattern** ilə **Filter Chain** (Süzgəc Zənciri) necə əlaqəlidir?
94. **Command Pattern** ilə **functional programming** (funksional proqramlaşdırma) arasındakı əlaqə nədir?
95. **Interpreter Pattern** ilə **Composite Pattern** arasındakı fərq nədir?
96. **Iterator Pattern** ilə **forEach** metodu arasındakı fərq nədir?
97. **Mediator Pattern** ilə **Facade Pattern** arasındakı fərq nədir?
98. **Memento Pattern** ilə **Command Pattern** arasındakı fərq nədir?
99. **Observer Pattern** ilə **Publish-Subscribe** (Nəşr-Abunə) modeli arasındakı fərq nədir?
100. **State Pattern** ilə **Strategy Pattern** arasındakı fərq nədir?
101. **Template Method Pattern** ilə **Strategy Pattern** arasındakı fərq nədir?
102. **Visitor Pattern** ilə **type safety** (tip təhlükəsizliyi) necə təmin olunur?
103. **Behavioral Patterns** hansı problemləri həll edir?
104. **Observer Pattern** Spring-də **ApplicationEvent** ilə necə tətbiq olunur?
105. **Strategy Pattern** Java-da **Comparator** ilə necə istifadə olunur?
106. **Template Method Pattern** Java-da **Servlet** sinfində necə tətbiq olunur?
107. **Chain of Responsibility Pattern** Spring Security-də necə istifadə olunur?
108. **Command Pattern** Java-da **Runnable** ilə necə əlaqəlidir?
109. **Mediator Pattern** GUI tətbiqlərində necə tətbiq olunur?
110. **Memento Pattern** Java-da **serialization** ilə necə istifadə olunur?

### Real-World Tətbiqlər
111. **Singleton Pattern** real dünya tətbiqlərində hansı hallarda istifadə olunur?
112. **Factory Method Pattern** Spring-də **Bean Factory** ilə necə tətbiq olunur?
113. **Abstract Factory Pattern** Java-da **JDBC** ilə necə istifadə olunur?
114. **Builder Pattern** Java-da **StringBuilder** və **HttpClient** ilə necə tətbiq olunur?
115. **Prototype Pattern** Java-da **clone()** metodu ilə necə istifadə olunur?
116. **Adapter Pattern** Java-da **legacy systems** (köhnə sistemlər) ilə necə inteqrasiya olunur?
117. **Bridge Pattern** Java-da **JDBC Driver** ilə necə tətbiq olunur?
118. **Composite Pattern** Java-da **Swing** komponentlərində necə istifadə olunur?
119. **Decorator Pattern** Java-da **IO Streams** ilə necə tətbiq olunur?
120. **Facade Pattern** Java-da **JDBC API** ilə necə istifadə olunur?
121. **Flyweight Pattern** Java-da **String** sinfində necə tətbiq olunur?
122. **Proxy Pattern** Hibernate-də **lazy loading** ilə necə istifadə olunur?
123. **Chain of Responsibility Pattern** Java-da **Servlet Filters** ilə necə tətbiq olunur?
124. **Command Pattern** Java-da **Swing Action** ilə necə istifadə olunur?
125. **Interpreter Pattern** Java-da **regular expressions** (requlyar ifadələr) ilə necə tətbiq olunur?
126. **Iterator Pattern** Java-da **Collections** ilə necə istifadə olunur?
127. **Mediator Pattern** Java-da **Spring MVC** ilə necə tətbiq olunur?
128. **Memento Pattern** Java-da **undo/redo** ilə necə istifadə olunur?
129. **Observer Pattern** Java-da **JavaFX** ilə necə tətbiq olunur?
130. **State Pattern** Java-da **workflow systems** (iş axını sistemləri) ilə necə istifadə olunur?
131. **Strategy Pattern** Java-da **sorting algorithms** (sıralama alqoritmləri) ilə necə tətbiq olunur?
132. **Template Method Pattern** Java-da **HttpServlet** ilə necə istifadə olunur?
133. **Visitor Pattern** Java-da **compiler design** (kompilyator dizaynı) ilə necə tətbiq olunur?
134. **Singleton Pattern** Spring-də **singleton scope** ilə necə əlaqəlidir?
135. **Factory Pattern** Spring-də **ApplicationContext** ilə necə tətbiq olunur?
136. **Builder Pattern** Spring-də **RestTemplate** ilə necə istifadə olunur?
137. **Adapter Pattern** Spring-də **legacy code** inteqrasiyasında necə tətbiq olunur?
138. **Decorator Pattern** Spring-də **AOP** ilə necə istifadə olunur?
139. **Facade Pattern** Spring-də **JPA Repository** ilə necə tətbiq olunur?
140. **Proxy Pattern** Spring-də **transaction management** (tranzaksiya idarəetmə) ilə necə istifadə olunur?
141. **Chain of Responsibility Pattern** Spring Security-də **filter chain** ilə necə tətbiq olunur?
142. **Command Pattern** Spring-də **event handling** (hadisə idarəetmə) ilə necə istifadə olunur?
143. **Observer Pattern** Spring-də **ApplicationListener** ilə necə tətbiq olunur?
144. **Strategy Pattern** Spring-də **validation** (doğrulama) ilə necə istifadə olunur?
145. **Template Method Pattern** Spring-də **JdbcTemplate** ilə necə tətbiq olunur?

### Digər Mövzular
146. **Null Object Pattern** (Boş Obyekt Nümunəsi) nədir?
147. **Repository Pattern** (Anbar Nümunəsi) nədir və Java-da necə tətbiq olunur?
148. **Service Locator Pattern** (Xidmət Tapıcı Nümunəsi) nədir?
149. **Dependency Injection Pattern** (Asılılıq Yeridilmə Nümunəsi) nədir?
150. **Module Pattern** (Modul Nümunəsi) Java-da necə istifadə olunur?
151. **MVC Pattern** (Model-View-Controller Nümunəsi) nədir?
152. **DAO Pattern** (Data Access Object Nümunəsi) nədir?
153. **Unit of Work Pattern** (İş Vahidi Nümunəsi) nədir?
154. **Specification Pattern** (Spesifikasiya Nümunəsi) nədir?
155. **Circuit Breaker Pattern** (Dövrə Qoruyucusu Nümunəsi) nədir?
156. **Retry Pattern** (Təkrar Sınaq Nümunəsi) nədir?
157. **Event Sourcing Pattern** (Hadisə Mənbəyi Nümunəsi) nədir?
158. **CQRS Pattern** (Command Query Responsibility Segregation Nümunəsi) nədir?
159. **Saga Pattern** (Saqa Nümunəsi) nədir?
160. **Strangler Fig Pattern** (Böcək İnciri Nümunəsi) nədir?
161. **Null Object Pattern** Java-da **Optional** ilə necə əlaqəlidir?
162. **Repository Pattern** Spring Data ilə necə tətbiq olunur?
163. **Service Locator Pattern** ilə **Dependency Injection** arasındakı fərq nədir?
164. **MVC Pattern** Spring MVC-də necə istifadə olunur?
165. **DAO Pattern** Hibernate ilə necə tətbiq olunur?
166. **Unit of Work Pattern** JPA ilə necə istifadə olunur?
167. **Specification Pattern** Spring Data Specifications ilə necə tətbiq olunur?
168. **Circuit Breaker Pattern** Spring Cloud ilə necə istifadə olunur?
169. **Retry Pattern** Spring Retry ilə necə tətbiq olunur?
170. **Event Sourcing Pattern** Spring Boot ilə necə həyata keçirilir?
171. **CQRS Pattern** Spring Boot ilə necə tətbiq olunur?
172. **Saga Pattern** microservices arxitekturasında necə istifadə olunur?
173. **Strangler Fig Pattern** köhnə sistemləri modernləşdirmək üçün necə tətbiq olunur?
174. **Null Object Pattern** ilə **default behavior** (standart davranış) necə təmin olunur?
175. **Repository Pattern** ilə **DAO Pattern** arasındakı fərq nədir?
176. **Module Pattern** Java 9+ modullarında necə tətbiq olunur?
177. **Dependency Injection Pattern** Spring-də necə həyata keçirilir?
178. **Circuit Breaker Pattern** ilə **Retry Pattern** arasındakı fərq nədir?
179. **Event Sourcing Pattern** ilə **CQRS Pattern** arasındakı əlaqə nədir?
180. **Saga Pattern** ilə **Orchestration** və **Choreography** arasındakı fərq nədir?
181. **Abstract Factory Pattern** ilə **Dependency Injection** necə inteqrasiya olunur?
182. **Builder Pattern** ilə **immutable objects** (dəyişilməz obyektlər) yaratmağın üstünlükləri nələrdir?
183. **Decorator Pattern** ilə **AOP** (Aspect-Oriented Programming) arasındakı əlaqə nədir?
184. **Proxy Pattern** ilə **dynamic proxies** Java-da necə yaradılır?
185. **Observer Pattern** ilə **reactive programming** (reaktiv proqramlaşdırma) arasındakı əlaqə nədir?
186. **Strategy Pattern** ilə **functional interfaces** (funksional interfeyslər) necə istifadə olunur?
187. **Template Method Pattern** ilə **inheritance** (mirasalma) necə əlaqəlidir?
188. **Visitor Pattern** ilə **type checking** (tip yoxlaması) necə idarə olunur?
189. **Chain of Responsibility Pattern** ilə **pipeline architecture** (boru xətti arxitekturası) necə əlaqəlidir?
190. **Command Pattern** ilə **event-driven architecture** (hadisə yönümlü arxitektura) necə inteqrasiya olunur?
191. **Mediator Pattern** ilə **microservices** arxitekturasında necə istifadə olunur?
192. **Memento Pattern** ilə **state management** (vəziyyət idarəetmə) necə həyata keçirilir?
193. **State Pattern** ilə **workflow automation** (iş axını avtomatlaşdırması) necə tətbiq olunur?
194. **Singleton Pattern** ilə **thread pool** (axın hovuzu) necə əlaqəlidir?
195. **Factory Pattern** ilə **service creation** (xidmət yaratma) necə optimallaşdırılır?
196. **Adapter Pattern** ilə **API integration** (API inteqrasiyası) necə həyata keçirilir?
197. **Composite Pattern** ilə **hierarchical data** (iyerarxik məlumat) necə idarə olunur?
198. **Facade Pattern** ilə **microservices** arxitekturasında necə istifadə olunur?
199. **Flyweight Pattern** ilə **caching** (keşləmə) necə əlaqəlidir?
200. **Proxy Pattern** ilə **remote objects** (uzaq obyektlər) necə idarə olunur?
201. **Null Object Pattern** ilə **exception handling** (istisna idarəetmə) necə optimallaşdırılır?
202. **Repository Pattern** ilə **domain-driven design** (domen yönümlü dizayn) necə tətbiq olunur?
203. **Service Locator Pattern** Spring-də necə istifadə olunur?
204. **MVC Pattern** ilə **separation of concerns** (vəzifələrin ayrılması) necə təmin olunur?
205. **DAO Pattern** ilə **data persistence** (məlumat davamlılığı) necə həyata keçirilir?
206. **Unit of Work Pattern** ilə **transaction management** (tranzaksiya idarəetmə) necə inteqrasiya olunur?
207. **Specification Pattern** ilə **business rules** (biznes qaydaları) necə idarə olunur?
208. **Circuit Breaker Pattern** ilə **resilience** (dayanıqlılıq) necə təmin olunur?
209. **Retry Pattern** ilə **fault tolerance** (səhvə dözümlülük) necə artır?
210. **Event Sourcing Pattern** ilə **audit logging** (audit qeydiyyatı) necə həyata keçirilir?
211. **CQRS Pattern** ilə **scalability** (miqyaslılıq) necə təmin olunur?
212. **Saga Pattern** ilə **distributed transactions** (paylanmış tranzaksiyalar) necə idarə olunur?
213. **Strangler Fig Pattern** ilə **legacy system migration** (köhnə sistem miqrasiyası) necə aparılır?
214. **Null Object Pattern** ilə **default values** (standart dəyərlər) necə təyin olunur?
215. **Repository Pattern** ilə **unit testing** (vahid testlər) necə asanlaşdırılır?
216. **Service Locator Pattern** ilə **dependency management** (asılılıq idarəetmə) necə həyata keçirilir?
217. **MVC Pattern** ilə **REST API** dizaynı necə inteqrasiya olunur?
218. **DAO Pattern** ilə **ORM** (Object-Relational Mapping) necə əlaqəlidir?
219. **Unit of Work Pattern** ilə **batch processing** (toplu emal) necə optimallaşdırılır?
220. **Specification Pattern** ilə **dynamic queries** (dinamik sorğular) necə yaradılır?
221. **Circuit Breaker Pattern** ilə **microservices resilience** (mikroservis dayanıqlılığı) necə təmin olunur?
222. **Retry Pattern** ilə **exponential backoff** (eksponensial geri çəkilmə) necə tətbiq olunur?
223. **Event Sourcing Pattern** ilə **event replay** (hadisə təkrar oynatma) necə həyata keçirilir?
224. **CQRS Pattern** ilə **read/write separation** (oxuma/yazma ayrılığı) necə təmin olunur?
225. **Saga Pattern** ilə **compensation transactions** (kompensasiya tranzaksiyaları) necə idarə olunur?
226. **Strangler Fig Pattern** ilə **incremental migration** (addım-addım miqrasiya) necə aparılır?
227. **Null Object Pattern** ilə **code readability** (kod oxunaqlılığı) necə artır?
228. **Repository Pattern** ilə **data abstraction** (məlumat abstraksiyası) necə təmin olunur?
229. **Service Locator Pattern** ilə **testability** (test oluna bilmə) necə təsirə məruz qalır?
230. **MVC Pattern** ilə **front-end frameworks** (ön tərəf çərçivələri) necə inteqrasiya olunur?
231. **DAO Pattern** ilə **database independence** (verilənlər bazasından asılı olmama) necə təmin olunur?
232. **Unit of Work Pattern** ilə **consistency** (tutarlılıq) necə təmin olunur?
233. **Specification Pattern** ilə **business logic** (biznes məntiqi) necə modullaşdırılır?
234. **Circuit Breaker Pattern** ilə **fallback mechanisms** (ehtiyat mexanizmlər) necə tətbiq olunur?
235. **Retry Pattern** ilə **timeout handling** (vaxtaşımı idarəetmə) necə həyata keçirilir?
236. **Event Sourcing Pattern** ilə **event versioning** (hadisə versiyalaşdırma) necə idarə olunur?
237. **CQRS Pattern** ilə **eventual consistency** (nəticədə tutarlılıq) necə təmin olunur?
238. **Saga Pattern** ilə **choreography** (xoreoqrafiya) necə tətbiq olunur?
239. **Strangler Fig Pattern** ilə **risk management** (risk idarəetmə) necə aparılır?
240. **Null Object Pattern** ilə **null checks** (boş yoxlamalar) necə azaldılır?
241. **Repository Pattern** ilə **Spring Data** necə inteqrasiya olunur?
242. **Service Locator Pattern** ilə **Spring ApplicationContext** necə əlaqəlidir?
243. **MVC Pattern** ilə **microservices** arxitekturasında necə istifadə olunur?
244. **DAO Pattern** ilə **JPA** necə tətbiq olunur?
245. **Unit of Work Pattern** ilə **Hibernate Session** necə əlaqəlidir?
246. **Specification Pattern** ilə **Criteria API** necə istifadə olunur?
247. **Circuit Breaker Pattern** ilə **Resilience4j** necə tətbiq olunur?
248. **Retry Pattern** ilə **Spring Cloud** necə inteqrasiya olunur?
249. **Event Sourcing Pattern** ilə **Kafka** necə istifadə olunur?
250. **CQRS Pattern** ilə **event-driven architecture** (hadisə yönümlü arxitektura) necə inteqrasiya olunur?
251. **Saga Pattern** ilə **Spring Cloud Stream** necə tətbiq olunur?
252. **Strangler Fig Pattern** ilə **monolith-to-microservices** (monolitdən mikroservislərə) keçid necə aparılır?
253. **Null Object Pattern** ilə **Optional** sinfi necə əlaqəlidir?
254. **Repository Pattern** ilə **clean architecture** (təmiz arxitektura) necə tətbiq olunur?
255. **Service Locator Pattern** ilə **inversion of control** (idarəetmənin tərsinə çevrilməsi) necə əlaqəlidir?
256. **MVC Pattern** ilə **RESTful services** (REST xidmətləri) necə inteqrasiya olunur?
257. **DAO Pattern** ilə **Spring JDBC** necə tətbiq olunur?
258. **Unit of Work Pattern** ilə **Spring Transaction Management** necə inteqrasiya olunur?
259. **Specification Pattern** ilə **Spring Data JPA** necə istifadə olunur?
260. **Circuit Breaker Pattern** ilə **Hystrix** necə tətbiq olunur?
261. **Retry Pattern** ilə **resilience patterns** (dayanıqlılıq nümunələri) necə inteqrasiya olunur?
262. **Event Sourcing Pattern** ilə **event store** (hadisə anbarı) necə idarə olunur?
263. **CQRS Pattern** ilə **read model** (oxuma modeli) necə yaradılır?
264. **Saga Pattern** ilə **orchestration** (orkestrasiya) necə tətbiq olunur?
265. **Strangler Fig Pattern** ilə **API versioning** (API versiyalaşdırma) necə idarə olunur?
266. **Null Object Pattern** ilə **defensive programming** (müdafiə proqramlaşdırması) necə tətbiq olunur?
267. **Repository Pattern** ilə **hexagonal architecture** (altıbucaqlı arxitektura) necə inteqrasiya olunur?
268. **Service Locator Pattern** ilə **Spring Boot** necə tətbiq olunur?
269. **MVC Pattern** ilə **GraphQL** necə inteqrasiya olunur?
270. **DAO Pattern** ilə **NoSQL** verilənlər bazaları necə tətbiq olunur?
271. **Unit of Work Pattern** ilə **MongoDB** necə istifadə olunur?
272. **Specification Pattern** ilə **dynamic filtering** (dinamik süzgəcləmə) necə həyata keçirilir?
273. **Circuit Breaker Pattern** ilə **microservices monitoring** (mikroservis monitorinqi) necə inteqrasiya olunur?
274. **Retry Pattern** ilə **circuit breaker** necə birləşdirilir?
275. **Event Sourcing Pattern** ilə **event versioning** (hadisə versiyalaşdırma) necə idarə olunur?
276. **CQRS Pattern** ilə **event sourcing** necə birləşdirilir?
277. **Saga Pattern** ilə **event-driven microservices** (hadisə yönümlü mikroservislər) necə tətbiq olunur?
278. **Strangler Fig Pattern** ilə **cloud migration** (bulud miqrasiyası) necə aparılır?
279. **Null Object Pattern** ilə **API responses** (API cavabları) necə optimallaşdırılır?
280. **Repository Pattern** ilə **test-driven development** (test yönümlü inkişaf) necə tətbiq olunur?
281. **Service Locator Pattern** ilə **Spring DI** (Dependency Injection) necə müqayisə edilir?
282. **MVC Pattern** ilə **reactive programming** (reaktiv proqramlaşdırma) necə inteqrasiya olunur?
283. **DAO Pattern** ilə **Spring Data MongoDB** necə tətbiq olunur?
284. **Unit of Work Pattern** ilə **Spring Data JPA** necə inteqrasiya olunur?
285. **Specification Pattern** ilə **Spring Boot** necə istifadə olunur?
286. **Circuit Breaker Pattern** ilə **Spring Cloud Gateway** necə tətbiq olunur?
287. **Retry Pattern** ilə **Spring WebFlux** necə inteqrasiya olunur?
288. **Event Sourcing Pattern** ilə **Spring Cloud Stream** necə tətbiq olunur?
289. **CQRS Pattern** ilə **Spring Data Redis** necə istifadə olunur?
290. **Saga Pattern** ilə **Spring Cloud Data Flow** necə tətbiq olunur?
291. **Strangler Fig Pattern** ilə **Kubernetes** necə inteqrasiya olunur?
292. **Null Object Pattern** ilə **REST API error handling** (REST API səhv idarəetmə) necə optimallaşdırılır?
293. **Repository Pattern** ilə **microservices** arxitekturasında necə istifadə olunur?
294. **Service Locator Pattern** ilə **Spring Cloud** necə tətbiq olunur?
295. **MVC Pattern** ilə **Spring WebFlux** necə inteqrasiya olunur?
296. **DAO Pattern** ilə **Spring Data Cassandra** necə tətbiq olunur?
297. **Unit of Work Pattern** ilə **Spring Data Neo4j** necə istifadə olunur?
298. **Specification Pattern** ilə **Spring Security** necə inteqrasiya olunur?
299. **Circuit Breaker Pattern** ilə **Spring Boot Actuator** necə tətbiq olunur?
300. **Retry Pattern** ilə **Spring Batch** necə inteqrasiya olunur?

---

# Algorithms Müsahibə Sualları

Bu sənəd Java, Hibernate, Spring Boot, Data Structures/Collections, Design Patterns və Algorithms ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Sorting Algorithms](#sorting-algorithms)
  - [Searching Algorithms](#searching-algorithms)
  - [Tree Algorithms](#tree-algorithms)
  - [Graph Algorithms](#graph-algorithms)
  - [Dynamic Programming](#dynamic-programming)
  - [Greedy Algorithms](#greedy-algorithms)
  - [Divide and Conquer](#divide-and-conquer)
  - [Hashing Algorithms](#hashing-algorithms)
  - [Other Algorithms](#other-algorithms)

## Algorithms

### Ümumi Suallar
1. **Algorithm** (Alqoritm) nədir və niyə vacibdir?
2. **Time Complexity** (Vaxt Mürəkkəbliyi) nədir və necə hesablanır?
3. **Space Complexity** (Yer Mürəkkəbliyi) nədir və necə ölçülür?
4. **Big-O Notation** (Böyük-O İşarəsi) nədir?
5. **Big-Theta** və **Big-Omega** notasyonları nədir?
6. **Asymptotic Analysis** (Asimptotik Təhlil) nədir?
7. Alqoritmlərdə **worst-case** (ən pis hal) ilə **average-case** (orta hal) arasındakı fərq nədir?
8. **Iterative** (Təkrarlayan) və **Recursive** (Rekursiv) alqoritmlər arasındakı fərq nədir?
9. **Divide and Conquer** (Böl və Hökm Et) strategiyası nədir?
10. **Greedy Algorithm** (Acgöz Alqoritm) nədir?
11. **Dynamic Programming** (Dinamik Proqramlaşdırma) nədir?
12. Alqoritmlərdə **backtracking** (geri dönüş) nədir?
13. **Brute Force** (Kobud Qüvvə) alqoritmləri nədir?
14. Alqoritmlərdə **optimization** (optimallaşdırma) necə aparılır?
15. Java-da alqoritmlərin performansını ölçmək üçün hansı alətlər istifadə olunur?

### Sorting Algorithms
16. **Bubble Sort** (Köpüklü Sıralama) nədir?
17. **Selection Sort** (Seçim Sıralaması) nədir?
18. **Insertion Sort** (Daxil Etmə Sıralaması) nədir?
19. **Merge Sort** (Birləşmə Sıralaması) nədir?
20. **Quick Sort** (Sürətli Sıralama) nədir?
21. **Heap Sort** (Yığın Sıralaması) nədir?
22. **TimSort** nədir və Java-da necə istifadə olunur?
23. **Radix Sort** (Radiks Sıralaması) nədir?
24. **Bucket Sort** (Səbət Sıralaması) nədir?
25. **Counting Sort** (Sayma Sıralaması) nədir?
26. **Bubble Sort** ilə **Selection Sort** arasındakı fərq nədir?
27. **Merge Sort** ilə **Quick Sort** arasındakı fərq nədir?
28. **Quick Sort**-da **pivot** (dayaq nöqtəsi) seçimi necə təsir edir?
29. **Heap Sort** ilə **Merge Sort** arasındakı performans fərqi nədir?
30. **TimSort**-un **Merge Sort** və **Insertion Sort** ilə əlaqəsi nədir?
31. **Radix Sort** hansı hallarda effektivdir?
32. **Bucket Sort** ilə **Counting Sort** arasındakı fərq nədir?
33. **Stable Sorting** (Sabit Sıralama) ilə **Unstable Sorting** (Qeyri-sabit Sıralama) nədir?
34. Java-da **Collections.sort()** hansı alqoritmdən istifadə edir?
35. **Arrays.sort()** ilə **Collections.sort()** arasındakı fərq nədir?
36. **In-place Sorting** (Yerində Sıralama) nədir?
37. **External Sorting** (Xarici Sıralama) nədir?
38. **Quick Sort**-da **randomized pivot** (təsadüfi dayaq) necə istifadə olunur?
39. **Merge Sort**-da **divide** (bölmə) və **merge** (birləşdirmə) necə işləyir?
40. **Heap Sort**-da **heapify** (yığınlaşdırma) prosesi nədir?

### Searching Algorithms
41. **Linear Search** (Xətti Axtarış) nədir?
42. **Binary Search** (İkili Axtarış) nədir?
43. **Jump Search** (Sıçrayış Axtarışı) nədir?
44. **Interpolation Search** (İnterpolyasiya Axtarışı) nədir?
45. **Exponential Search** (Eksponensial Axtarış) nədir?
46. **Linear Search** ilə **Binary Search** arasındakı fərq nədir?
47. **Binary Search** hansı hallarda effektivdir?
48. **Jump Search** ilə **Binary Search** arasındakı fərq nədir?
49. **Interpolation Search** necə işləyir və hansı hallarda üstünlük təşkil edir?
50. **Exponential Search** ilə **Binary Search** arasındakı fərq nədir?
51. Java-da **Arrays.binarySearch()** necə istifadə olunur?
52. **Collections.binarySearch()** necə işləyir?
53. **Binary Search**-da **iterative** və **recursive** yanaşmalar arasındakı fərq nədir?
54. **Ternary Search** (Üçlü Axtarış) nədir?
55. **Search Algorithm**-larda **time complexity** (vaxt mürəkkəbliyi) necə hesablanır?
56. **Binary Search Tree** ilə **Binary Search** arasındakı fərq nədir?
57. **Hash-based Search** (Xəş əsaslı axtarış) necə işləyir?
58. **Bloom Filter** axtarışda necə istifadə olunur?
59. **Trie**-də **prefix search** (prefiks axtarışı) necə həyata keçirilir?
60. **Graph**-də **search** alqoritmləri hansılardır?

### Tree Algorithms
61. **Binary Tree Traversal** (İkili Ağac Keçidi) növləri hansılardır?
62. **In-order Traversal** (Sıralı Keçid) nədir?
63. **Pre-order Traversal** (Əvvəlcədən Keçid) nədir?
64. **Post-order Traversal** (Sondan Keçid) nədir?
65. **Level-order Traversal** (Səviyyəli Keçid) nədir?
66. **Binary Search Tree** (İkili Axtarış Ağacı) əməliyyatları hansılardır?
67. **BST Insert** (İkili Axtarış Ağacına Əlavə Etmə) necə işləyir?
68. **BST Delete** (İkili Axtarış Ağacından Silmə) necə həyata keçirilir?
69. **BST Search** (İkili Axtarış Ağacında Axtarış) necə aparılır?
70. **AVL Tree** balanslaşdırma necə işləyir?
71. **Red-Black Tree** əməliyyatları hansılardır?
72. **AVL Tree** ilə **Red-Black Tree** arasındakı fərq nədir?
73. **B-Tree** nədir və nə üçün istifadə olunur?
74. **B+-Tree** nədir və verilənlər bazalarında necə tətbiq olunur?
75. **Trie** (Prefiks Ağacı) nədir və necə işləyir?
76. **Heap**-də **insert** (əlavə etmə) və **delete** (silmə) necə aparılır?
77. **Min-Heap** ilə **Max-Heap** arasındakı fərq nədir?
78. **Binary Tree**-də **height** (hündürlük) necə hesablanır?
79. **Binary Tree**-də **diameter** (diametr) necə tapılır?
80. **Lowest Common Ancestor** (Ən Aşağı Ümumi Ata) necə hesablanır?
81. **Binary Tree**-də **balanced tree** (balanslaşdırılmış ağac) necə yoxlanılır?
82. **AVL Tree**-də **rotation** (fırlanma) növləri hansılardır?
83. **Red-Black Tree**-də **color flip** (rəng dəyişmə) necə işləyir?
84. **Trie**-də **autocomplete** (avtomatik tamamlama) necə həyata keçirilir?
85. **Segment Tree** (Seqment Ağacı) nədir?
86. **Fenwick Tree** (Fenwick Ağacı) nədir?
87. **Interval Tree** (Interval Ağacı) nədir?
88. **Quad Tree** (Dördlük Ağac) nədir?
89. **KD-Tree** (K-Ölçülü Ağac) nədir?
90. **Segment Tree**-də **range queries** (aralıq sorğuları) necə aparılır?

### Graph Algorithms
91. **Depth-First Search** (Dərinlik Axtarışı) nədir?
92. **Breadth-First Search** (Eninə Axtarış) nədir?
93. **Dijkstra’s Algorithm** (Dijkstra Alqoritmi) nədir?
94. **Bellman-Ford Algorithm** (Bellman-Ford Alqoritmi) nədir?
95. **Floyd-Warshall Algorithm** (Floyd-Warshall Alqoritmi) nədir?
96. **Kruskal’s Algorithm** (Kruskal Alqoritmi) nədir?
97. **Prim’s Algorithm** (Prim Alqoritmi) nədir?
98. **Topological Sort** (Topoloji Sıralama) nədir?
99. **Kosaraju’s Algorithm** (Kosaraju Alqoritmi) nədir?
100. **Tarjan’s Algorithm** (Tarjan Alqoritmi) nədir?
101. **DFS** ilə **BFS** arasındakı fərq nədir?
102. **Dijkstra’s Algorithm** ilə **A* Algorithm** (A Ulduz Alqoritmi) arasındakı fərq nədir?
103. **Minimum Spanning Tree** (Minimum Örtük Ağacı) nədir?
104. **Ford-Fulkerson Algorithm** (Ford-Fulkerson Alqoritmi) nədir?
105. **Edmonds-Karp Algorithm** (Edmonds-Karp Alqoritmi) nədir?
106. **Graph**-də **cycle detection** (dövr aşkarlanması) necə aparılır?
107. **Floyd’s Cycle Detection Algorithm** (Floyd’un Dövr Aşkarlama Alqoritmi) nədir?
108. **Union-Find** alqoritmi nədir?
109. **Graph**-də **connected components** (bağlı komponentlər) necə tapılır?
110. **Strongly Connected Components** (Güclü Bağlı Komponentlər) necə aşkarlanır?
111. **Graph**-də **bipartite graph** (ikiqisimli qrafik) necə yoxlanılır?
112. **Graph Coloring** (Qrafik Boyama) nədir?
113. **Maximum Flow** (Maksimum Axın) problemi necə həll olunur?
114. **Max-Flow Min-Cut Theorem** (Maksimum Axın Minimum Kəsik Teoremi) nədir?
115. **Articulation Points** (Artikulyasiya Nöqtələri) necə tapılır?
116. **Bridges** (Körpülər) qrafikdə necə aşkarlanır?
117. **Eulerian Path** (Eyler Yolu) necə tapılır?
118. **Hamiltonian Cycle** (Hamilton Dövrü) necə aşkarlanır?
119. **Weighted Shortest Path** (Çəkili Ən Qısa Yol) necə tapılır?
120. **All-Pairs Shortest Path** (Bütün Cütlərin Ən Qısa Yolu) necə hesablanır?

### Dynamic Programming
121. **Dynamic Programming** (Dinamik Proqramlaşdırma) nədir?
122. **Memoization** (Yadda Saxlama) ilə **Tabulation** (Cədvəlləşdirmə) arasındakı fərq nədir?
123. **Fibonacci Sequence** (Fibonacci Sırası) dinamik proqramlaşdırma ilə necə hesablanır?
124. **Knapsack Problem** (Çanta Problemi) nədir?
125. **0/1 Knapsack** ilə **Fractional Knapsack** arasındakı fərq nədir?
126. **Longest Common Subsequence** (Ən Uzun Ümumi Altsıra) nədir?
127. **Longest Increasing Subsequence** (Ən Uzun Artan Altsıra) necə tapılır?
128. **Edit Distance** (Redaktə Məsafəsi) nədir?
129. **Matrix Chain Multiplication** (Matris Zəncir Çoxalması) nədir?
130. **Subset Sum Problem** (Alt Cəm Problemi) nədir?
131. **Coin Change Problem** (Sikkə Dəyişmə Problemi) necə həll olunur?
132. **Longest Palindromic Substring** (Ən Uzun Palindromik Altsətir) necə tapılır?
133. **Dynamic Programming** ilə **Greedy Algorithm** arasındakı fərq nədir?
134. **Optimal Substructure** (Optimal Altstruktur) nədir?
135. **Overlapping Subproblems** (Örtüşən Altproblemlər) nədir?
136. **Rod Cutting Problem** (Çubuq Kəsmə Problemi) nədir?
137. **Word Break Problem** (Söz Ayırma Problemi) necə həll olunur?
138. **Partition Problem** (Bölüşdürmə Problemi) nədir?
139. **Longest Path in Matrix** (Matrisdə Ən Uzun Yol) necə tapılır?
140. **Dynamic Programming**-də **state transition** (vəziyyət keçidi) necə təyin olunur?

### Greedy Algorithms
141. **Greedy Algorithm** (Acgöz Alqoritm) nədir?
142. **Huffman Coding** (Huffman Kodlaşdırması) nədir?
143. **Kruskal’s Algorithm** ilə **Greedy** yanaşma necə tətbiq olunur?
144. **Prim’s Algorithm** ilə **Greedy** yanaşma necə istifadə olunur?
145. **Fractional Knapsack Problem** (Kəsir Çanta Problemi) necə həll olunur?
146. **Activity Selection Problem** (Fəaliyyət Seçimi Problemi) nədir?
147. **Job Scheduling Problem** (İş Planlaşdırma Problemi) nədir?
148. **Greedy Algorithm**-də **optimal choice** (optimal seçim) necə təmin olunur?
149. **Dijkstra’s Algorithm** ilə **Greedy** yanaşma necə əlaqəlidir?
150. **Greedy Algorithm** hansı hallarda uğursuz olur?
151. **Huffman Coding**-də **prefix codes** (prefiks kodları) necə yaradılır?
152. **Activity Selection Problem**-də **greedy choice property** (acgöz seçim xüsusiyyəti) nədir?
153. **Minimum Coin Change** (Minimum Sikkə Dəyişmə) problemi Greedy ilə necə həll olunur?
154. **Greedy Algorithm**-də **local optimum** (lokal optimal) ilə **global optimum** (qlobal optimal) arasındakı fərq nədir?
155. **Interval Scheduling** (Interval Planlaşdırma) problemi necə həll olunur?
156. **Greedy Algorithm**-də **proof of correctness** (doğruluğun sübutu) necə aparılır?
157. **Kruskal’s Algorithm**-də **disjoint set** (ayrılmış dəst) necə istifadə olunur?
158. **Prim’s Algorithm**-də **priority queue** (prioritet növbəsi) necə tətbiq olunur?
159. **Greedy Algorithm**-də **time complexity** (vaxt mürəkkəbliyi) necə hesablanır?
160. **Huffman Coding**-də **binary tree** (ikili ağac) necə qurulur?

### Divide and Conquer
161. **Divide and Conquer** (Böl və Hökm Et) strategiyası nədir?
162. **Merge Sort** ilə **Divide and Conquer** necə tətbiq olunur?
163. **Quick Sort** ilə **Divide and Conquer** necə istifadə olunur?
164. **Binary Search** ilə **Divide and Conquer** necə əlaqəlidir?
165. **Strassen’s Matrix Multiplication** (Strassen Matris Çoxalması) nədir?
166. **Closest Pair of Points** (Ən Yaxın Nöqtə Cütü) problemi necə həll olunur?
167. **Karatsuba Algorithm** (Karatsuba Alqoritmi) nədir?
168. **Divide and Conquer**-də **recursion depth** (rekursiya dərinliyi) necə təsir edir?
169. **Fast Fourier Transform** (Sürətli Furye Çevrilməsi) nədir?
170. **Divide and Conquer** ilə **Dynamic Programming** arasındakı fərq nədir?
171. **Quick Sort**-da **partitioning** (bölüşdürmə) necə işləyir?
172. **Merge Sort**-da **merge** (birləşdirmə) prosesi necə optimallaşdırılır?
173. **Binary Search**-də **divide** (bölmə) strategiyası necə tətbiq olunur?
174. **Strassen’s Algorithm**-də **matrix partitioning** (matris bölüşdürməsi) necə işləyir?
175. **Closest Pair of Points**-də **divide and conquer** necə tətbiq olunur?
176. **Karatsuba Algorithm**-də **multiplication** (çoxalma) necə optimallaşdırılır?
177. **Fast Fourier Transform**-də **divide and conquer** necə istifadə olunur?
178. **Divide and Conquer**-də **base case** (əsas hal) necə təyin olunur?
179. **Divide and Conquer**-də **time complexity** (vaxt mürəkkəbliyi) necə hesablanır?
180. **Quick Sort**-da **tail recursion** (quyruq rekursiyası) necə optimallaşdırılır?

### Hashing Algorithms
181. **Hashing** (Xəşləmə) nədir və alqoritmlərdə necə istifadə olunur?
182. **Hash Function** (Xəş Funksiyası) nədir və necə işləyir?
183. **Collision Resolution** (Toqquşma Həlli) üsulları hansılardır?
184. **Separate Chaining** (Ayrı Zəncirləmə) necə işləyir?
185. **Open Addressing** (Açıq Ünvanlama) nədir?
186. **Linear Probing** (Xətti Yoxlama) ilə **Quadratic Probing** (Kvadratik Yoxlama) arasındakı fərq nədir?
187. **Double Hashing** (İkiqat Xəşləmə) nədir?
188. **Consistent Hashing** (Sabit Xəşləmə) nədir və nə üçün istifadə olunur?
189. **Hash Table** (Xəş Cədvəli) performansını necə optimallaşdırmaq olar?
190. **Bloom Filter** nədir və necə işləyir?
191. **HyperLogLog** nədir və necə istifadə olunur?
192. **Count-Min Sketch** nədir?
193. **HashMap**-də **hashCode()** metodu necə işləyir?
194. **Hashing**-də **load factor** (yükləmə faktoru) nədir?
195. **Hashing**-də **collision** (toqquşma) sayını azaltmaq üçün hansı üsullar istifadə olunur?
196. **Bloom Filter**-də **false positive** (yanlış müsbət) nədir?
197. **HyperLogLog**-də **cardinality estimation** (əsaslılıq təxmini) necə aparılır?
198. **Count-Min Sketch**-də **frequency estimation** (tezlik təxmini) necə işləyir?
199. **Hashing**-də **uniform distribution** (vahid paylanma) necə təmin olunur?
200. **Consistent Hashing**-də **virtual nodes** (virtual düyünlər) necə istifadə olunur?

### Other Algorithms
201. **Backtracking** (Geri Dönüş) alqoritmləri nədir?
202. **N-Queens Problem** (N Vəzir Problemi) necə həll olunur?
203. **Sudoku Solver** (Sudoku Həlledicisi) necə işləyir?
204. **Permutations** (Permutasiyalar) necə yaradılır?
205. **Combinations** (Kombinasiyalar) necə hesablanır?
206. **Knapsack Problem** ilə **Backtracking** necə tətbiq olunur?
207. **Graph Coloring** ilə **Backtracking** necə istifadə olunur?
208. **Randomized Algorithms** (Təsadüfi Alqoritmlər) nədir?
209. **Monte Carlo Algorithm** (Monte Karlo Alqoritmi) nədir?
210. **Las Vegas Algorithm** (Las Veqas Alqoritmi) nədir?
211. **Randomized Quick Sort** (Təsadüfi Sürətli Sıralama) necə işləyir?
212. **Karger’s Algorithm** (Karger Alqoritmi) nədir?
213. **Reservoir Sampling** (Rezervuar Nümunələmə) nədir?
214. **Approximation Algorithms** (Təxmini Alqoritmlər) nədir?
215. **Travelling Salesman Problem** (Səyyah Satıcı Problemi) təxmini alqoritmlərlə necə həll olunur?
216. **Vertex Cover Problem** (Təpə Örtüyü Problemi) nədir?
217. **Set Cover Problem** (Dəst Örtüyü Problemi) nədir?
218. **String Matching Algorithms** (Sətir Uyğunluğu Alqoritmləri) hansılardır?
219. **Knuth-Morris-Pratt Algorithm** (KMP Alqoritmi) nədir?
220. **Rabin-Karp Algorithm** (Rabin-Karp Alqoritmi) nədir?
221. **Boyer-Moore Algorithm** (Boyer-Moore Alqoritmi) nədir?
222. **KMP Algorithm** ilə **Rabin-Karp Algorithm** arasındakı fərq nədir?
223. **Aho-Corasick Algorithm** (Aho-Corasick Alqoritmi) nədir?
224. **String Matching**-də **pattern preprocessing** (nümunə ön emalı) necə işləyir?
225. **Regular Expression Matching** (Requlyar İfadə Uyğunluğu) necə həyata keçirilir?
226. **Bit Manipulation Algorithms** (Bit Manipulyasiya Alqoritmləri) nədir?
227. **Bitwise XOR** ilə **single number** problemi necə həll olunur?
228. **Bitwise AND** ilə **range queries** (aralıq sorğuları) necə aparılır?
229. **Two’s Complement** (İkili Komplement) necə işləyir?
230. **Bit Manipulation**-də **masking** (maskeleme) necə istifadə olunur?
231. **Union-Find** ilə **disjoint set** (ayrılmış dəst) necə idarə olunur?
232. **Path Compression** (Yol Sıxışdırması) Union-Find-də necə işləyir?
233. **Rank-based Union** (Səviyyə əsaslı Birləşmə) necə tətbiq olunur?
234. **Sliding Window Algorithm** (Sürüşən Pəncərə Alqoritmi) nədir?
235. **Two-Pointer Technique** (İki Göstərici Texnikası) nədir?
236. **Kadane’s Algorithm** (Kadane Alqoritmi) nədir?
237. **Manacher’s Algorithm** (Manacher Alqoritmi) nədir?
238. **Z-Algorithm** (Z Alqoritmi) nədir?
239. **Sliding Window**-də **maximum sum subarray** (maksimum cəmli altmassiv) necə tapılır?
240. **Two-Pointer Technique**-də **sorted array** (sıralanmış massiv) ilə necə işləyir?
241. **Kadane’s Algorithm**-də **maximum subarray sum** (maksimum altmassiv cəmi) necə hesablanır?
242. **Manacher’s Algorithm**-də **longest palindromic substring** (ən uzun palindromik altsətir) necə tapılır?
243. **Z-Algorithm**-də **pattern matching** (nümunə uyğunluğu) necə aparılır?
244. **Reservoir Sampling**-də **random selection** (təsadüfi seçim) necə təmin olunur?
245. **Monte Carlo Algorithm**-də **probability** (ehtimal) necə istifadə olunur?
246. **Las Vegas Algorithm**-də **correctness** (doğruluq) necə təmin olunur?
247. **Karger’s Algorithm**-də **minimum cut** (minimum kəsik) necə tapılır?
248. **Approximation Algorithms**-də **trade-off** (mübadilə) necə idarə olunur?
249. **Vertex Cover Problem**-də **greedy approximation** (acgöz təxmini) necə tətbiq olunur?
250. **Set Cover Problem**-də **approximation ratio** (təxmini nisbət) nədir?
251. **String Matching**-də **hashing** (xəşləmə) necə istifadə olunur?
252. **KMP Algorithm**-də **prefix function** (prefiks funksiyası) necə hesablanır?
253. **Rabin-Karp Algorithm**-də **rolling hash** (sürüşən xəş) necə işləyir?
254. **Boyer-Moore Algorithm**-də **bad character heuristic** (pis simvol evristikası) nədir?
255. **Aho-Corasick Algorithm**-də **trie** (prefiks ağacı) necə istifadə olunur?
256. **Bit Manipulation**-də **power of two** (ikinin qüvvəti) necə yoxlanılır?
257. **Union-Find**-də **connected components** (bağlı komponentlər) necə tapılır?
258. **Sliding Window**-də **minimum window substring** (minimum pəncərə altsətiri) necə tapılır?
259. **Two-Pointer Technique**-də **array merging** (massiv birləşdirmə) necə aparılır?
260. **Kadane’s Algorithm**-də **circular array** (dairəvi massiv) ilə necə işləyir?
261. **Manacher’s Algorithm**-də **even-length palindromes** (cüt uzunluqlu palindromlar) necə tapılır?
262. **Z-Algorithm**-də **Z-array** (Z-massivi) necə hesablanır?
263. **Reservoir Sampling**-də **stream processing** (axın emalı) necə həyata keçirilir?
264. **Monte Carlo Algorithm**-də **random sampling** (təsadüfi nümunələmə) necə işləyir?
265. **Las Vegas Algorithm**-də **randomized correctness** (təsadüfi doğruluğ) necə təmin olunur?
266. **Karger’s Algorithm**-də **randomized contraction** (təsadüfi sıxılma) necə işləyir?
267. **Approximation Algorithms**-də **polynomial time** (polinomial vaxt) necə təmin olunur?
268. **Vertex Cover Problem**-də **2-approximation** (2-təxmini) alqoritmi nədir?
269. **Set Cover Problem**-də **greedy approach** (acgöz yanaşma) necə işləyir?
270. **String Matching**-də **multiple patterns** (çoxlu nümunələr) necə tapılır?
271. **KMP Algorithm**-də **failure function** (uğursuzluq funksiyası) necə işləyir?
272. **Rabin-Karp Algorithm**-də **hash collision** (xəş toqquşması) necə idarə olunur?
273. **Boyer-Moore Algorithm**-də **good suffix heuristic** (yaxşı sufiks evristikası) nədir?
274. **Aho-Corasick Algorithm**-də **failure links** (uğursuzluq bağlantıları) necə qurulur?
275. **Bit Manipulation**-də **count set bits** (qurulmuş bitlərin sayılması) necə aparılır?
276. **Union-Find**-də **path compression** (yol sıxışdırması) ilə **rank** arasındakı əlaqə nədir?
277. **Sliding Window**-də **fixed-size window** (sabit ölçülü pəncərə) necə işləyir?
278. **Two-Pointer Technique**-də **reverse pointers** (tərs göstəricilər) necə istifadə olunur?
279. **Kadane’s Algorithm**-də **negative numbers** (mənfi ədədlər) ilə necə işləyir?
280. **Manacher’s Algorithm**-də **center expansion** (mərkəz genişlənməsi) necə işləyir?
281. **Z-Algorithm**-də **pattern preprocessing** (nümunə ön emalı) necə aparılır?
282. **Reservoir Sampling**-də **weighted sampling** (çəkili nümunələmə) necə həyata keçirilir?
283. **Monte Carlo Algorithm**-də **error probability** (səhv ehtimalı) necə idarə olunur?
284. **Las Vegas Algorithm**-də **expected runtime** (gözlənilən işləmə müddəti) necə hesablanır?
285. **Karger’s Algorithm**-də **success probability** (uğur ehtimalı) necə artır?
286. **Approximation Algorithms**-də **NP-hard problems** (NP-çətin problemlər) necə həll olunur?
287. **Vertex Cover Problem**-də **matching-based approach** (uyğunlaşma əsaslı yanaşma) nədir?
288. **Set Cover Problem**-də **logarithmic approximation** (loqarifmik təxmini) necə işləyir?
289. **String Matching**-də **suffix tree** (sufiks ağacı) necə istifadə olunur?
290. **KMP Algorithm**-də **partial match table** (qismən uyğunluq cədvəli) necə yaradılır?
291. **Rabin-Karp Algorithm**-də **modular arithmetic** (modul arifmetikası) necə tətbiq olunur?
292. **Boyer-Moore Algorithm**-də **skip table** (atlama cədvəli) necə qurulur?
293. **Aho-Corasick Algorithm**-də **state machine** (vəziyyət maşını) necə işləyir?
294. **Bit Manipulation**-də **bitwise operations** (bit əməliyyatları) performansı necə artır?
295. **Union-Find**-də **amortized complexity** (amortizasiya edilmiş mürəkkəblik) nədir?
296. **Sliding Window**-də **variable-size window** (dəyişkən ölçülü pəncərə) necə işləyir?
297. **Two-Pointer Technique**-də **linked list** (bağlı siyahı) ilə necə istifadə olunur?
298. **Kadane’s Algorithm**-də **maximum product subarray** (maksimum hasilli altmassiv) necə tapılır?
299. **Manacher’s Algorithm**-də **odd-length palindromes** (tək uzunluqlu palindromlar) necə tapılır?
300. **Z-Algorithm**-də **substring matching** (altsətir uyğunluğu) necə həyata keçirilir?

---

# RabbitMQ Müsahibə Sualları

Bu sənəd Java, Hibernate, Spring Boot, Data Structures/Collections, Design Patterns, Algorithms və RabbitMQ ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Arxitektura və Komponentlər](#arxitektura-və-komponentlər)
  - [Exchange Növləri](#exchange-növləri)
  - [Queue İdarəetmə](#queue-idarəetmə)
  - [Mesajlaşma Nümunələri](#mesajlaşma-nümunələri)
  - [Performans və Optimallaşdırma](#performans-və-optimallaşdırma)
  - [Təhlükəsizlik](#təhlükəsizlik)
  - [Clustering və Yüksək Əlçatanlıq](#clustering-və-yüksək-əlçatanlıq)
  - [Spring ilə İnteqrasiya](#spring-ilə-inteqrasiya)
  - [Digər Mövzular](#digər-mövzular)

## RabbitMQ

### Ümumi Suallar
1. **RabbitMQ** nədir və nə üçün istifadə olunur?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
2. **AMQP** (Advanced Message Queuing Protocol - Qabaqcıl Mesaj Növbələmə Protokolu) nədir?
3. **RabbitMQ**-nun digər mesaj brokerləri ilə müqayisədə üstünlükləri nələrdir?[](https://mindmajix.com/rabbitmq-interview-questions)
4. **RabbitMQ**-nun **Kafka** ilə fərqləri nələrdir?[](https://www.interviewbit.com/kafka-interview-questions/)
5. **RabbitMQ**-nun **ActiveMQ** ilə müqayisədə fərqləri nələrdir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
6. **RabbitMQ**-nun açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
7. **RabbitMQ**-nun hansı proqramlaşdırma dillərini dəstəklədiyi nədir?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
8. **RabbitMQ**-nun mikroservis arxitekturasında rolu nədir?[](https://mindmajix.com/rabbitmq-interview-questions)
9. **RabbitMQ**-nun əsas xüsusiyyətləri hansılardır?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
10. **RabbitMQ**-nun istifadəsi zamanı qarşılaşılacaq çətinliklər nələrdir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
11. **RabbitMQ**-nun **Erlang** dilində yazılmasının üstünlükləri nələrdir?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
12. **RabbitMQ**-nun hansı protokolları dəstəklədiyi nədir (AMQP, MQTT, STOMP)?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
13. **RabbitMQ**-nun **message-oriented middleware** (mesaj yönümlü ara proqram) kimi rolu nədir?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
14. **RabbitMQ**-nun **asynchronous messaging** (asinxron mesajlaşma) üçün faydaları nələrdir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
15. **RabbitMQ**-nun **enterprise** tətbiqlərdə istifadəsi necədir?

### Arxitektura və Komponentlər
16. **Producer** (Mesaj İstehsalçısı) nədir və RabbitMQ-da rolu nədir?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
17. **Consumer** (Mesaj İstehlakçısı) nədir və necə işləyir?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
18. **Queue** (Növbə) nədir və RabbitMQ-da hansı funksiyanı yerinə yetirir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
19. **Exchange** (Mübadilə) nədir və mesaj yönləndirməsində rolu nədir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
20. **Binding** (Bağlama) nədir və necə təyin olunur?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
21. **Routing Key** (Yönləndirmə Açarı) nədir və necə istifadə olunur?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
22. **Virtual Host** (Virtual Host - Virtual Ev Sahibi) nədir və nə üçün istifadə olunur?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
23. **Channel** (Kanal) nədir və RabbitMQ-da necə işləyir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
24. **Connection** (Əlaqə) ilə **Channel** arasındakı fərq nədir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
25. **Message Acknowledgment** (Mesaj Təsdiqləmə) nədir və niyə vacibdir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
26. **Publisher Confirms** (Nəşriyyat Təsdiqləri) nədir?[](https://medium.com/%40razzak.cse65/rabbitmq-interview-q-a-grouped-by-difficulty-level-6ce55df26674)
27. **Dead Letter Queue** (Ölü Məktub Növbəsi) nədir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
28. **Dead Letter Exchange** (Ölü Məktub Mübadiləsi) nədir və necə işləyir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
29. **Message Durability** (Mesaj Davamlılığı) nədir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
30. **Persistent Messages** (Davamlı Mesajlar) ilə **Transient Messages** (Müvəqqəti Mesajlar) arasındakı fərq nədir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
31. **RabbitMQ**-nun **message flow** (mesaj axını) prosesi necədir?[](https://www.techgeeknext.com/java/rabbitmq-interview-questions)
32. **RabbitMQ**-nun **broker** (broker) kimi rolu nədir?[](https://github.com/rhidoyhasanmahmud/The-Anatomy-of-RabbitMQ)
33. **RabbitMQ**-da **message format** (mesaj formatı) necə təyin olunur?
34. **RabbitMQ**-da **message priority** (mesaj prioriteti) necə idarə olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
35. **RabbitMQ**-nun **AMQP 0-9-1** protokolu ilə bağlı xüsusiyyətləri nələrdir?[](https://github.com/rhidoyhasanmahmud/The-Anatomy-of-RabbitMQ)

### Exchange Növləri
36. **Direct Exchange** (Birbaşa Mübadilə) nədir və nə vaxt istifadə olunur?[](https://medium.com/%40razzak.cse65/rabbitmq-interview-q-a-grouped-by-difficulty-level-6ce55df26674)
37. **Fanout Exchange** (Fanout Mübadiləsi) nədir və necə işləyir?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
38. **Topic Exchange** (Mövzu Mübadiləsi) nədir və nə üçün istifadə olunur?[](https://medium.com/%40razzak.cse65/rabbitmq-interview-q-a-grouped-by-difficulty-level-6ce55df26674)
39. **Headers Exchange** (Başlıq Mübadiləsi) nədir və necə tətbiq olunur?[](https://medium.com/%40razzak.cse65/rabbitmq-interview-q-a-grouped-by-difficulty-level-6ce55df26674)
40. **Direct Exchange** ilə **Topic Exchange** arasındakı fərq nədir?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
41. **Fanout Exchange** ilə **Topic Exchange** arasındakı fərq nədir?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
42. **Headers Exchange** ilə **Topic Exchange** arasındakı performans fərqi nədir?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
43. **Exchange Type** (Mübadilə Növü) seçimi hansı amillərdən asılıdır?
44. **Default Exchange** (Standart Mübadilə) nədir və necə işləyir?
45. **Exchange**-də **routing key** ilə **binding key** arasındakı fərq nədir?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
46. **Topic Exchange**-də **wildcard matching** (joker simvol uyğunluğu) necə işləyir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
47. **Fanout Exchange**-də mesajların bütün növbələrə paylanması necə təmin olunur?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
48. **Headers Exchange**-də **header attributes** (başlıq atributları) necə istifadə olunur?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
49. **Exchange**-də **alternate exchange** (alternativ mübadilə) nədir?
50. **Exchange**-də **auto-delete** (avtomatik silinmə) xüsusiyyəti nədir?

### Queue İdarəetmə
51. **Queue** (Növbə) necə yaradılır və konfiqurasiya olunur?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
52. **Durable Queue** (Davamlı Növbə) ilə **Non-Durable Queue** (Qeyri-Davamlı Növbə) arasındakı fərq nədir?[](https://mindmajix.com/rabbitmq-interview-questions)
53. **Exclusive Queue** (Eksklüziv Növbə) nədir?[](https://www.scmgalaxy.com/tutorials/top-50-rabbitmq-interview-questions-with-answers/)
54. **Auto-Delete Queue** (Avtomatik Silinən Növbə) nədir?[](https://www.scmgalaxy.com/tutorials/top-50-rabbitmq-interview-questions-with-answers/)
55. **Queue Length Limit** (Növbə Uzunluğu Limiti) necə təyin olunur?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
56. **Message TTL** (Mesaj Yaşama Müddəti) nədir və necə konfiqurasiya olunur?[](https://interviewprep.org/rabbitmq-interview-questions/)
57. **Queue Mirroring** (Növbə Güzgülənməsi) nədir və necə işləyir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
58. **Dead Letter Queue** (Ölü Məktub Növbəsi) hansı hallarda istifadə olunur?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
59. **x-dead-letter-exchange** parametri nədir?[](https://interviewprep.org/rabbitmq-interview-questions/)
60. **x-dead-letter-routing-key** parametri nədir?[](https://interviewprep.org/rabbitmq-interview-questions/)
61. **Queue**-də **message expiration** (mesajın müddəti bitməsi) necə idarə olunur?
62. **Queue**-də **priority queues** (prioritet növbələri) necə təyin olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
63. **Queue**-də **consumer tag** (istehlakçı etiketi) nədir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
64. **Queue**-də **message prefetch count** (mesaj öncədən yükləmə sayı) necə təyin olunur?
65. **Queue**-də **requeue** (yenidən növbəyə qaytarma) necə işləyir?
66. **Queue**-də **message rejection** (mesaj rədd etmə) necə həyata keçirilir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
67. **Queue**-də **basic.qos** metodu nə üçün istifadə olunur?
68. **Queue**-də **purge** (təmizləmə) əməliyyatı nədir?
69. **Queue**-də **overflow behavior** (daşma davranışı) necə idarə olunur?
70. **Queue**-də **lazy queues** (tənbəl növbələr) nədir və nə üçün istifadə olunur?

### Mesajlaşma Nümunələri
71. **Point-to-Point** (Nöqtədən-Nöqtəyə) mesajlaşma nümunəsi nədir?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
72. **Publish/Subscribe** (Nəşr/Abunə) mesajlaşma nümunəsi nədir?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
73. **Request/Reply** (Sorğu/Cavab) mesajlaşma nümunəsi nədir?[](https://www.geeksforgeeks.org/blogs/introduction-to-rabbitmq/)
74. **Work Queue** (İş Növbəsi) nümunəsi nədir?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
75. **Publish/Subscribe** ilə **Point-to-Point** arasındakı fərq nədir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
76. **Request/Reply** nümunəsində **correlation ID** (korrelyasiya ID) nədir?
77. **Work Queue** ilə **load balancing** (yük balanslaşdırması) necə təmin olunur?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
78. **Publish/Subscribe** nümunəsində **Fanout Exchange** necə istifadə olunur?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
79. **Request/Reply** nümunəsində **temporary queues** (müvəqqəti növbələr) necə yaradılır?
80. **Work Queue**-də **fair dispatch** (ədalətli göndəriş) necə təmin olunur?[](https://www.slideshare.net/slideshow/rabbitmq-interview-questions-and-answers/254165925)
81. **Publish/Subscribe** ilə **Topic Exchange** necə istifadə olunur?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
82. **Point-to-Point** ilə **Direct Exchange** necə əlaqəlidir?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
83. **Request/Reply** nümunəsində **reply-to queue** (cavab növbəsi) nədir?
84. **Work Queue**-də **multiple consumers** (çoxsaylı istehlakçılar) necə idarə olunur?
85. **Publish/Subscribe** nümunəsində **message filtering** (mesaj süzgəcləmə) necə aparılır?

### Performans və Optimallaşdırma
86. **RabbitMQ**-da **performance monitoring** (performans monitorinqi) necə həyata keçirilir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
87. **RabbitMQ Management Plugin** ilə performans necə monitorinq edilir?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
88. **RabbitMQ**-da **message rate** (mesaj sürəti) necə ölçülür?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
89. **RabbitMQ**-da **queue depth** (növbə dərinliyi) necə izlənilir?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
90. **RabbitMQ**-da **connection count** (əlaqə sayı) necə optimallaşdırılır?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
91. **RabbitMQ**-da **channel multiplexing** (kanal çoxsaylılığı) nədir?
92. **RabbitMQ**-da **message batching** (mesaj toplulaşdırması) necə tətbiq olunur?
93. **RabbitMQ**-da **prefetch count** (öncədən yükləmə sayı) performansına necə təsir edir?
94. **RabbitMQ**-da **lazy queues** performans baxımından necə üstünlük təmin edir?
95. **RabbitMQ**-da **message compression** (mesaj sıxışdırması) necə həyata keçirilir?
96. **RabbitMQ**-da **message size** (mesaj ölçüsü) performansına necə təsir edir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
97. **RabbitMQ**-da **queue mirroring** performansına necə təsir edir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
98. **RabbitMQ**-da **high throughput** (yüksək ötürmə qabiliyyəti) necə təmin olunur?
99. **RabbitMQ**-da **low latency** (aşağı gecikmə) necə əldə olunur?
100. **RabbitMQ**-da **bottleneck** (darboğaz) problemləri necə aşkarlanır?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
101. **RabbitMQ**-da **message persistence** (mesaj davamlılığı) performansına necə təsir edir?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
102. **RabbitMQ**-da **disk I/O** (disk giriş/çıxış) optimallaşdırması necə aparılır?
103. **RabbitMQ**-da **memory usage** (yaddaş istifadəsi) necə optimallaşdırılır?
104. **RabbitMQ**-da **CPU usage** (prosessor istifadəsi) necə idarə olunur?
105. **RabbitMQ**-da **Prometheus** və **Grafana** ilə monitorinq necə qurulur?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)

### Təhlükəsizlik
106. **RabbitMQ**-da **authentication** (autentifikasiya) necə konfiqurasiya olunur?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
107. **RabbitMQ**-da **authorization** (səlahiyyətləndirmə) necə təmin olunur?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
108. **RabbitMQ**-da **SSL/TLS** şifrələməsi necə aktivləşdirilir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
109. **RabbitMQ**-da **Access Control Lists (ACLs)** (Giriş Nəzarət Siyahıları) nədir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
110. **RabbitMQ**-da **message spoofing** (mesaj saxtalaşdırması) necə qarşısı alınır?[](https://www.projectpractical.com/rabbitmq-interview-questions-and-answers/)
111. **RabbitMQ**-da **message replay** (mesaj təkrar oynatma) hücumlarına qarşı necə qorunulur?[](https://www.projectpractical.com/rabbitmq-interview-questions-and-answers/)
112. **RabbitMQ**-da **user management** (istifadəçi idarəetmə) necə aparılır?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
113. **RabbitMQ**-da **password policies** (şifrə siyasətləri) necə təyin olunur?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
114. **RabbitMQ**-da **network security** (şəbəkə təhlükəsizliyi) necə təmin olunur?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
115. **RabbitMQ**-da **firewall** konfiqurasiyası necə aparılır?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
116. **RabbitMQ**-da **secure communication** (təhlükəsiz rabitə) üçün hansı protokollar istifadə olunur?
117. **RabbitMQ**-da **role-based access control** (rol əsaslı giriş nəzarəti) necə tətbiq olunur?
118. **RabbitMQ**-da **encryption at rest** (sabit vəziyyətdə şifrələmə) necə təmin olunur?
119. **RabbitMQ**-da **audit logging** (audit qeydiyyatı) necə aktivləşdirilir?
120. **RabbitMQ**-da **LDAP** inteqrasiyası necə həyata keçirilir?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)

### Clustering və Yüksək Əlçatanlıq
121. **RabbitMQ Cluster** (RabbitMQ Klasteri) nədir və necə konfiqurasiya olunur?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
122. **RabbitMQ**-da **mirrored queues** (güzgülənmiş növbələr) necə işləyir?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
123. **RabbitMQ**-da **high availability** (yüksək əlçatanlıq) necə təmin olunur?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
124. **RabbitMQ**-da **load balancing** (yük balanslaşdırması) necə həyata keçirilir?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
125. **RabbitMQ**-da **failover** (əks funksionallıq) necə idarə olunur?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
126. **RabbitMQ**-da **node failure** (düyün sıradan çıxması) zamanı mesajlar necə qorunur?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
127. **RabbitMQ**-da **clustering** performansına necə təsir edir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
128. **RabbitMQ**-da **federation** nədir və necə konfiqurasiya olunur?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
129. **RabbitMQ Federation Plugin** ilə mesaj mübadiləsi necə həyata keçirilir?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
130. **RabbitMQ Shovel Plugin** nədir və nə üçün istifadə olunur?[](https://www.scmgalaxy.com/tutorials/top-50-rabbitmq-interview-questions-with-answers/)
131. **RabbitMQ**-da **network partitioning** (şəbəkə bölünməsi) necə idarə olunur?[](https://interviewprep.org/rabbitmq-interview-questions/)
132. **RabbitMQ**-da **net_ticktime** parametri nədir?[](https://interviewprep.org/rabbitmq-interview-questions/)
133. **RabbitMQ**-da **mirrored queues** ilə **federation** arasındakı fərq nədir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
134. **RabbitMQ**-da **cluster scalability** (klaster miqyaslılığı) necə təmin olunur?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
135. **RabbitMQ**-da **dynamic cluster expansion** (dinamik klaster genişlənməsi) necə aparılır?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
136. **RabbitMQ**-da **HAProxy** ilə yük balanslaşdırması necə qurulur?
137. **RabbitMQ**-da **quorum queues** (kvorum növbələri) nədir?
138. **RabbitMQ**-da **classic queues** (klassik növbələr) ilə **quorum queues** arasındakı fərq nədir?
139. **RabbitMQ**-da **queue master location** (növbə ustası yeri) necə təyin olunur?
140. **RabbitMQ**-da **replication** (təkrarlanma) necə işləyir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)

### Spring ilə İnteqrasiya
141. **Spring AMQP** ilə RabbitMQ inteqrasiyası necə həyata keçirilir?[](https://www.slideshare.net/slideshow/rabbitmq-interview-questions-and-answers/254165925)
142. **Spring Boot** ilə RabbitMQ necə konfiqurasiya olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
143. **Spring Cloud Stream** ilə RabbitMQ inteqrasiyası nədir?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
144. **@RabbitListener** annotasiyası nədir və necə istifadə olunur?[](https://github.com/rhidoyhasanmahmud/The-Anatomy-of-RabbitMQ)
145. **RabbitTemplate** sinfi nədir və necə işləyir?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
146. **Spring AMQP**-də **message converter** (mesaj çeviricisi) necə təyin olunur?
147. **Spring Boot**-da **RabbitMQ listener** (RabbitMQ dinləyicisi) necə yaradılır?[](https://github.com/rhidoyhasanmahmud/The-Anatomy-of-RabbitMQ)
148. **Spring AMQP**-də **retry mechanism** (təkrar sınaq mexanizmi) necə konfiqurasiya olunur?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
149. **Spring Cloud Stream**-də **binding** (bağlama) necə təyin olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
150. **Spring Boot**-da **RabbitMQ exchange types** (mübadilə növləri) necə tətbiq olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
151. **Spring AMQP**-də **message acknowledgment** (mesaj təsdiqləmə) necə idarə olunur?
152. **Spring Boot**-da **Dead Letter Queue** necə konfiqurasiya olunur?[](https://github.com/rhidoyhasanmahmud/The-Anatomy-of-RabbitMQ)
153. **Spring AMQP**-də **error handling** (səhv idarəetmə) necə həyata keçirilir?
154. **Spring Cloud Stream**-də **consumer groups** (istehlakçı qrupları) necə istifadə olunur?
155. **Spring Boot**-da **RabbitMQ connection pooling** (əlaqə hovuzu) necə təmin olunur?
156. **Spring AMQP**-də **publisher confirms** necə konfiqurasiya olunur?
157. **Spring Boot**-da **RabbitMQ retry policies** (təkrar sınaq siyasətləri) necə təyin olunur?
158. **Spring Cloud Stream**-də **partitioning** (bölüşdürmə) necə həyata keçirilir?
159. **Spring AMQP**-də **message serialization** (mesaj seriyalaşdırması) necə aparılır?
160. **Spring Boot**-da **RabbitMQ monitoring** (RabbitMQ monitorinqi) necə qurulur?

### Digər Mövzular
161. **RabbitMQ Management Plugin** nədir və necə aktivləşdirilir?[](https://www.remoterocketship.com/advice/10-rabbitmq-interview-questions-and-answers-in-2023)
162. **rabbitmqctl** komanda xətti aləti nədir və necə istifadə olunur?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
163. **RabbitMQ**-da **policies** (siyasətlər) nədir və necə təyin olunur?[](https://interviewprep.org/rabbitmq-interview-questions/)
164. **RabbitMQ**-da **message tracing** (mesaj izləmə) necə həyata keçirilir?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
165. **RabbitMQ**-da **federation plugin** ilə klasterlər arası mesajlaşma necə təmin olunur?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
166. **RabbitMQ Shovel Plugin** ilə mesaj ötürülməsi necə aparılır?[](https://www.scmgalaxy.com/tutorials/top-50-rabbitmq-interview-questions-with-answers/)
167. **RabbitMQ**-da **STOMP** protokolu nədir və necə istifadə olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
168. **RabbitMQ**-da **MQTT** protokolu nədir və necə dəstəklənir?[](https://www.devopsschool.com/blog/top-50-rabbitmq-interview-questions-answer/)
169. **RabbitMQ**-da **HTTP API** necə istifadə olunur?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
170. **RabbitMQ**-da **plugins** (plaginlər) necə aktivləşdirilir?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
171. **RabbitMQ**-da **message retry** (mesaj təkrar sınağı) necə konfiqurasiya olunur?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
172. **RabbitMQ**-da **message expiration policies** (mesaj müddəti siyasətləri) necə təyin olunur?
173. **RabbitMQ**-da **consumer priorities** (istehlakçı prioritetləri) necə idarə olunur?
174. **RabbitMQ**-da **message headers** (mesaj başlıqları) necə istifadə olunur?
175. **RabbitMQ**-da **message properties** (mesaj xassələri) hansılardır?
176. **RabbitMQ**-da **alternate exchange** necə təyin olunur?
177. **RabbitMQ**-da **queue policies** (növbə siyasətləri) necə tətbiq olunur?[](https://interviewprep.org/rabbitmq-interview-questions/)
178. **RabbitMQ**-da **exchange policies** (mübadilə siyasətləri) nədir?
179. **RabbitMQ**-da **message routing** (mesaj yönləndirmə) optimallaşdırması necə aparılır?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
180. **RabbitMQ**-da **message deduplication** (mesaj təkrarlanmasının qarşısını alma) necə həyata keçirilir?
181. **RabbitMQ**-da **message ordering** (mesaj sıralaması) necə təmin olunur?[](https://www.wisdomjobs.com/e-university/rabbitmq-interview-questions.html)
182. **RabbitMQ**-da **message batch processing** (mesaj toplu emalı) necə aparılır?
183. **RabbitMQ**-da **consumer cancellation** (istehlakçı ləğvi) necə idarə olunur?
184. **RabbitMQ**-da **message redelivery** (mesaj yenidən göndərilməsi) necə işləyir?
185. **RabbitMQ**-da **message timeout** (mesaj vaxtaşımı) necə təyin olunur?
186. **RabbitMQ**-da **priority queues** ilə **message prioritization** (mesaj prioritetləşdirmə) necə həyata keçirilir?
187. **RabbitMQ**-da **message compression** (mesaj sıxışdırması) hansı hallarda istifadə olunur?
188. **RabbitMQ**-da **message encryption** (mesaj şifrələməsi) necə tətbiq olunur?
189. **RabbitMQ**-da **message validation** (mesaj doğrulaması) necə aparılır?
190. **RabbitMQ**-da **message logging** (mesaj qeydiyyatı) necə konfiqurasiya olunur?
191. **RabbitMQ**-da **queue monitoring** (növbə monitorinqi) necə həyata keçirilir?
192. **RabbitMQ**-da **exchange monitoring** (mübadilə monitorinqi) necə aparılır?
193. **RabbitMQ**-da **connection monitoring** (əlaqə monitorinqi) necə təmin olunur?
194. **RabbitMQ**-da **health checks** (sağlamlıq yoxlamaları) necə qurulur?
195. **RabbitMQ**-da **metrics** (metrikalar) hansılardır və necə toplanır?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
196. **RabbitMQ**-da **Prometheus** ilə inteqrasiya necə aparılır?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
197. **RabbitMQ**-da **Grafana** ilə vizualizasiya necə qurulur?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
198. **RabbitMQ**-da **message tracing** ilə **debugging** (sazlama) necə aparılır?
199. **RabbitMQ**-da **log aggregation** (qeyd toplama) necə həyata keçirilir?
200. **RabbitMQ**-da **distributed tracing** (paylanmış izləmə) necə tətbiq olunur?[](https://www.javainuse.com/misc/rabbitmq-interview-questions)
201. **RabbitMQ**-da **message serialization** (mesaj seriyalaşdırması) necə idarə olunur?
202. **RabbitMQ**-da **message deserialization** (mesaj deserializasiyası) necə aparılır?
203. **RabbitMQ**-da **message validation** (mesaj doğrulaması) üçün hansı alətlər istifadə olunur?
204. **RabbitMQ**-da **message transformation** (mesaj transformasiyası) necə həyata keçirilir?
205. **RabbitMQ**-da **message routing patterns** (mesaj yönləndirmə nümunələri) hansılardır?
206. **RabbitMQ**-da **message retry policies** (mesaj təkrar sınaq siyasətləri) necə təyin olunur?
207. **RabbitMQ**-da **message expiration** ilə **TTL** arasındakı fərq nədir?
208. **RabbitMQ**-da **message delivery guarantees** (mesaj çatdırılma zəmanətləri) nədir?
209. **RabbitMQ**-da **at-least-once delivery** (ən azı bir dəfə çatdırılma) necə təmin olunur?
210. **RabbitMQ**-da **at-most-once delivery** (ən çox bir dəfə çatdırılma) necə işləyir?
211. **RabbitMQ**-da **exactly-once delivery** (dəqiq bir dəfə çatdırılma) mümkünmü?
212. **RabbitMQ**-da **message idempotency** (mesaj idempotentliyi) necə təmin olunur?
213. **RabbitMQ**-da **message versioning** (mesaj versiyalaşdırma) necə idarə olunur?
214. **RabbitMQ**-da **message filtering** (mesaj süzgəcləmə) necə həyata keçirilir?
215. **RabbitMQ**-da **message routing** ilə **message filtering** arasındakı fərq nədir?

### Əlavə Mövzular
216. **RabbitMQ**-da **management console** (idarəetmə konsolu) necə istifadə olunur?[](https://www.finalroundai.com/blog/rabbitmq-interview-questions)
217. **RabbitMQ**-da **CLI tools** (komanda xətti alətləri) hansılardır?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
218. **RabbitMQ**-da **rabbitmqadmin** aləti nədir?[](https://www.onlineinterviewquestions.com/rabbitmq-interview-questions/)
219. **RabbitMQ**-da **plugins** (plaginlər) hansı funksiyaları təmin edir?[](https://www.mytectra.com/interview-question/frequently-asked-rabbitmq-interview-questions-and-answers)
220. **RabbitMQ**-da **federation** ilə **shovel** arasındakı fərq nədir?[](https://www.scmgalaxy.com/tutorials/top-50-rabbitmq-interview-questions-with-answers/)
221. **RabbitMQ**-da **consistent hashing exchange** (sabit xəşləmə mübadiləsi) nədir?
222. **RabbitMQ**-da **message priority** ilə **queue priority** arasındakı fərq nədir?
223. **RabbitMQ**-da **message batching** ilə **message compression** arasındakı fərq nədir?
224. **RabbitMQ**-da **consumer prefetch** ilə **basic.qos** arasındakı əlaqə nədir?
225. **RabbitMQ**-da **message requeue** ilə **message redelivery** arasındakı fərq nədir?
226. **RabbitMQ**-da **exchange-to-exchange binding** (mübadilədən-mübadiləyə bağlama) nədir?
227. **RabbitMQ**-da **message tracing plugin** (mesaj izləmə plagini) necə istifadə olunur?
228. **RabbitMQ**-da **management API** ilə **HTTP API** arasındakı fərq nədir?
229. **RabbitMQ**-da **message encryption** ilə **SSL/TLS** arasındakı fərq nədir?
230. **RabbitMQ**-da **queue policies** ilə **exchange policies** arasındakı fərq nədir?
231. **RabbitMQ**-da **message retry** ilə **dead letter queue** arasındakı əlaqə nədir?
232. **RabbitMQ**-da **message acknowledgment modes** (mesaj təsdiqləmə rejimləri) hansılardır?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
233. **RabbitMQ**-da **automatic acknowledgment** (avtomatik təsdiqləmə) nədir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
234. **RabbitMQ**-da **manual acknowledgment** (əl ilə təsdiqləmə) necə işləyir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
235. **RabbitMQ**-da **negative acknowledgment (NACK)** (mənfi təsdiqləmə) nədir?[](https://hellointern.in/blog/rabbitmq-interview-questions-and-answers-54896)
236. **RabbitMQ**-da **message durability** ilə **queue durability** arasındakı fərq nədir?
237. **RabbitMQ**-da **message store** (mesaj anbarı) necə işləyir?[](https://mindmajix.com/rabbitmq-interview-questions)
238. **RabbitMQ**-da **Mnesia** verilənlər bazası nədir və necə istifadə olunur?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
239. **RabbitMQ**-da **external database** (xarici verilənlər bazası) inteqrasiyası necə aparılır?[](https://www.acte.in/rabbitmq-interview-questions-and-answers)
240. **RabbitMQ**-da **message delivery semantics** (mesaj çatdırılma semantikası) nədir?
241. **RabbitMQ**-da **message routing** ilə **message delivery** arasındakı fərq nədir?
242. **RabbitMQ**-da **message headers** ilə **message properties** arasındakı fərq nədir?
243. **RabbitMQ**-da **message deduplication** ilə **idempotency** arasındakı fərq nədir?
244. **RabbitMQ**-da **message versioning** ilə **message transformation** arasındakı fərq nədir?
245. **RabbitMQ**-da **message filtering** ilə **message validation** arasındakı fərq nədir?
246. **RabbitMQ**-da **message logging** ilə **message tracing** arasındakı fərq nədir?
247. **RabbitMQ**-da **queue monitoring** ilə **exchange monitoring** arasındakı fərq nədir?
248. **RabbitMQ**-da **connection pooling** (əlaqə hovuzu) necə optimallaşdırılır?
249. **RabbitMQ**-da **message batching** ilə **bulk operations** (toplu əməliyyatlar) arasındakı fərq nədir?
250. **RabbitMQ**-da **message prefetch** ilə **message batching** arasındakı fərq nədir?
251. **RabbitMQ**-da **message retry** ilə **message redelivery** arasındakı fərq nədir?
252. **RabbitMQ**-da **message expiration** ilə **queue TTL** arasındakı fərq nədir?
253. **RabbitMQ**-da **consumer cancellation** ilə **message rejection** arasındakı fərq nədir?
254. **RabbitMQ**-da **message priority** ilə **consumer priority** arasındakı fərq nədir?
255. **RabbitMQ**-da **federation** ilə **sharding** (bölüşdürmə) arasındakı fərq nədir?
256. **RabbitMQ**-da **message compression** ilə **message encryption** arasındakı fərq nədir?
257. **RabbitMQ**-da **message validation** ilə **message transformation** arasındakı fərq nədir?
258. **RabbitMQ**-da **message logging** ilə **audit logging** arasındakı fərq nədir?
259. **RabbitMQ**-da **queue policies** ilə **message policies** arasındakı fərq nədir?
260. **RabbitMQ**-da **exchange policies** ilə **binding policies** arasındakı fərq nədir?
261. **RabbitMQ**-da **message tracing** ilə **distributed tracing** arasındakı fərq nədir?
262. **RabbitMQ**-da **message delivery guarantees** ilə **message acknowledgment** arasındakı fərq nədir?
263. **RabbitMQ**-da **message idempotency** ilə **message deduplication** arasındakı fərq nədir?
264. **RabbitMQ**-da **message versioning** ilə **message routing** arasındakı fərq nədir?
265. **RabbitMQ**-da **message filtering** ilə **message routing** arasındakı fərq nədir?
266. **RabbitMQ**-da **message batching** ilə **message prefetch** arasındakı fərq nədir?
267. **RabbitMQ**-da **message retry** ilə **message redelivery** arasındakı fərq nədir?
268. **RabbitMQ**-da **message expiration** ilə **message TTL** arasındakı fərq nədir?
269. **RabbitMQ**-da **consumer cancellation** ilə **message rejection** arasındakı fərq nədir?
270. **RabbitMQ**-da **message priority** ilə **queue priority** arasındakı fərq nədir?
271. **RabbitMQ**-da **federation** ilə **clustering** arasındakı fərq nədir?[](https://tutorialspedia.com/rabbitmq-interview-questions-answers/)
272. **RabbitMQ**-da **message compression** ilə **message batching** arasındakı fərq nədir?
273. **RabbitMQ**-da **message encryption** ilə **SSL/TLS** arasındakı fərq nədir?
274. **RabbitMQ**-da **message validation** ilə **message filtering** arasındakı fərq nədir?
275. **RabbitMQ**-da **message logging** ilə **message tracing** arasındakı fərq nədir?
276. **RabbitMQ**-da **queue monitoring** ilə **connection monitoring** arasındakı fərq nədir?
277. **RabbitMQ**-da **exchange monitoring** ilə **message monitoring** arasındakı fərq nədir?
278. **RabbitMQ**-da **message delivery semantics** ilə **message routing semantics** arasındakı fərq nədir?
279. **RabbitMQ**-da **message idempotency** ilə **message versioning** arasındakı fərq nədir?
280. **RabbitMQ**-da **message deduplication** ilə **message filtering** arasındakı fərq nədir?
281. **RabbitMQ**-da **message routing** ilə **message transformation** arasındakı fərq nədir?
282. **RabbitMQ**-da **message batching** ilə **message serialization** arasındakı fərq nədir?
283. **RabbitMQ**-da **message prefetch** ilə **message acknowledgment** arasındakı fərq nədir?
284. **RabbitMQ**-da **message retry** ilə **message expiration** arasındakı fərq nədir?
285. **RabbitMQ**-da **consumer priorities** ilə **queue priorities** arasındakı fərq nədir?
286. **RabbitMQ**-da **federation plugin** ilə **shovel plugin** arasındakı fərq nədir?
287. **RabbitMQ**-da **message compression** ilə **message deduplication** arasındakı fərq nədir?
288. **RabbitMQ**-da **message encryption** ilə **message validation** arasındakı fərq nədir?
289. **RabbitMQ**-da **message logging** ilə **message validation** arasındakı fərq nədir?
290. **RabbitMQ**-da **queue policies** ilə **consumer policies** arasındakı fərq nədir?
291. **RabbitMQ**-da **exchange policies** ilə **message policies** arasındakı fərq nədir?
292. **RabbitMQ**-da **message tracing** ilə **message logging** arasındakı fərq nədir?
293. **RabbitMQ**-da **message delivery guarantees** ilə **message persistence** arasındakı fərq nədir?
294. **RabbitMQ**-da **message idempotency** ilə **message deduplication** arasındakı fərq nədir?
295. **RabbitMQ**-da **message versioning** ilə **message filtering** arasındakı fərq nədir?
296. **RabbitMQ**-da **message routing** ilə **message delivery** arasındakı fərq nədir?
297. **RabbitMQ**-da **message batching** ilə **message compression** arasındakı fərq nədir?
298. **RabbitMQ**-da **message prefetch** ilə **message redelivery** arasındakı fərq nədir?
299. **RabbitMQ**-da **message retry** ilə **message acknowledgment** arasındakı fərq nədir?
300. **RabbitMQ**-da **message expiration** ilə **message validation** arasındakı fərq nədir?

---

# Kafka/Kafka Streams Müsahibə Sualları

Bu sənəd Kafka/Kafka Streams ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
- [Kafka və Kafka Streams](#kafka-və-kafka-streams)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Kafka Arxitekturası](#kafka-arxitekturası)
  - [Topic və Partition](#topic-və-partition)
  - [Producer və Consumer](#producer-və-consumer)
  - [Kafka Streams](#kafka-streams)
  - [Performans və Optimallaşdırma](#performans-və-optimallaşdırma)
  - [Təhlükəsizlik](#təhlükəsizlik)
  - [Clustering və Yüksək Əlçatanlıq](#clustering-və-yüksək-əlçatanlıq)
  - [Spring ilə İnteqrasiya](#spring-ilə-inteqrasiya)
  - [Digər Mövzular](#digər-mövzular)

## Kafka və Kafka Streams

### Ümumi Suallar
1. **Apache Kafka** nədir və nə üçün istifadə olunur?
2. **Kafka Streams** nədir və necə işləyir?
3. **Kafka**-nın **RabbitMQ** ilə müqayisədə fərqləri nələrdir?
4. **Kafka**-nın digər mesaj brokerləri ilə üstünlükləri nələrdir?
5. **Kafka**-nın **publish-subscribe** (nəşr-abunə) modeli necə işləyir?
6. **Kafka**-nın **event streaming** (hadisə axını) platforması kimi rolu nədir?
7. **Kafka**-nın **log-based** (jurnal əsaslı) arxitekturası nədir?
8. **Kafka**-nın açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?
9. **Kafka**-nın hansı proqramlaşdırma dillərini dəstəklədiyi nədir?
10. **Kafka**-nın mikroservis arxitekturasında istifadəsi necədir?
11. **Kafka Streams** ilə **Kafka** arasındakı fərq nədir?
12. **Kafka**-nın **real-time processing** (real vaxt emalı) üçün faydaları nələrdir?
13. **Kafka**-nın **big data** tətbiqlərində rolu nədir?
14. **Kafka**-nın **data retention** (məlumat saxlama) siyasəti nədir?
15. **Kafka**-nın **distributed system** (paylanmış sistem) kimi xüsusiyyətləri nələrdir?

### Kafka Arxitekturası
16. **Kafka Broker** (Kafka Brokeri) nədir və rolu nədir?
17. **Kafka Cluster** (Kafka Klasteri) necə işləyir?
18. **Topic** (Mövzu) nədir və Kafka-da necə təyin olunur?
19. **Partition** (Bölmə) nədir və Kafka-da necə istifadə olunur?
20. **Replication** (Təkrarlanma) Kafka-da necə təmin olunur?
21. **Leader** və **Follower** replikalar arasındakı fərq nədir?
22. **In-Sync Replicas (ISR)** (Sinxron Replikalar) nədir?
23. **Zookeeper** Kafka-da nə üçün istifadə olunur?
24. **Kafka Controller** nədir və hansı funksiyaları yerinə yetirir?
25. **Log Segment** (Jurnal Seqmenti) nədir və necə işləyir?
26. **Offset** (Ofset) nədir və Kafka-da necə idarə olunur?
27. **Consumer Group** (İstehlakçı Qrupu) nədir və necə işləyir?
28. **Producer** (İstehsalçı) ilə **Consumer** (İstehlakçı) arasındakı əlaqə nədir?
29. **Kafka Log** (Kafka Jurnalı) necə strukturlaşdırılır?
30. **Kafka**-nın **message format** (mesaj formatı) necədir?
31. **Kafka**-da **message key** (mesaj açarı) nə üçün istifadə olunur?
32. **Kafka**-da **message compression** (mesaj sıxışdırması) necə tətbiq olunur?
33. **Kafka**-da **message retention** (mesaj saxlama) müddəti necə təyin olunur?
34. **Kafka**-da **log compaction** (jurnal sıxışdırması) nədir?
35. **Kafka**-da **broker configuration** (broker konfiqurasiyası) hansı parametrləri əhatə edir?

### Topic və Partition
36. **Kafka Topic** (Kafka Mövzusu) necə yaradılır?
37. **Partition** sayının seçimi Kafka-da hansı amillərdən asılıdır?
38. **Kafka**-da **partition key** (bölmə açarı) nədir və necə istifadə olunur?
39. **Kafka**-da **replication factor** (təkrarlanma faktoru) necə təyin olunur?
40. **Kafka**-da **partition reassignment** (bölmə yenidən təyinatı) necə aparılır?
41. **Kafka**-da **preferred leader** (üstünlük verilən lider) nədir?
42. **Kafka**-da **partition balancing** (bölmə balanslaşdırması) necə təmin olunur?
43. **Kafka**-da **topic deletion** (mövzu silinməsi) necə həyata keçirilir?
44. **Kafka**-da **topic configuration** (mövzu konfiqurasiyası) hansı parametrləri əhatə edir?
45. **Kafka**-da **log retention** (jurnal saxlama) ilə **message retention** arasındakı fərq nədir?
46. **Kafka**-da **compacted topics** (sıxışdırılmış mövzular) necə işləyir?
47. **Kafka**-da **partition scaling** (bölmə miqyaslandırması) necə aparılır?
48. **Kafka**-da **partition skew** (bölmə əyriliyi) necə qarşısı alınır?
49. **Kafka**-da **topic naming conventions** (mövzu adlandırma qaydaları) nələrdir?
50. **Kafka**-da **multi-partition topics** (çoxbölməli mövzular) necə idarə olunur?

### Producer və Consumer
51. **Kafka Producer** (Kafka İstehsalçısı) nədir və necə işləyir?
52. **Kafka Consumer** (Kafka İstehlakçısı) nədir və necə işləyir?
53. **Producer**-də **message batching** (mesaj toplulaşdırması) nədir?
54. **Producer**-də **acks** (təsdiqləmə) parametrləri hansılardır?
55. **Consumer Group**-da **partition assignment** (bölmə təyinatı) necə aparılır?
56. **Consumer**-də **offset management** (ofset idarəetmə) necə təmin olunur?
57. **Kafka**-da **manual offset commit** (əl ilə ofset təsdiqləmə) necə işləyir?
58. **Kafka**-da **auto offset commit** (avtomatik ofset təsdiqləmə) nədir?
59. **Producer**-də **idempotent delivery** (idempotent çatdırılma) nədir?
60. **Producer**-də **transactional producer** (tranzaksiyalı istehsalçı) nədir?
61. **Consumer**-də **seek()** metodu nə üçün istifadə olunur?
62. **Kafka**-da **message key** ilə **message ordering** (mesaj sıralaması) necə təmin olunur?
63. **Consumer Group**-da **rebalancing** (yenidən balanslaşdırma) necə işləyir?
64. **Kafka**-da **at-least-once delivery** (ən azı bir dəfə çatdırılma) necə təmin olunur?
65. **Kafka**-da **at-most-once delivery** (ən çox bir dəfə çatdırılma) necə işləyir?
66. **Kafka**-da **exactly-once delivery** (dəqiq bir dəfə çatdırılma) necə təmin olunur?
67. **Producer**-də **compression.type** parametri nədir?
68. **Consumer**-də **fetch size** (yükləmə ölçüsü) necə təyin olunur?
69. **Kafka**-da **message retry** (mesaj təkrar sınağı) necə konfiqurasiya olunur?
70. **Kafka**-da **dead letter topic** (ölü məktub mövzusu) nədir?

### Kafka Streams
71. **Kafka Streams** nədir və hansı problemləri həll edir?
72. **Kafka Streams** ilə **Kafka Consumer** arasındakı fərq nədir?
73. **KStream** nədir və necə istifadə olunur?
74. **KTable** nədir və necə işləyir?
75. **KStream** ilə **KTable** arasındakı fərq nədir?
76. **GlobalKTable** nədir və nə üçün istifadə olunur?
77. **Kafka Streams DSL** (Domain Specific Language) nədir?
78. **Kafka Streams Processor API** nədir?
79. **Kafka Streams**-də **state store** (vəziyyət anbarı) nədir?
80. **Kafka Streams**-də **windowing** (pəncərələmə) necə işləyir?
81. **Kafka Streams**-də **time windows** (vaxt pəncərələri) hansılardır?
82. **Kafka Streams**-də **session windows** (sessiya pəncərələri) nədir?
83. **Kafka Streams**-də **join** əməliyyatları hansılardır?
84. **Kafka Streams**-də **inner join** necə tətbiq olunur?
85. **Kafka Streams**-də **left join** ilə **outer join** arasındakı fərq nədir?
86. **Kafka Streams**-də **aggregation** (toplama) necə həyata keçirilir?
87. **Kafka Streams**-də **groupBy** ilə **groupByKey** arasındakı fərq nədir?
88. **Kafka Streams**-də **stateful transformations** (vəziyyətli transformasiyalar) nədir?
89. **Kafka Streams**-də **stateless transformations** (vəziyyətsiz transformasiyalar) nədir?
90. **Kafka Streams**-də **exactly-once processing** (dəqiq bir dəfə emal) necə təmin olunur?
91. **Kafka Streams**-də **fault tolerance** (səhvə dözümlülük) necə təmin olunur?
92. **Kafka Streams**-də **state store** ilə **changelog topic** (dəyişiklik jurnalı mövzusu) arasındakı əlaqə nədir?
93. **Kafka Streams**-də **timestamp extractor** (vaxt damğası çıxarıcı) nədir?
94. **Kafka Streams**-də **interactive queries** (interaktiv sorğular) necə həyata keçirilir?
95. **Kafka Streams**-də **stream-table join** (axın-cədvəl birləşməsi) necə işləyir?
96. **Kafka Streams**-də **windowed aggregation** (pəncərəli toplama) necə tətbiq olunur?
97. **Kafka Streams**-də **suppress** operatoru nədir?
98. **Kafka Streams**-də **grace period** (imtiyaz müddəti) nədir?
99. **Kafka Streams**-də **stream processing topology** (axın emal topologiyası) nədir?
100. **Kafka Streams**-də **repartitioning** (yenidən bölüşdürmə) necə işləyir?

### Performans və Optimallaşdırma
101. **Kafka**-da **performance tuning** (performans tənzimləmə) necə aparılır?
102. **Kafka**-da **broker performance** (broker performansı) necə optimallaşdırılır?
103. **Kafka**-da **producer performance** (istehsalçı performansı) necə artır?
104. **Kafka**-da **consumer performance** (istehlakçı performansı) necə optimallaşdırılır?
105. **Kafka**-da **partition count** (bölmə sayı) performansına necə təsir edir?
106. **Kafka**-da **replication factor** performansına necə təsir edir?
107. **Kafka**-da **message compression** performansına necə təsir edir?
108. **Kafka**-da **batch size** (toplu ölçüsü) necə təyin olunur?
109. **Kafka**-da **linger.ms** parametri nədir?
110. **Kafka**-da **buffer.memory** parametri nə üçün istifadə olunur?
111. **Kafka**-da **fetch.max.bytes** parametri necə təsir edir?
112. **Kafka**-da **max.poll.records** parametri nədir?
113. **Kafka**-da **log segment size** (jurnal seqment ölçüsü) necə optimallaşdırılır?
114. **Kafka**-da **log retention** performansına necə təsir edir?
115. **Kafka**-da **log compaction** performansına necə təsir edir?
116. **Kafka Streams**-də **state store** optimallaşdırması necə aparılır?
117. **Kafka Streams**-də **parallel processing** (paralel emal) necə təmin olunur?
118. **Kafka**-da **network I/O** (şəbəkə giriş/çıxış) necə optimallaşdırılır?
119. **Kafka**-da **disk I/O** (disk giriş/çıxış) necə idarə olunur?
120. **Kafka**-da **CPU usage** (prosessor istifadəsi) necə optimallaşdırılır?

### Təhlükəsizlik
121. **Kafka**-da **authentication** (autentifikasiya) necə konfiqurasiya olunur?
122. **Kafka**-da **authorization** (səlahiyyətləndirmə) necə təmin olunur?
123. **Kafka**-da **SSL/TLS** şifrələməsi necə aktivləşdirilir?
124. **Kafka**-da **SASL** (Simple Authentication and Security Layer) nədir?
125. **Kafka**-da **Kerberos** ilə autentifikasiya necə tətbiq olunur?
126. **Kafka**-da **ACLs** (Access Control Lists - Giriş Nəzarət Siyahıları) nədir?
127. **Kafka**-da **encryption at rest** (sabit vəziyyətdə şifrələmə) necə təmin olunur?
128. **Kafka**-da **message encryption** (mesaj şifrələməsi) necə həyata keçirilir?
129. **Kafka**-da **network security** (şəbəkə təhlükəsizliyi) necə təmin olunur?
130. **Kafka**-da **audit logging** (audit qeydiyyatı) necə aktivləşdirilir?
131. **Kafka**-da **message spoofing** (mesaj saxtalaşdırması) necə qarşısı alınır?
132. **Kafka**-da **message replay** (mesaj təkrar oynatma) hücumlarına qarşı necə qorunulur?
133. **Kafka**-da **role-based access control** (rol əsaslı giriş nəzarəti) necə tətbiq olunur?
134. **Kafka**-da **firewall** konfiqurasiyası necə aparılır?
135. **Kafka**-da **secure communication** (təhlükəsiz rabitə) üçün hansı protokollar istifadə olunur?

### Clustering və Yüksək Əlçatanlıq
136. **Kafka Cluster** (Kafka Klasteri) necə konfiqurasiya olunur?
137. **Kafka**-da **replication** (təkrarlanma) necə təmin olunur?
138. **Kafka**-da **high availability** (yüksək əlçatanlıq) necə təmin olunur?
139. **Kafka**-da **failover** (əks funksionallıq) necə idarə olunur?
140. **Kafka**-da **partition leader election** (bölmə lideri seçimi) necə işləyir?
141. **Kafka**-da **Zookeeper** ilə klaster idarəetməsi necə aparılır?
142. **Kafka**-da **broker failure** (broker sıradan çıxması) zamanı mesajlar necə qorunur?
143. **Kafka**-da **replica lag** (replika gecikməsi) necə idarə olunur?
144. **Kafka**-da **ISR** (In-Sync Replicas) ilə **replication** arasındakı fərq nədir?
145. **Kafka**-da **dynamic cluster expansion** (dinamik klaster genişlənməsi) necə aparılır?
146. **Kafka**-da **partition reassignment** ilə klaster balanslaşdırması necə təmin olunur?
147. **Kafka**-da **network partitioning** (şəbəkə bölünməsi) necə idarə olunur?
148. **Kafka**-da **controller failover** (kontroller əks funksionallığı) necə işləyir?
149. **Kafka**-da **quorum-based replication** (kvorum əsaslı təkrarlanma) nədir?
150. **Kafka**-da **Zookeeper ensemble** (Zookeeper ansamblı) necə konfiqurasiya olunur?

### Spring ilə İnteqrasiya
151. **Spring Kafka** ilə Kafka inteqrasiyası necə həyata keçirilir?
152. **Spring Boot** ilə Kafka necə konfiqurasiya olunur?
153. **Spring Cloud Stream** ilə Kafka inteqrasiyası nədir?
154. **@KafkaListener** annotasiyası nədir və necə istifadə olunur?
155. **KafkaTemplate** sinfi nədir və necə işləyir?
156. **Spring Kafka**-da **message converter** (mesaj çeviricisi) necə təyin olunur?
157. **Spring Boot**-da **Kafka consumer** (Kafka istehlakçısı) necə yaradılır?
158. **Spring Kafka**-da **retry mechanism** (təkrar sınaq mexanizmi) necə konfiqurasiya olunur?
159. **Spring Cloud Stream**-də **Kafka binder** (Kafka bağlayıcısı) nədir?
160. **Spring Kafka**-da **message acknowledgment** (mesaj təsdiqləmə) necə idarə olunur?
161. **Spring Boot**-da **Kafka dead letter topic** (ölü məktub mövzusu) necə konfiqurasiya olunur?
162. **Spring Kafka**-da **error handling** (səhv idarəetmə) necə həyata keçirilir?
163. **Spring Cloud Stream**-də **consumer groups** (istehlakçı qrupları) necə istifadə olunur?
164. **Spring Boot**-da **Kafka topic creation** (mövzu yaratma) necə aparılır?
165. **Spring Kafka**-da **message serialization** (mesaj seriyalaşdırması) necə aparılır?
166. **Spring Kafka**-da **message deserialization** (mesaj deserializasiyası) necə təmin olunur?
167. **Spring Cloud Stream**-də **partitioning** (bölüşdürmə) necə həyata keçirilir?
168. **Spring Kafka**-da **transactional producer** necə konfiqurasiya olunur?
169. **Spring Boot**-da **Kafka Streams** ilə inteqrasiya necə aparılır?
170. **Spring Kafka**-da **interactive queries** necə tətbiq olunur?

### Digər Mövzular
171. **Kafka Connect** nədir və necə istifadə olunur?
172. **Kafka Connect Source Connector** (Mənbə Konnektoru) nədir?
173. **Kafka Connect Sink Connector** (Çıxış Konnektoru) nədir?
174. **Kafka MirrorMaker** nədir və necə işləyir?
175. **Kafka**-da **schema registry** (sxem reyestri) nədir?
176. **Kafka**-da **Avro serialization** (Avro seriyalaşdırması) necə tətbiq olunur?
177. **Kafka**-da **message versioning** (mesaj versiyalaşdırma) necə idarə olunur?
178. **Kafka**-da **message deduplication** (mesaj təkrarlanmasının qarşısını alma) necə təmin olunur?
179. **Kafka**-da **message ordering** (mesaj sıralaması) necə təmin olunur?
180. **Kafka**-da **message filtering** (mesaj süzgəcləmə) necə həyata keçirilir?
181. **Kafka**-da **message transformation** (mesaj transformasiyası) necə aparılır?
182. **Kafka**-da **message validation** (mesaj doğrulaması) necə tətbiq olunur?
183. **Kafka**-da **message logging** (mesaj qeydiyyatı) necə konfiqurasiya olunur?
184. **Kafka**-da **message tracing** (mesaj izləmə) necə həyata keçirilir?
185. **Kafka**-da **distributed tracing** (paylanmış izləmə) necə tətbiq olunur?
186. **Kafka**-da **OpenTelemetry** ilə inteqrasiya necə aparılır?
187. **Kafka**-da **Prometheus** ilə monitorinq necə qurulur?
188. **Kafka**-da **Grafana** ilə vizualizasiya necə təmin olunur?
189. **Kafka**-da **health checks** (sağlamlıq yoxlamaları) necə konfiqurasiya olunur?
190. **Kafka**-da **metrics** (metrikalar) hansılardır və necə toplanır?
191. **Kafka**-da **JMX** (Java Management Extensions) ilə monitorinq necə aparılır?
192. **Kafka**-da **log aggregation** (qeyd toplama) necə həyata keçirilir?
193. **Kafka**-da **ELK Stack** (Elasticsearch, Logstash, Kibana) ilə inteqrasiya necə aparılır?
194. **Kafka**-da **message retry policies** (mesaj təkrar sınaq siyasətləri) necə təyin olunur?
195. **Kafka**-da **message expiration** (mesaj müddəti bitməsi) necə idarə olunur?
196. **Kafka**-da **message priority** (mesaj prioriteti) necə təyin olunur?
197. **Kafka**-da **message batch processing** (mesaj toplu emalı) necə aparılır?
198. **Kafka**-da **message compression types** (mesaj sıxışdırma növləri) hansılardır?
199. **Kafka**-da **message delivery semantics** (mesaj çatdırılma semantikası) nədir?
200. **Kafka**-da **message idempotency** (mesaj idempotentliyi) necə təmin olunur?
201. **Kafka**-da **message headers** (mesaj başlıqları) nədir və necə istifadə olunur?
202. **Kafka**-da **message properties** (mesaj xassələri) hansılardır?
203. **Kafka**-da **message validation** ilə **message filtering** arasındakı fərq nədir?
204. **Kafka**-da **message transformation** ilə **message filtering** arasındakı fərq nədir?
205. **Kafka**-da **message logging** ilə **message tracing** arasındakı fərq nədir?
206. **Kafka**-da **message deduplication** ilə **message idempotency** arasındakı fərq nədir?
207. **Kafka**-da **message versioning** ilə **message transformation** arasındakı fərq nədir?
208. **Kafka**-da **message ordering** ilə **message delivery** arasındakı fərq nədir?
209. **Kafka**-da **message compression** ilə **message batching** arasındakı fərq nədir?
210. **Kafka**-da **message retry** ilə **message redelivery** arasındakı fərq nədir?
211. **Kafka**-da **message expiration** ilə **log retention** arasındakı fərq nədir?
212. **Kafka**-da **message priority** ilə **partition priority** arasındakı fərq nədir?
213. **Kafka**-da **consumer group rebalancing** ilə **partition reassignment** arasındakı fərq nədir?
214. **Kafka**-da **log compaction** ilə **log retention** arasındakı fərq nədir?
215. **Kafka**-da **broker configuration** ilə **topic configuration** arasındakı fərq nədir?
216. **Kafka**-da **Zookeeper** ilə **Kafka Controller** arasındakı fərq nədir?
217. **Kafka**-da **producer acks** ilə **consumer acknowledgment** arasındakı fərq nədir?
218. **Kafka**-da **message key** ilə **partition key** arasındakı fərq nədir?
219. **Kafka**-da **message compression** ilə **log compaction** arasındakı fərq nədir?
220. **Kafka**-da **message serialization** ilə **message transformation** arasındakı fərq nədir?
221. **Kafka**-da **message validation** ilə **message deduplication** arasındakı fərq nədir?
222. **Kafka**-da **message logging** ilə **audit logging** arasındakı fərq nədir?
223. **Kafka**-da **message tracing** ilə **distributed tracing** arasındakı fərq nədir?
224. **Kafka**-da **message delivery guarantees** ilə **message persistence** arasındakı fərq nədir?
225. **Kafka**-da **message idempotency** ilə **message versioning** arasındakı fərq nədir?
226. **Kafka**-da **message filtering** ilə **message routing** arasındakı fərq nədir?
227. **Kafka**-da **message batching** ilə **message serialization** arasındakı fərq nədir?
228. **Kafka**-da **message prefetch** ilə **message acknowledgment** arasındakı fərq nədir?
229. **Kafka**-da **message retry** ilə **message expiration** arasındakı fərq nədir?
230. **Kafka**-da **consumer priorities** ilə **partition priorities** arasındakı fərq nədir?
231. **Kafka**-da **Kafka Connect** ilə **Kafka Streams** arasındakı fərq nədir?
232. **Kafka**-da **schema registry** ilə **message serialization** arasındakı fərq nədir?
233. **Kafka**-da **Avro** ilə **JSON** seriyalaşdırması arasındakı fərq nədir?
234. **Kafka**-da **message deduplication** ilə **log compaction** arasındakı fərq nədir?
235. **Kafka**-da **message ordering** ilə **partition ordering** arasındakı fərq nədir?
236. **Kafka**-da **message filtering** ilə **message validation** arasındakı fərq nədir?
237. **Kafka**-da **message transformation** ilə **message serialization** arasındakı fərq nədir?
238. **Kafka**-da **message logging** ilə **message validation** arasındakı fərq nədir?
239. **Kafka**-da **message tracing** ilə **message logging** arasındakı fərq nədir?
240. **Kafka**-da **message delivery guarantees** ilə **message acknowledgment** arasındakı fərq nədir?
241. **Kafka**-da **message idempotency** ilə **message deduplication** arasındakı fərq nədir?
242. **Kafka**-da **message versioning** ilə **message filtering** arasındakı fərq nədir?
243. **Kafka**-da **message routing** ilə **message delivery** arasındakı fərq nədir?
244. **Kafka**-da **message batching** ilə **message compression** arasındakı fərq nədir?
245. **Kafka**-da **message prefetch** ilə **message redelivery** arasındakı fərq nədir?
246. **Kafka**-da **message retry** ilə **message acknowledgment** arasındakı fərq nədir?
247. **Kafka**-da **message expiration** ilə **message validation** arasındakı fərq nədir?
248. **Kafka**-da **consumer group rebalancing** ilə **partition balancing** arasındakı fərq nədir?
249. **Kafka**-da **log compaction** ilə **message retention** arasındakı fərq nədir?
250. **Kafka**-da **broker configuration** ilə **consumer configuration** arasındakı fərq nədir?
251. **Kafka**-da **Zookeeper** ilə **Kafka Streams** arasındakı fərq nədir?
252. **Kafka**-da **producer acks** ilə **message delivery guarantees** arasındakı fərq nədir?
253. **Kafka**-da **message key** ilə **message headers** arasındakı fərq nədir?
254. **Kafka**-da **message compression** ilə **message serialization** arasındakı fərq nədir?
255. **Kafka**-da **message validation** ilə **message transformation** arasındakı fərq nədir?
256. **Kafka**-da **message logging** ilə **message tracing** arasındakı fərq nədir?
257. **Kafka**-da **message deduplication** ilə **message filtering** arasındakı fərq nədir?
258. **Kafka**-da **message versioning** ilə **message routing** arasındakı fərq nədir?
259. **Kafka**-da **message batching** ilə **message prefetch** arasındakı fərq nədir?
260. **Kafka**-da **message retry** ilə **message redelivery** arasındakı fərq nədir?
261. **Kafka**-da **message expiration** ilə **log retention** arasındakı fərq nədir?
262. **Kafka**-da **consumer priorities** ilə **message priorities** arasındakı fərq nədir?
263. **Kafka**-da **Kafka Connect** ilə **Kafka MirrorMaker** arasındakı fərq nədir?
264. **Kafka**-da **schema registry** ilə **Avro serialization** arasındakı fərq nədir?
265. **Kafka**-da **message deduplication** ilə **message idempotency** arasındakı fərq nədir?
266. **Kafka**-da **message ordering** ilə **message filtering** arasındakı fərq nədir?
267. **Kafka**-da **message transformation** ilə **message validation** arasındakı fərq nədir?
268. **Kafka**-da **message logging** ilə **audit logging** arasındakı fərq nədir?
269. **Kafka**-da **message tracing** ilə **distributed tracing** arasındakı fərq nədir?
270. **Kafka**-da **message delivery guarantees** ilə **message persistence** arasındakı fərq nədir?
271. **Kafka**-da **message idempotency** ilə **message versioning** arasındakı fərq nədir?
272. **Kafka**-da **message filtering** ilə **message routing** arasındakı fərq nədir?
273. **Kafka**-da **message batching** ilə **message serialization** arasındakı fərq nədir?
274. **Kafka**-da **message prefetch** ilə **message acknowledgment** arasındakı fərq nədir?
275. **Kafka**-da **message retry** ilə **message expiration** arasındakı fərq nədir?
276. **Kafka**-da **consumer priorities** ilə **partition priorities** arasındakı fərq nədir?
277. **Kafka**-da **Kafka Connect** ilə **Spring Cloud Stream** arasındakı fərq nədir?
278. **Kafka**-da **schema registry** ilə **message validation** arasındakı fərq nədir?
279. **Kafka**-da **Avro** ilə **Protobuf** seriyalaşdırması arasındakı fərq nədir?
280. **Kafka**-da **message deduplication** ilə **log compaction** arasındakı fərq nədir?
281. **Kafka**-da **message ordering** ilə **partition ordering** arasındakı fərq nədir?
282. **Kafka**-da **message filtering** ilə **message transformation** arasındakı fərq nədir?
283. **Kafka**-da **message logging** ilə **message validation** arasındakı fərq nədir?
284. **Kafka**-da **message tracing** ilə **message logging** arasındakı fərq nədir?
285. **Kafka**-da **message delivery guarantees** ilə **message acknowledgment** arasındakı fərq nədir?
286. **Kafka**-da **message idempotency** ilə **message deduplication** arasındakı fərq nədir?
287. **Kafka**-da **message versioning** ilə **message filtering** arasındakı fərq nədir?
288. **Kafka**-da **message routing** ilə **message delivery** arasındakı fərq nədir?
289. **Kafka**-da **message batching** ilə **message compression** arasındakı fərq nədir?
290. **Kafka**-da **message prefetch** ilə **message redelivery** arasındakı fərq nədir?
291. **Kafka**-da **message retry** ilə **message acknowledgment** arasındakı fərq nədir?
292. **Kafka**-da **message expiration** ilə **message validation** arasındakı fərq nədir?
293. **Kafka**-da **consumer group rebalancing** ilə **partition balancing** arasındakı fərq nədir?
294. **Kafka**-da **log compaction** ilə **message retention** arasındakı fərq nədir?
295. **Kafka**-da **broker configuration** ilə **consumer configuration** arasındakı fərq nədir?
296. **Kafka**-da **Zookeeper** ilə **Kafka Controller** arasındakı fərq nədir?
297. **Kafka**-da **producer acks** ilə **message delivery guarantees** arasındakı fərq nədir?
298. **Kafka**-da **message key** ilə **message headers** arasındakı fərq nədir?
299. **Kafka**-da **message compression** ilə **message serialization** arasındakı fərq nədir?
300. **Kafka**-da **message validation** ilə **message transformation** arasındakı fərq nədir?

---

# Liquibase Müsahibə Sualları

Bu sənəd Java, Liquibase ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
- [Kafka və Kafka Streams](#kafka-və-kafka-streams)
- [Liquibase](#liquibase)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Changelog və Changeset](#changelog-və-changeset)
  - [Konfiqurasiya və İdarəetmə](#konfiqurasiya-və-idarəetmə)
  - [Spring ilə İnteqrasiya](#spring-ilə-inteqrasiya)
  - [Performans və Best Practices](#performans-və-best-practices)
  - [Digər Mövzular](#digər-mövzular)

## Liquibase

### Ümumi Suallar
1. **Liquibase** nədir və nə üçün istifadə olunur?
2. **Database Migration** (Verilənlər Bazası Miqrasiyası) nədir və Liquibase ilə necə həyata keçirilir?
3. **Liquibase**-in digər migration alətləri ilə (məsələn, Flyway) fərqləri nələrdir?
4. **Liquibase**-in açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?
5. **Liquibase**-in hansı verilənlər bazalarını dəstəklədiyi nədir?
6. **Liquibase**-in əsas xüsusiyyətləri hansılardır?
7. **Liquibase**-in **version control** (versiya nəzarəti) ilə əlaqəsi nədir?
8. **Liquibase**-də **database schema** (verilənlər bazası sxemi) necə idarə olunur?
9. **Liquibase**-in mikroservis arxitekturasında istifadəsi necədir?
10. **Liquibase**-in **continuous integration** (davamlı inteqrasiya) ilə inteqrasiyası necədir?
11. **Liquibase**-in istifadəsində qarşılaşılacaq çətinliklər nələrdir?
12. **Liquibase**-də **database refactoring** (verilənlər bazası yenidənqurma) nədir?
13. **Liquibase**-in **JDBC** ilə əlaqəsi nədir?
14. **Liquibase**-in **SQL-based** və **XML-based** miqrasiyaları arasındakı fərq nədir?
15. **Liquibase**-in **platform independence** (platformadan asılı olmama) xüsusiyyəti nədir?

### Changelog və Changeset
16. **Changelog** (Dəyişiklik Jurnalı) nədir və Liquibase-da rolu nədir?
17. **Changeset** (Dəyişiklik Dəsti) nədir və necə təyin olunur?
18. **Changelog File** (Dəyişiklik Jurnalı Faylı) hansı formatlarda ola bilər (XML, YAML, JSON, SQL)?
19. **Changeset**-də **id**, **author** və **file** atributlarının rolu nədir?
20. **Liquibase**-də **preconditions** (ön şərtlər) nədir və necə istifadə olunur?
21. **Changeset**-də **rollback** (geri qaytarma) necə təyin olunur?
22. **Liquibase**-də **context** (kontekst) nədir və nə üçün istifadə olunur?
23. **Liquibase**-də **labels** (etiketlər) necə istifadə olunur?
24. **Changeset**-də **runAlways** parametri nədir?
25. **Changeset**-də **runOnChange** parametri nədir?
26. **Liquibase**-də **logicalFilePath** atributu nə üçün istifadə olunur?
27. **Changelog**-da **include** və **includeAll** direktivləri nədir?
28. **Liquibase**-də **master changelog** (əsas dəyişiklik jurnalı) necə təyin olunur?
29. **Changeset**-də **failOnError** parametri nədir?
30. **Liquibase**-də **onDuplicate** parametri nə üçün istifadə olunur?
31. **Changeset**-də **runOrder** atributu nədir?
32. **Liquibase**-də **precondition** ilə **context** arasındakı fərq nədir?
33. **Liquibase**-də **changeset checksum** (dəyişiklik dəsti yoxlama cəmi) nədir?
34. **Liquibase**-də **databaseChangeLog** cədvəli nədir?
35. **Liquibase**-də **databaseChangeLogLock** cədvəli nə üçün istifadə olunur?

### Konfiqurasiya və İdarəetmə
36. **Liquibase**-də **database connection** (verilənlər bazası əlaqəsi) necə konfiqurasiya olunur?
37. **Liquibase**-də **properties file** (xassələr faylı) necə istifadə olunur?
38. **Liquibase**-də **JDBC URL** necə təyin olunur?
39. **Liquibase**-də **changeLogSync** əmri nədir?
40. **Liquibase**-də **update** əmri necə işləyir?
41. **Liquibase**-də **rollback** əmri necə istifadə olunur?
42. **Liquibase**-də **rollbackCount** ilə **rollbackToDate** arasındakı fərq nədir?
43. **Liquibase**-də **tagDatabase** əmri nədir?
44. **Liquibase**-də **diff** əmri nə üçün istifadə olunur?
45. **Liquibase**-də **generateChangeLog** əmri nədir?
46. **Liquibase**-də **status** əmri nə edir?
47. **Liquibase**-də **history** əmri necə işləyir?
48. **Liquibase**-də **futureRollbackSQL** əmri nədir?
49. **Liquibase**-də **dropAll** əmri nə üçün istifadə olunur?
50. **Liquibase**-də **validate** əmri nədir?
51. **Liquibase**-də **database schema** ilə **changelog** sinxronizasiyası necə aparılır?
52. **Liquibase**-də **database snapshot** (verilənlər bazası anlıq görüntüsü) necə yaradılır?
53. **Liquibase**-də **custom change** (xüsusi dəyişiklik) necə təyin olunur?
54. **Liquibase**-də **SQL preconditions** (SQL ön şərtləri) necə istifadə olunur?
55. **Liquibase**-də **stored procedures** (saxlanılan prosedurlar) necə miqrasiya edilir?

### Spring ilə İnteqrasiya
56. **Spring Boot** ilə Liquibase inteqrasiyası necə həyata keçirilir?
57. **Spring Boot**-da **liquibase.enabled** xassəsi nədir?
58. **Spring Boot**-da **liquibase.change-log** xassəsi necə təyin olunur?
59. **Spring Boot**-da **Liquibase bean** necə konfiqurasiya olunur?
60. **Spring Boot**-da **Liquibase profiles** (profillər) necə istifadə olunur?
61. **Spring Boot**-da **Liquibase context** (kontekst) necə təyin olunur?
62. **Spring Boot**-da **Liquibase rollback** necə həyata keçirilir?
63. **Spring Boot**-da **Liquibase diff** necə istifadə olunur?
64. **Spring Boot**-da **Liquibase update** əmri necə işləyir?
65. **Spring Boot**-da **Liquibase databaseChangeLog** cədvəli necə idarə olunur?
66. **Spring Boot**-da **Liquibase logging** (qeydiyyat) necə konfiqurasiya olunur?
67. **Spring Boot**-da **Liquibase Maven Plugin** ilə inteqrasiya necə aparılır?
68. **Spring Boot**-da **Liquibase Gradle Plugin** ilə inteqrasiya necə həyata keçirilir?
69. **Spring Boot**-da **Liquibase testing** (testlər) necə aparılır?
70. **Spring Boot**-da **Liquibase H2 database** ilə necə istifadə olunur?
71. **Spring Boot**-da **Liquibase və Hibernate** inteqrasiyası necə təmin olunur?
72. **Spring Boot**-da **Liquibase və JPA** necə birləşdirilir?
73. **Spring Boot**-da **Liquibase preconditions** ilə **Spring profiles** arasındakı əlaqə nədir?
74. **Spring Boot**-da **Liquibase custom change** necə tətbiq olunur?
75. **Spring Boot**-da **Liquibase rollback** ilə **Spring transaction** arasındakı fərq nədir?

### Performans və Best Practices
76. **Liquibase**-də **performance optimization** (performans optimallaşdırması) necə aparılır?
77. **Liquibase**-də **large migrations** (böyük miqrasiyalar) necə idarə olunur?
78. **Liquibase**-də **database locking** (verilənlər bazası kilidlənməsi) necə işləyir?
79. **Liquibase**-də **changeset** sayını azaltmaq üçün hansı strategiyalar istifadə olunur?
80. **Liquibase**-də **rollback performance** (geri qaytarma performansı) necə optimallaşdırılır?
81. **Liquibase**-də **diff performance** (fərq performansı) necə artır?
82. **Liquibase**-də **database schema comparison** (verilənlər bazası sxemi müqayisəsi) necə optimallaşdırılır?
83. **Liquibase**-də **best practices** (ən yaxşı təcrübələr) hansılardır?
84. **Liquibase**-də **changelog versioning** (dəyişiklik jurnalı versiyalaşdırması) necə aparılır?
85. **Liquibase**-də **team collaboration** (komanda əməkdaşlığı) necə təmin olunur?
86. **Liquibase**-də **conflict resolution** (ziddiyyət həlli) necə aparılır?
87. **Liquibase**-də **large datasets** (böyük məlumat dəstləri) ilə miqrasiya necə idarə olunur?
88. **Liquibase**-də **database backup** (verilənlər bazası ehtiyat nüsxəsi) necə aparılır?
89. **Liquibase**-də **performance monitoring** (performans monitorinqi) necə həyata keçirilir?
90. **Liquibase**-də **logging** (qeydiyyat) necə konfiqurasiya olunur?
91. **Liquibase**-də **error handling** (səhv idarəetmə) necə təmin olunur?
92. **Liquibase**-də **schema validation** (sxem doğrulaması) necə aparılır?
93. **Liquibase**-də **migration rollback strategies** (miqrasiya geri qaytarma strategiyaları) hansılardır?
94. **Liquibase**-də **database compatibility** (verilənlər bazası uyğunluğu) necə təmin olunur?
95. **Liquibase**-də **incremental migrations** (addım-addım miqrasiyalar) necə həyata keçirilir?

### Digər Mövzular
96. **Liquibase Maven Plugin** nədir və necə istifadə olunur?
97. **Liquibase Gradle Plugin** nədir və necə konfiqurasiya olunur?
98. **Liquibase**-də **SQL-based changesets** (SQL əsaslı dəyişiklik dəstləri) necə təyin olunur?
99. **Liquibase**-də **XML-based changesets** (XML əsaslı dəyişiklik dəstləri) necə istifadə olunur?
100. **Liquibase**-də **YAML-based changesets** (YAML əsaslı dəyişiklik dəstləri) necə təyin olunur?
101. **Liquibase**-də **JSON-based changesets** (JSON əsaslı dəyişiklik dəstləri) necə işləyir?
102. **Liquibase**-də **custom SQL** (xüsusi SQL) necə tətbiq olunur?
103. **Liquibase**-də **stored procedures migration** (saxlanılan prosedurlar miqrasiyası) necə aparılır?
104. **Liquibase**-də **triggers migration** (tetikleyici miqrasiyası) necə həyata keçirilir?
105. **Liquibase**-də **views migration** (görünüşlər miqrasiyası) necə təmin olunur?
106. **Liquibase**-də **indexes migration** (indekslər miqrasiyası) necə aparılır?
107. **Liquibase**-də **foreign keys migration** (xarici açarlar miqrasiyası) necə idarə olunur?
108. **Liquibase**-də **constraints migration** (məhdudiyyətlər miqrasiyası) necə tətbiq olunur?
109. **Liquibase**-də **database functions migration** (verilənlər bazası funksiyaları miqrasiyası) necə aparılır?
110. **Liquibase**-də **database schema synchronization** (verilənlər bazası sxemi sinxronizasiyası) necə həyata keçirilir?
111. **Liquibase**-də **database diff** ilə **database snapshot** arasındakı fərq nədir?
112. **Liquibase**-də **changelog locking** (dəyişiklik jurnalı kilidlənməsi) necə işləyir?
113. **Liquibase**-də **multi-tenant databases** (çoxkirayəçi verilənlər bazaları) necə idarə olunur?
114. **Liquibase**-də **NoSQL databases** (NoSQL verilənlər bazaları) ilə inteqrasiya necə aparılır?
115. **Liquibase**-də **MongoDB** ilə miqrasiya necə həyata keçirilir?
116. **Liquibase**-də **Cassandra** ilə miqrasiya necə tətbiq olunur?
117. **Liquibase**-də **database versioning** (verilənlər bazası versiyalaşdırması) necə idarə olunur?
118. **Liquibase**-də **changelog merge** (dəyişiklik jurnalı birləşdirmə) necə aparılır?
119. **Liquibase**-də **conditional migrations** (şərtli miqrasiyalar) necə təyin olunur?
120. **Liquibase**-də **database rollback** ilə **database backup** arasındakı fərq nədir?
121. **Liquibase**-də **database testing** (verilənlər bazası testləri) necə aparılır?
122. **Liquibase**-də **Testcontainers** ilə inteqrasiya necə həyata keçirilir?
123. **Liquibase**-də **H2 database** ilə test miqrasiyaları necə aparılır?
124. **Liquibase**-də **database schema validation** (verilənlər bazası sxemi doğrulaması) necə təmin olunur?
125. **Liquibase**-də **database schema documentation** (verilənlər bazası sxemi sənədləşdirmə) necə aparılır?
126. **Liquibase**-də **changelog history** (dəyişiklik jurnalı tarixçəsi) necə idarə olunur?
127. **Liquibase**-də **changelog validation** (dəyişiklik jurnalı doğrulaması) necə həyata keçirilir?
128. **Liquibase**-də **database migration strategies** (verilənlər bazası miqrasiya strategiyaları) hansılardır?
129. **Liquibase**-də **schema drift** (sxem sürüşməsi) necə aşkarlanır?
130. **Liquibase**-də **database schema drift** ilə **changelog** sinxronizasiyası necə aparılır?
131. **Liquibase**-də **custom preconditions** (xüsusi ön şərtlər) necə təyin olunur?
132. **Liquibase**-də **custom change types** (xüsusi dəyişiklik növləri) necə yaradılır?
133. **Liquibase**-də **database-specific changes** (verilənlər bazasına xas dəyişikliklər) necə idarə olunur?
134. **Liquibase**-də **database schema comparison tools** (verilənlər bazası sxemi müqayisə alətləri) nələrdir?
135. **Liquibase**-də **changelog refactoring** (dəyişiklik jurnalı yenidənqurma) necə aparılır?
136. **Liquibase**-də **database schema rollback** (verilənlər bazası sxemi geri qaytarma) necə təmin olunur?
137. **Liquibase**-də **database schema backup** (verilənlər bazası sxemi ehtiyat nüsxəsi) necə aparılır?
138. **Liquibase**-də **database schema testing** (verilənlər bazası sxemi testləri) necə həyata keçirilir?
139. **Liquibase**-də **database schema migration** ilə **data migration** arasındakı fərq nədir?
140. **Liquibase**-də **database schema versioning** (verilənlər bazası sxemi versiyalaşdırması) necə idarə olunur?
141. **Liquibase**-də **changelog conflict resolution** (dəyişiklik jurnalı ziddiyyət həlli) necə aparılır?
142. **Liquibase**-də **database schema synchronization** (verilənlər bazası sxemi sinxronizasiyası) necə təmin olunur?
143. **Liquibase**-də **database schema deployment** (verilənlər bazası sxemi yerləşdirmə) necə aparılır?
144. **Liquibase**-də **database schema monitoring** (verilənlər bazası sxemi monitorinqi) necə həyata keçirilir?
145. **Liquibase**-də **database schema auditing** (verilənlər bazası sxemi audit etmə) necə aparılır?
146. **Liquibase**-də **database schema documentation** ilə **changelog documentation** arasındakı fərq nədir?
147. **Liquibase**-də **database schema validation** ilə **changelog validation** arasındakı fərq nədir?
148. **Liquibase**-də **database schema testing** ilə **database integration testing** arasındakı fərq nədir?
149. **Liquibase**-də **database schema migration** ilə **database schema refactoring** arasındakı fərq nədir?
150. **Liquibase**-də **database schema versioning** ilə **changelog versioning** arasındakı fərq nədir?

---

# GitHub Müsahibə Sualları

Bu sənəd GitHub ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
- [Kafka və Kafka Streams](#kafka-və-kafka-streams)
- [Liquibase](#liquibase)
- [GitHub](#github)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Repository İdarəetmə](#repository-idarəetmə)
  - [Branching və Merging](#branching-və-merging)
  - [Pull Requests və Code Review](#pull-requests-və-code-review)
  - [GitHub Actions](#github-actions)
  - [Təhlükəsizlik](#təhlükəsizlik)
  - [İnteqrasiyalar və API](#inteqrasiyalar-və-api)
  - [Digər Mövzular](#digər-mövzular)

## GitHub

### Ümumi Suallar
1. **GitHub** nədir və nə üçün istifadə olunur?
2. **Git** ilə **GitHub** arasındakı fərq nədir?
3. **GitHub**-un **version control** (versiya nəzarəti) üçün rolu nədir?
4. **GitHub**-un digər platformalarla (Bitbucket, GitLab) fərqləri nələrdir?
5. **GitHub**-un açıq mənbəli (open-source) layihələrdəki üstünlükləri nələrdir?
6. **GitHub Repository** (Anbar) nədir və necə yaradılır?
7. **GitHub**-un **collaboration** (əməkdaşlıq) xüsusiyyətləri hansılardır?
8. **GitHub**-un **cloud-based** (bulud əsaslı) olması nə kimi faydalar təmin edir?
9. **GitHub**-un **enterprise** tətbiqlərdə istifadəsi necədir?
10. **GitHub**-un **open-source community** (açıq mənbəli icma) ilə əlaqəsi nədir?
11. **GitHub**-da **forking** (çəngəlləmə) nədir və nə üçün istifadə olunur?
12. **GitHub**-da **clone** ilə **fork** arasındakı fərq nədir?
13. **GitHub**-un **social coding** (sosial kodlaşdırma) konsepsiyası nədir?
14. **GitHub**-un **continuous integration** (davamlı inteqrasiya) ilə əlaqəsi nədir?
15. **GitHub**-un **DevOps** təcrübələrində rolu nədir?

### Repository İdarəetmə
16. **GitHub Repository** necə yaradılır?
17. **Public Repository** (İctimai Anbar) ilə **Private Repository** (Şəxsi Anbar) arasındakı fərq nədir?
18. **GitHub**-da **repository permissions** (anbar icazələri) necə idarə olunur?
19. **GitHub**-da **collaborators** (əməkdaşlar) necə əlavə olunur?
20. **GitHub**-da **repository settings** (anbar parametrləri) hansılardır?
21. **GitHub**-da **repository deletion** (anbar silinməsi) necə aparılır?
22. **GitHub**-da **repository archiving** (anbar arxivləşdirmə) nədir?
23. **GitHub**-da **repository visibility** (anbar görünürlüyü) necə dəyişdirilir?
24. **GitHub**-da **repository templates** (anbar şablonları) nədir?
25. **GitHub**-da **repository description** (anbar təsviri) necə əlavə olunur?
26. **GitHub**-da **README.md** faylının rolu nədir?
27. **GitHub**-da **LICENSE** faylı nə üçün istifadə olunur?
28. **GitHub**-da **.gitignore** faylı nədir və necə konfiqurasiya olunur?
29. **GitHub**-da **repository stars** (anbar ulduzları) nə üçün istifadə olunur?
30. **GitHub**-da **repository watching** (anbar izləmə) nədir?

### Branching və Merging
31. **Git Branch** (Git Şaxəsi) nədir və necə yaradılır?
32. **GitHub**-da **branching strategy** (şaxələnmə strategiyası) hansılardır?
33. **GitHub Flow** nədir?
34. **Git Flow** ilə **GitHub Flow** arasındakı fərq nədir?
35. **GitHub**-da **protected branches** (qorunan şaxələr) nədir?
36. **GitHub**-da **branch restrictions** (şaxə məhdudiyyətləri) necə təyin olunur?
37. **Git Merge** (Git Birləşdirmə) necə işləyir?
38. **GitHub**-da **merge conflicts** (birləşdirmə ziddiyyətləri) necə həll olunur?
39. **GitHub**-da **rebase** ilə **merge** arasındakı fərq nədir?
40. **GitHub**-da **squash merge** (sıxışdırılmış birləşdirmə) nədir?
41. **GitHub**-da **fast-forward merge** (sürətli irəli birləşdirmə) nədir?
42. **GitHub**-da **merge commit** (birləşdirmə komiti) nədir?
43. **GitHub**-da **branch deletion** (şaxə silinməsi) necə aparılır?
44. **GitHub**-da **default branch** (standart şaxə) necə dəyişdirilir?
45. **GitHub**-da **branch naming conventions** (şaxə adlandırma qaydaları) nələrdir?

### Pull Requests və Code Review
46. **Pull Request** (Çəkmə Sorğusu) nədir və necə yaradılır?
47. **GitHub**-da **Pull Request** ilə **Merge Request** arasındakı fərq nədir?
48. **GitHub**-da **code review** (kod baxışı) necə həyata keçirilir?
49. **GitHub**-da **Pull Request comments** (çəkmə sorğusu şərhləri) necə əlavə olunur?
50. **GitHub**-da **Pull Request approvals** (çəkmə sorğusu təsdiqləri) necə idarə olunur?
51. **GitHub**-da **required reviews** (tələb olunan baxışlar) necə təyin olunur?
52. **GitHub**-da **Pull Request templates** (çəkmə sorğusu şablonları) nədir?
53. **GitHub**-da **draft Pull Request** (qaralama çəkmə sorğusu) nədir?
54. **GitHub**-da **Pull Request conflicts** (çəkmə sorğusu ziddiyyətləri) necə həll olunur?
55. **GitHub**-da **Pull Request labels** (çəkmə sorğusu etiketləri) nə üçün istifadə olunur?
56. **GitHub**-da **Pull Request milestones** (çəkmə sorğusu mərhələləri) nədir?
57. **GitHub**-da **Pull Request assignees** (çəkmə sorğusu təyinatçıları) necə təyin olunur?
58. **GitHub**-da **Pull Request reviewers** (çəkmə sorğusu baxışçıları) necə seçilir?
59. **GitHub**-da **auto-merge** (avtomatik birləşdirmə) nədir?
60. **GitHub**-da **Pull Request status checks** (çəkmə sorğusu status yoxlamaları) nədir?

### GitHub Actions
61. **GitHub Actions** nədir və nə üçün istifadə olunur?
62. **GitHub Actions Workflow** (GitHub Actions İş Axını) nədir?
63. **GitHub Actions**-da **workflow file** (iş axını faylı) necə təyin olunur?
64. **GitHub Actions**-da **jobs** (tapşırıqlar) nədir?
65. **GitHub Actions**-da **steps** (addımlar) necə işləyir?
66. **GitHub Actions**-da **actions** (hərəkətlər) nədir?
67. **GitHub Actions**-da **triggers** (tetikleyicilər) hansılardır?
68. **GitHub Actions**-da **on.push** tətikleyicisi nədir?
69. **GitHub Actions**-da **on.pull_request** tətikleyicisi nədir?
70. **GitHub Actions**-da **matrix builds** (matris qurulmaları) nədir?
71. **GitHub Actions**-da **secrets** (sirlər) necə idarə olunur?
72. **GitHub Actions**-da **environment variables** (mühit dəyişənləri) necə təyin olunur?
73. **GitHub Actions**-da **self-hosted runners** (özüyerləşdirilən icraçıları) nədir?
74. **GitHub Actions**-da **Docker containers** (Docker konteynerləri) necə istifadə olunur?
75. **GitHub Actions**-da **caching dependencies** (asılılıqların keşlənməsi) necə aparılır?
76. **GitHub Actions**-da **workflow_dispatch** tətikleyicisi nədir?
77. **GitHub Actions**-da **schedule** tətikleyicisi nədir?
78. **GitHub Actions**-da **artifacts** (artefaktlar) necə idarə olunur?
79. **GitHub Actions**-da **status badges** (status nişanları) nədir?
80. **GitHub Actions**-da **CI/CD** (Continuous Integration/Continuous Deployment) necə qurulur?

### Təhlükəsizlik
81. **GitHub**-da **repository permissions** (anbar icazələri) necə təhlükəsiz idarə olunur?
82. **GitHub**-da **two-factor authentication** (iki faktorlu autentifikasiya) necə aktivləşdirilir?
83. **GitHub**-da **dependabot** nədir və necə işləyir?
84. **GitHub**-da **code scanning** (kod skan etmə) nədir?
85. **GitHub**-da **secret scanning** (sirlərin skan edilməsi) nədir?
86. **GitHub**-da **security advisories** (təhlükəsizlik xəbərdarlıqları) nədir?
87. **GitHub**-da **vulnerability alerts** (zəiflik xəbərdarlıqları) necə idarə olunur?
88. **GitHub**-da **branch protection rules** (şaxə qoruma qaydaları) necə təyin olunur?
89. **GitHub**-da **commit signing** (komit imzalama) necə həyata keçirilir?
90. **GitHub**-da **GPG keys** (GPG açarları) necə istifadə olunur?
91. **GitHub**-da **SSH keys** (SSH açarları) necə konfiqurasiya olunur?
92. **GitHub**-da **access tokens** (giriş tokenləri) nədir?
93. **GitHub**-da **personal access tokens** (şəxsi giriş tokenləri) necə yaradılır?
94. **GitHub**-da **security policies** (təhlükəsizlik siyasətləri) necə təyin olunur?
95. **GitHub**-da **dependabot security updates** (dependabot təhlükəsizlik yeniləmələri) nədir?

### İnteqrasiyalar və API
96. **GitHub API** nədir və necə istifadə olunur?
97. **GitHub REST API** ilə **GitHub GraphQL API** arasındakı fərq nədir?
98. **GitHub**-da **webhooks** (veb çəngəlləri) nədir və necə konfiqurasiya olunur?
99. **GitHub**-da **GitHub Apps** nədir?
100. **GitHub**-da **OAuth Apps** ilə **GitHub Apps** arasındakı fərq nədir?
101. **GitHub**-da **API rate limiting** (API sürət məhdudlaşdırması) necə idarə olunur?
102. **GitHub**-da **third-party integrations** (üçüncü tərəf inteqrasiyaları) hansılardır?
103. **GitHub**-da **Jenkins** ilə inteqrasiya necə aparılır?
104. **GitHub**-da **Travis CI** ilə inteqrasiya necə həyata keçirilir?
105. **GitHub**-da **CircleCI** ilə inteqrasiya necə qurulur?
106. **GitHub**-da **Slack** ilə inteqrasiya necə aparılır?
107. **GitHub**-da **JIRA** ilə inteqrasiya necə həyata keçirilir?
108. **GitHub**-da **Docker Hub** ilə inteqrasiya necə qurulur?
109. **GitHub**-da **AWS CodePipeline** ilə inteqrasiya necə aparılır?
110. **GitHub**-da **GitHub Marketplace** nədir?

### Digər Mövzular
111. **GitHub Issues** nədir və necə istifadə olunur?
112. **GitHub Projects** nədir və necə idarə olunur?
113. **GitHub Wiki** nədir və nə üçün istifadə olunur?
114. **GitHub Pages** nədir və necə qurulur?
115. **GitHub**-da **markdown** faylları necə istifadə olunur?
116. **GitHub**-da **commit history** (komit tarixçəsi) necə idarə olunur?
117. **GitHub**-da **commit message conventions** (komit mesaj qaydaları) nələrdir?
118. **GitHub**-da **git blame** necə istifadə olunur?
119. **GitHub**-da **git stash** ilə dəyişikliklər necə saxlanılır?
120. **GitHub**-da **git cherry-pick** nədir?
121. **GitHub**-da **git rebase interactive** (interaktiv yenidən bazalaşdırma) nədir?
122. **GitHub**-da **git bisect** ilə səhvlər necə tapılır?
123. **GitHub**-da **git reflog** nədir və necə istifadə olunur?
124. **GitHub**-da **submodules** (alt modullar) nədir və necé istifadə olunur?
125. **GitHub**-da **git hooks** (git çəngəlləri) nədir?
126. **GitHub**-da **pre-commit hooks** (ön komit çəngəlləri) necə konfiqurasiya olunur?
127. **GitHub**-da **code owners** (kod sahibləri) nədir və necə təyin olunur?
128. **GitHub**-da **repository rulesets** (anbar qaydaları dəsti) nədir?
129. **GitHub**-da **issue templates** (məsələ şablonları) nədir?
130. **GitHub**-da **discussion** (müzakirə) xüsusiyyəti nədir?
131. **GitHub**-da **team management** (komanda idarəetməsi) necə aparılır?
132. **GitHub**-da **organization** (təşkilat) necə yaradılır?
133. **GitHub**-da **organization roles** (təşkilat rolları) nədir?
134. **GitHub**-da **team permissions** (komanda icazələri) necə idarə olunur?
135. **GitHub**-da **repository insights** (anbar anlayışları) nədir?
136. **GitHub**-da **traffic analytics** (trafik analitikası) necə istifadə olunur?
137. **GitHub**-da **dependency graph** (asılılıq qrafiki) nədir?
138. **GitHub**-da **code frequency** (kod tezliyi) necə analiz edilir?
139. **GitHub**-da **contributor statistics** (iştirakçı statistikası) necə əldə olunur?
140. **GitHub**-da **GitHub Sponsors** nədir?
141. **GitHub**-da **GitHub Packages** nədir və necə istifadə olunur?
142. **GitHub**-da **Docker images** (Docker şəkilləri) necə yayımlanır?
143. **GitHub**-da **Maven packages** (Maven paketləri) necə idarə olunur?
144. **GitHub**-da **npm packages** (npm paketləri) necə yayımlanır?
145. **GitHub**-da **GitHub Desktop** nədir və necə istifadə olunur?
146. **GitHub**-da **GitHub CLI** nədir və necə konfiqurasiya olunur?
147. **GitHub**-da **GitHub Codespaces** nədir?
148. **GitHub**-da **dependabot version updates** (dependabot versiya yeniləmələri) nədir?
149. **GitHub**-da **repository insights** ilə **traffic analytics** arasındakı fərq nədir?
150. **GitHub**-da **code review** ilə **Pull Request review** arasındakı fərq nədir?

---

# Docker Müsahibə Sualları

Bu sənəd Docker ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
- [Kafka və Kafka Streams](#kafka-və-kafka-streams)
- [Liquibase](#liquibase)
- [GitHub](#github)
- [Docker](#docker)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Images və Containers](#images-və-containers)
  - [Dockerfile](#dockerfile)
  - [Networking](#networking)
  - [Storage](#storage)
  - [Docker Compose](#docker-compose)
  - [Security](#security)
  - [Orchestration](#orchestration)
  - [CI/CD İnteqrasiyası](#ci-cd-inteqrasiyası)
  - [Digər Mövzular](#digər-mövzular)

## Docker

### Ümumi Suallar
1. **Docker** nədir və nə üçün istifadə olunur?
2. **Containerization** (Konteynerləşdirmə) nədir və virtual maşınlardan fərqi nədir?
3. **Docker**-ın **Kubernetes** ilə fərqi nədir?
4. **Docker**-ın açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?
5. **Docker**-ın **DevOps** təcrübələrində rolu nədir?
6. **Docker**-ın mikroservis arxitekturasında istifadəsi necədir?
7. **Docker**-ın əsas xüsusiyyətləri hansılardır?
8. **Docker Engine** nədir və necə işləyir?
9. **Docker Hub** nədir və nə üçün istifadə olunur?
10. **Docker**-ın **container orchestration** (konteyner orkestrasiyası) ilə əlaqəsi nədir?
11. **Docker**-ın **lightweight** (yüngül) olmasının faydaları nələrdir?
12. **Docker**-ın **portability** (daşıma qabiliyyəti) necə təmin olunur?
13. **Docker**-ın digər konteyner texnologiyaları ilə fərqləri nələrdir?
14. **Docker**-ın **cloud integration** (bulud inteqrasiyası) imkanları nələrdir?
15. **Docker**-ın **continuous deployment** (davamlı yerləşdirmə) ilə əlaqəsi nədir?

### Images və Containers
16. **Docker Image** (Docker Şəkli) nədir və necə yaradılır?
17. **Docker Container** (Docker Konteyneri) nədir və necə işləyir?
18. **Docker Image** ilə **Docker Container** arasındakı fərq nədir?
19. **Docker Image Layers** (Docker Şəkil Qatları) nədir?
20. **Docker**-da **image tagging** (şəkil etiketləmə) necə aparılır?
21. **Docker**-da **image versioning** (şəkil versiyalaşdırma) necə idarə olunur?
22. **Docker**-da **base image** (əsas şəkil) nədir?
23. **Docker**-da **multi-stage builds** (çoxmərhələli qurmalar) nədir?
24. **Docker**-da **image pruning** (şəkil təmizləmə) necə aparılır?
25. **Docker**-da **container lifecycle** (konteyner həyat dövrü) hansı mərhələlərdən ibarətdir?
26. **Docker**-da **docker run** komandası nə edir?
27. **Docker**-da **docker build** komandası necə işləyir?
28. **Docker**-da **docker pull** komandası nədir?
29. **Docker**-da **docker push** komandası nə üçün istifadə olunur?
30. **Docker**-da **docker commit** ilə şəkil necə yaradılır?

### Dockerfile
31. **Dockerfile** nədir və necə yazılır?
32. **Dockerfile**-da **FROM** direktivi nə üçün istifadə olunur?
33. **Dockerfile**-da **RUN** ilə **CMD** arasındakı fərq nədir?
34. **Dockerfile**-da **ENTRYPOINT** nədir və necə istifadə olunur?
35. **Dockerfile**-da **COPY** ilə **ADD** arasındakı fərq nədir?
36. **Dockerfile**-da **WORKDIR** direktivi nə edir?
37. **Dockerfile**-da **EXPOSE** direktivi nə üçün istifadə olunur?
38. **Dockerfile**-da **ENV** direktivi necə istifadə olunur?
39. **Dockerfile**-da **ARG** ilə **ENV** arasındakı fərq nədir?
40. **Dockerfile**-da **VOLUME** direktivi nədir?
41. **Dockerfile**-da **USER** direktivi nə üçün istifadə olunur?
42. **Dockerfile**-da **LABEL** direktivi nədir?
43. **Dockerfile**-da **HEALTHCHECK** direktivi necə işləyir?
44. **Dockerfile**-da **ONBUILD** direktivi nədir?
45. **Dockerfile**-da **multi-stage builds** necə tətbiq olunur?
46. **Dockerfile**-da **best practices** (ən yaxşı təcrübələr) hansılardır?
47. **Dockerfile**-da **image size optimization** (şəkil ölçüsü optimallaşdırması) necə aparılır?
48. **Dockerfile**-da **caching** (keşləmə) necə işləyir?
49. **Dockerfile**-da **build context** (qurma konteksti) nədir?
50. **Dockerfile**-da **ignore files** (.dockerignore) nə üçün istifadə olunur?

### Networking
51. **Docker Networking** (Docker Şəbəkəsi) nədir?
52. **Docker**-da **bridge network** (körpü şəbəkəsi) necə işləyir?
53. **Docker**-da **host network** (ev sahibi şəbəkəsi) nədir?
54. **Docker**-da **overlay network** (örtük şəbəkəsi) nədir?
55. **Docker**-da **none network** (heç bir şəbəkə) nədir?
56. **Docker**-da **user-defined networks** (istifadəçi tərəfindən təyin edilmiş şəbəkələr) necə yaradılır?
57. **Docker**-da **port mapping** (port xəritələşdirmə) necə tətbiq olunur?
58. **Docker**-da **container-to-container communication** (konteynerdən-konteynerə rabitə) necə təmin olunur?
59. **Docker**-da **DNS resolution** (DNS həlli) necə işləyir?
60. **Docker**-da **network driver** (şəbəkə sürücüsü) nədir?
61. **Docker**-da **bridge network** ilə **overlay network** arasındakı fərq nədir?
62. **Docker**-da **network alias** (şəbəkə ləqəbi) nədir?
63. **Docker**-da **external network access** (xarici şəbəkə girişi) necə təmin olunur?
64. **Docker**-da **network performance** (şəbəkə performansı) necə optimallaşdırılır?
65. **Docker**-da **network isolation** (şəbəkə izolyasiyası) necə tətbiq olunur?

### Storage
66. **Docker**-da **volume** (həcm) nədir və necə istifadə olunur?
67. **Docker**-da **bind mount** (bağlama nöqtəsi) nədir?
68. **Docker**-da **tmpfs mount** (müvəqqəti fayl sistemi bağlaması) nədir?
69. **Docker Volume** ilə **Bind Mount** arasındakı fərq nədir?
70. **Docker**-da **volume driver** (həcm sürücüsü) nədir?
71. **Docker**-da **persistent storage** (davamlı saxlama) necə təmin olunur?
72. **Docker**-da **volume backup** (həcm ehtiyat nüsxəsi) necə aparılır?
73. **Docker**-da **volume sharing** (həcm paylaşımı) necə həyata keçirilir?
74. **Docker**-da **storage performance** (saxlama performansı) necə optimallaşdırılır?
75. **Docker**-da **volume pruning** (həcm təmizləmə) necə aparılır?
76. **Docker**-da **named volumes** (adlandırılmış həcmlər) nədir?
77. **Docker**-da **anonymous volumes** (anonim həcmlər) nədir?
78. **Docker**-da **volume plugins** (həcm plaginləri) necə istifadə olunur?
79. **Docker**-da **data persistence** (məlumat davamlılığı) necə təmin olunur?
80. **Docker**-da **volume lifecycle** (həcm həyat dövrü) necə idarə olunur?

### Docker Compose
81. **Docker Compose** nədir və nə üçün istifadə olunur?
82. **docker-compose.yml** faylı necə yazılır?
83. **Docker Compose**-da **services** (xidmətlər) nədir?
84. **Docker Compose**-da **networks** (şəbəkələr) necə təyin olunur?
85. **Docker Compose**-da **volumes** (həcmlər) necə konfiqurasiya olunur?
86. **Docker Compose**-da **depends_on** direktivi nədir?
87. **Docker Compose**-da **environment variables** (mühit dəyişənləri) necə təyin olunur?
88. **Docker Compose**-da **ports** (portlar) necə xəritələşdirilir?
89. **Docker Compose**-da **build** direktivi nədir?
90. **Docker Compose**-da **profiles** (profillər) nədir?
91. **Docker Compose**-da **docker-compose up** komandası nə edir?
92. **Docker Compose**-da **docker-compose down** komandası nədir?
93. **Docker Compose**-da **scaling** (miqyaslandırma) necə həyata keçirilir?
94. **Docker Compose**-da **healthcheck** necə təyin olunur?
95. **Docker Compose**-da **extends** direktivi nədir?

### Security
96. **Docker**-da **container security** (konteyner təhlükəsizliyi) necə təmin olunur?
97. **Docker**-da **user namespaces** (istifadəçi ad məkanları) nədir?
98. **Docker**-da **rootless containers** (kök olmayan konteynerlər) nədir?
99. **Docker**-da **image scanning** (şəkil skan etmə) necə aparılır?
100. **Docker**-da **vulnerability scanning** (zəiflik skan etmə) necə həyata keçirilir?
101. **Docker**-da **Docker Content Trust** (Docker Məzmun Etibarı) nədir?
102. **Docker**-da **image signing** (şəkil imzalama) necë tətbiq olunur?
103. **Docker**-da **security best practices** (təhlükəsizlik ən yaxşı təcrübələri) hansılardır?
104. **Docker**-da **privileged containers** (imtiyazlı konteynerlər) nədir?
105. **Docker**-da **AppArmor** ilə təhlükəsizlik necə təmin olunur?
106. **Docker**-da **SELinux** ilə təhlükəsizlik necə tətbiq olunur?
107. **Docker**-da **resource limits** (resurs məhdudiyyətləri) necə təyin olunur?
108. **Docker**-da **network security** (şəbəkə təhlükəsizliyi) necə təmin olunur?
109. **Docker**-da **secrets management** (sirlər idarəetməsi) necə həyata keçirilir?
110. **Docker**-da **container isolation** (konteyner izolyasiyası) necə təmin olunur?

### Orchestration
111. **Docker Swarm** nədir və necə işləyir?
112. **Docker Swarm** ilə **Kubernetes** arasındakı fərq nədir?
113. **Docker Swarm**-da **services** (xidmətlər) necə təyin olunur?
114. **Docker Swarm**-da **overlay network** necə istifadə olunur?
115. **Docker Swarm**-da **service scaling** (xidmət miqyaslandırması) necə aparılır?
116. **Docker Swarm**-da **node management** (düyün idarəetməsi) necə həyata keçirilir?
117. **Docker Swarm**-da **leader election** (lider seçimi) necə işləyir?
118. **Docker Swarm**-da **service discovery** (xidmət kəşfi) necə təmin olunur?
119. **Docker Swarm**-da **load balancing** (yük balanslaşdırması) necə aparılır?
120. **Docker Swarm**-da **rolling updates** (sürüşən yeniləmələr) necə həyata keçirilir?
121. **Docker**-da **Kubernetes integration** (Kubernetes inteqrasiyası) necə aparılır?
122. **Docker**-da **container orchestration** (konteyner orkestrasiyası) nə üçün vacibdir?
123. **Docker**-da **service health checks** (xidmət sağlamlıq yoxlamaları) necə təyin olunur?
124. **Docker Swarm**-da **secrets** (sirlər) necə idarə olunur?
125. **Docker Swarm**-da **stack deployment** (yığın yerləşdirmə) necə aparılır?

### CI/CD İnteqrasiyası
126. **Docker**-da **CI/CD** (Continuous Integration/Continuous Deployment) necə qurulur?
127. **Docker**-da **GitHub Actions** ilə inteqrasiya necə həyata keçirilir?
128. **Docker**-da **Jenkins** ilə CI/CD necə qurulur?
129. **Docker**-da **GitLab CI** ilə inteqrasiya necə aparılır?
130. **Docker**-da **CircleCI** ilə inteqrasiya necə tətbiq olunur?
131. **Docker**-da **Docker Hub** ilə avtomatlaşdırılmış qurmalar necə konfiqurasiya olunur?
132. **Docker**-da **image scanning** CI/CD-də necə istifadə olunur?
133. **Docker**-da **multi-stage builds** CI/CD-də necə tətbiq olunur?
134. **Docker**-da **container registry** (konteyner reyestri) necə inteqrasiya olunur?
135. **Docker**-da **AWS ECR** (Elastic Container Registry) ilə inteqrasiya necə aparılır?
136. **Docker**-da **Azure Container Registry** ilə inteqrasiya necə həyata keçirilir?
137. **Docker**-da **Google Container Registry** ilə inteqrasiya necə tətbiq olunur?
138. **Docker**-da **blue-green deployment** (mavi-yaşıl yerləşdirmə) necə aparılır?
139. **Docker**-da **canary deployment** (kanarya yerləşdirmə) necə həyata keçirilir?
140. **Docker**-da **rolling deployment** (sürüşən yerləşdirmə) necə təmin olunur?

### Digər Mövzular
141. **Docker CLI** (Docker Komanda Xətti İnterfeysi) nədir və necə istifadə olunur?
142. **Docker**-da **docker ps** komandası nə edir?
143. **Docker**-da **docker logs** komandası nə üçün istifadə olunur?
144. **Docker**-da **docker inspect** komandası nədir?
145. **Docker**-da **docker exec** komandası necə işləyir?
146. **Docker**-da **docker stop** ilə **docker kill** arasındakı fərq nədir?
147. **Docker**-da **docker rm** ilə **docker rmi** arasındakı fərq nədir?
148. **Docker**-da **docker system prune** komandası nə edir?
149. **Docker**-da **docker info** komandası hansı məlumatları göstərir?
150. **Docker**-da **docker stats** komandası nə üçün istifadə olunur?
151. **Docker**-da **container monitoring** (konteyner monitorinqi) necə həyata keçirilir?
152. **Docker**-da **Prometheus** ilə monitorinq necə qurulur?
153. **Docker**-da **Grafana** ilə vizualizasiya necə təmin olunur?
154. **Docker**-da **log aggregation** (qeyd toplama) necə aparılır?
155. **Docker**-da **ELK Stack** (Elasticsearch, Logstash, Kibana) ilə inteqrasiya necə həyata keçirilir?
156. **Docker**-da **health monitoring** (sağlamlıq monitorinqi) necə təmin olunur?
157. **Docker**-da **resource monitoring** (resurs monitorinqi) necə aparılır?
158. **Docker**-da **container logging** (konteyner qeydiyyatı) necə konfiqurasiya olunur?
159. **Docker**-da **log drivers** (qeyd sürücüləri) hansılardır?
160. **Docker**-da **JSON logging** (JSON qeydiyyatı) necə tətbiq olunur?
161. **Docker**-da **multi-container applications** (çoxkonteynerli tətbiqlər) necə idarə olunur?
162. **Docker**-da **container restart policies** (konteyner yenidən başlatma siyasətləri) nələrdir?
163. **Docker**-da **container healthcheck** ilə **application healthcheck** arasındakı fərq nədir?
164. **Docker**-da **container debugging** (konteyner sazlama) necə aparılır?
165. **Docker**-da **container resource limits** (konteyner resurs məhdudiyyətləri) necə təyin olunur?
166. **Docker**-da **CPU limits** (prosessor məhdudiyyətləri) necə konfiqurasiya olunur?
167. **Docker**-da **memory limits** (yaddaş məhdudiyyətləri) necə təyin olunur?
168. **Docker**-da **container orchestration** ilə **container management** arasındakı fərq nədir?
169. **Docker**-da **container lifecycle management** (konteyner həyat dövrü idarəetməsi) necə aparılır?
170. **Docker**-da **container snapshot** (konteyner anlıq görüntüsü) necə yaradılır?
171. **Docker**-da **image optimization** (şəkil optimallaşdırması) necə həyata keçirilir?
172. **Docker**-da **container isolation** ilə **container security** arasındakı fərq nədir?
173. **Docker**-da **container networking** ilə **host networking** arasındakı fərq nədir?
174. **Docker**-da **volume management** ilə **bind mounts** arasındakı fərq nədir?
175. **Docker**-da **Docker Compose** ilə **Docker Swarm** arasındakı fərq nədir?
176. **Docker**-da **container logging** ilə **application logging** arasındakı fərq nədir?
177. **Docker**-da **container monitoring** ilə **application monitoring** arasındakı fərq nədir?
178. **Docker**-da **container healthcheck** ilə **Docker Swarm healthcheck** arasındakı fərq nədir?
179. **Docker**-da **container debugging** ilə **application debugging** arasındakı fərq nədir?
180. **Docker**-da **container resource limits** ilə **container orchestration** arasındakı fərq nədir?
181. **Docker**-da **image versioning** ilə **container versioning** arasındakı fərq nədir?
182. **Docker**-da **image scanning** ilə **container scanning** arasındakı fərq nədir?
183. **Docker**-da **image optimization** ilə **container optimization** arasındakı fərq nədir?
184. **Docker**-da **Docker Hub** ilə **private container registry** arasındakı fərq nədir?
185. **Docker**-da **Docker CLI** ilə **Docker API** arasındakı fərq nədir?
186. **Docker**-da **container orchestration** ilə **container scheduling** (konteyner planlaşdırma) arasındakı fərq nədir?
187. **Docker**-da **container logging** ilə **log aggregation** arasındakı fərq nədir?
188. **Docker**-da **container monitoring** ilə **resource monitoring** arasındakı fərq nədir?
189. **Docker**-da **container healthcheck** ilə **application healthcheck** arasındakı fərq nədir?
190. **Docker**-da **container debugging** ilə **container logging** arasındakı fərq nədir?
191. **Docker**-da **container resource limits** ilə **container performance optimization** arasındakı fərq nədir?
192. **Docker**-da **image versioning** ilə **image tagging** arasındakı fərq nədir?
193. **Docker**-da **image scanning** ilə **vulnerability scanning** arasındakı fərq nədir?
194. **Docker**-da **image optimization** ilə **multi-stage builds** arasındakı fərq nədir?
195. **Docker**-da **Docker Compose** ilə **Kubernetes YAML** arasındakı fərq nədir?
196. **Docker**-da **container networking** ilə **overlay networking** arasındakı fərq nədir?
197. **Docker**-da **volume management** ilə **container storage** arasındakı fərq nədir?
198. **Docker**-da **container orchestration** ilə **Docker Swarm** arasındakı fərq nədir?
199. **Docker**-da **container logging** ilə **Docker Compose logging** arasındakı fərq nədir?
200. **Docker**-da **container monitoring** ilə **Docker Swarm monitoring** arasındakı fərq nədir?

---

# Java, Hibernate, Spring Boot, Data Structures/Collections, Design Patterns, Algorithms, RabbitMQ, Kafka/Kafka Streams, Liquibase, GitHub, Docker və Redis Müsahibə Sualları

Bu sənəd Java, Hibernate, Spring Boot, Data Structures/Collections, Design Patterns, Algorithms, RabbitMQ, Kafka/Kafka Streams, Liquibase, GitHub, Docker və Redis ilə bağlı müsahibə suallarının başlıqlarını əhatə edir. Suallar hər bir mövzunun əsas və qabaqcıl aspektlərini başdan sona əhatə edir.

## Mündəricat
- [Core Java](#ümumi-suallar)
- [Hibernate](#hibernate)
- [Spring Boot](#spring-boot)
- [Data Structures və Collections](#data-structures-və-collections)
- [Design Patterns](#design-patterns)
- [Algorithms](#algorithms)
- [RabbitMQ](#rabbitmq)
- [Kafka və Kafka Streams](#kafka-və-kafka-streams)
- [Liquibase](#liquibase)
- [GitHub](#github)
- [Docker](#docker)
- [Redis](#redis)
  - [Ümumi Suallar](#ümumi-suallar)
  - [Data Structures](#data-structures)
  - [Persistence](#persistence)
  - [Pub/Sub](#pub-sub)
  - [Clustering](#clustering)
  - [Performans və Optimallaşdırma](#performans-və-optimallaşdırma)
  - [Təhlükəsizlik](#təhlükəsizlik)
  - [Spring ilə İnteqrasiya](#spring-ilə-inteqrasiya)
  - [Digər Mövzular](#digər-mövzular)

## Redis

### Ümumi Suallar
1. **Redis** nədir və nə üçün istifadə olunur?
2. **In-memory Database** (Yaddaşda Verilənlər Bazası) nədir və Redis-in rolu nədir?
3. **Redis**-in digər verilənlər bazaları ilə (məsələn, Memcached) fərqləri nələrdir?
4. **Redis**-in açıq mənbəli (open-source) olmasının üstünlükləri nələrdir?
5. **Redis**-in **NoSQL** verilənlər bazası kimi xüsusiyyətləri nələrdir?
6. **Redis**-in mikroservis arxitekturasında istifadəsi necədir?
7. **Redis**-in əsas xüsusiyyətləri hansılardır?
8. **Redis**-in **key-value store** (açar-dəyər anbarı) kimi rolu nədir?
9. **Redis**-in **caching** (keşləmə) üçün istifadəsi necədir?
10. **Redis**-in **real-time applications** (real vaxt tətbiqləri) üçün faydaları nələrdir?
11. **Redis**-in **single-threaded** (tək axınlı) arxitekturası nədir?
12. **Redis**-in **event-driven** (hadisə yönümlü) modeldən istifadəsi necədir?
13. **Redis**-in **data persistence** (məlumat davamlılığı) xüsusiyyətləri nələrdir?
14. **Redis**-in **high availability** (yüksək əlçatanlıq) təminatı necədir?
15. **Redis**-in **scalability** (miqyaslılıq) imkanları nələrdir?

### Data Structures
16. **Redis**-də **String** data strukturu nədir və necə istifadə olunur?
17. **Redis**-də **List** data strukturu nədir?
18. **Redis**-də **Set** data strukturu nədir və necə işləyir?
19. **Redis**-də **Sorted Set** (Sıralanmış Dəst) nədir?
20. **Redis**-də **Hash** data strukturu nədir?
21. **Redis**-də **Bitmap** nədir və necə istifadə olunur?
22. **Redis**-də **HyperLogLog** nədir?
23. **Redis**-də **Geo** data strukturu nədir və necə işləyir?
24. **Redis**-də **Stream** data strukturu nədir?
25. **Redis**-də **String** ilə **Hash** data strukturları arasındakı fərq nədir?
26. **Redis**-də **Set** ilə **Sorted Set** arasındakı fərq nədir?
27. **Redis**-də **List** ilə **Stream** arasındakı fərq nədir?
28. **Redis**-də **HyperLogLog** ilə **Set** arasındakı fərq nədir?
29. **Redis**-də **Bitmap** ilə **Set** arasındakı fərq nədir?
30. **Redis**-də **Geo** data strukturu ilə geolokasiya əməliyyatları necə aparılır?

### Persistence
31. **Redis Persistence** (Redis Davamlılığı) nədir?
32. **Redis**-də **RDB** (Redis Database Backup) nədir və necə işləyir?
33. **Redis**-də **AOF** (Append-Only File) nədir?
34. **Redis**-də **RDB** ilə **AOF** arasındakı fərq nədir?
35. **Redis**-də **hybrid persistence** (hibrid davamlılıq) nədir?
36. **Redis**-də **RDB snapshot** (RDB anlıq görüntüsü) necə yaradılır?
37. **Redis**-də **AOF rewrite** (AOF yenidən yazma) nədir?
38. **Redis**-də **persistence configuration** (davamlılıq konfiqurasiyası) necə təyin olunur?
39. **Redis**-də **fsync** parametri nədir və necə təsir edir?
40. **Redis**-də **persistence performance** (davamlılıq performansı) necə optimallaşdırılır?
41. **Redis**-də **data loss** (məlumat itirilməsi) riski necə azaldılır?
42. **Redis**-də **backup** (ehtiyat nüsxə) necə aparılır?
43. **Redis**-də **restore** (bərpa) necə həyata keçirilir?
44. **Redis**-də **RDB compression** (RDB sıxışdırması) necə işləyir?
45. **Redis**-də **AOF compaction** (AOF sıxışdırması) necə tətbiq olunur?

### Pub/Sub
46. **Redis Pub/Sub** (Nəşr/Abunə) nədir və necə işləyir?
47. **Redis**-də **publish** (nəşr) komandası nədir?
48. **Redis**-də **subscribe** (abunə) komandası nədir?
49. **Redis**-də **Pub/Sub channels** (nəşr/abunə kanalları) necə təyin olunur?
50. **Redis**-də **pattern-based subscription** (nümunə əsaslı abunə) nədir?
51. **Redis Pub/Sub** ilə **Redis Streams** arasındakı fərq nədir?
52. **Redis Pub/Sub**-də **message delivery guarantees** (mesaj çatdırılma zəmanətləri) nədir?
53. **Redis Pub/Sub**-də **scalability** (miqyaslılıq) necə təmin olunur?
54. **Redis Pub/Sub**-də **message persistence** (mesaj davamlılığı) mümkünmü?
55. **Redis Pub/Sub**-də **channel management** (kanal idarəetməsi) necə aparılır?
56. **Redis Pub/Sub**-də **message filtering** (mesaj süzgəcləmə) necə həyata keçirilir?
57. **Redis Pub/Sub**-də **high throughput** (yüksək ötürmə qabiliyyəti) necə təmin olunur?
58. **Redis Pub/Sub**-də **low latency** (aşağı gecikmə) necə əldə olunur?
59. **Redis Pub/Sub**-də **message ordering** (mesaj sıralaması) necə təmin olunur?
60. **Redis Pub/Sub**-də **message retry** (mesaj təkrar sınağı) necə idarə olunur?

### Clustering
61. **Redis Cluster** (Redis Klasteri) nədir və necə konfiqurasiya olunur?
62. **Redis**-də **sharding** (bölüşdürmə) necə işləyir?
63. **Redis Cluster**-də **hash slots** (xəş yuvaları) nədir?
64. **Redis Cluster**-də **replication** (təkrarlanma) necə təmin olunur?
65. **Redis Cluster**-də **master-slave** (usta-qul) arxitekturası nədir?
66. **Redis Cluster**-də **failover** (əks funksionallıq) necə işləyir?
67. **Redis Sentinel** nədir və necə konfiqurasiya olunur?
68. **Redis Sentinel** ilə **Redis Cluster** arasındakı fərq nədir?
69. **Redis Cluster**-də **node addition** (düyün əlavə etmə) necə aparılır?
70. **Redis Cluster**-də **node removal** (düyün silinmə) necə həyata keçirilir?
71. **Redis Cluster**-də **resharding** (yenidən bölüşdürmə) necə tətbiq olunur?
72. **Redis Cluster**-də **slot migration** (yuva miqrasiyası) nədir?
73. **Redis Cluster**-də **high availability** (yüksək əlçatanlıq) necə təmin olunur?
74. **Redis Cluster**-də **consistency** (tutarlılıq) necə idarə olunur?
75. **Redis Cluster**-də **network partitioning** (şəbəkə bölünməsi) necə idarə olunur?

### Performans və Optimallaşdırma
76. **Redis**-də **performance tuning** (performans tənzimləmə) necə aparılır?
77. **Redis**-də **latency** (gecikmə) necə azaldılır?
78. **Redis**-də **throughput** (ötürmə qabiliyyəti) necə artır?
79. **Redis**-də **memory optimization** (yaddaş optimallaşdırması) necə həyata keçirilir?
80. **Redis**-də **maxmemory** parametri nədir?
81. **Redis**-də **eviction policies** (çıxarılma siyasətləri) hansılardır?
82. **Redis**-də **LRU eviction** (Son İstifadə Olunan Çıxarılma) necə işləyir?
83. **Redis**-də **TTL** (Time To Live - Yaşama Müddəti) necə təyin olunur?
84. **Redis**-də **memory fragmentation** (yaddaş fraqmentasiyası) necə idarə olunur?
85. **Redis**-də **pipelining** (boru xətti) nədir və performansa necə təsir edir?
86. **Redis**-də **batch operations** (toplu əməliyyatlar) necə tətbiq olunur?
87. **Redis**-də **multi/exec** komandaları nədir?
88. **Redis**-də **lua scripting** (lua skriptləri) performansı necə artır?
89. **Redis**-də **connection pooling** (əlaqə hovuzu) necə optimallaşdırılır?
90. **Redis**-də **command latency** (komanda gecikməsi) necə ölçülür?

### Təhlükəsizlik
91. **Redis**-də **authentication** (autentifikasiya) necə konfiqurasiya olunur?
92. **Redis**-də **password protection** (şifrə qoruması) necə təyin olunur?
93. **Redis**-də **SSL/TLS** şifrələməsi necə aktivləşdirilir?
94. **Redis**-də **access control lists (ACLs)** (giriş nəzarət siyahıları) nədir?
95. **Redis**-də **user management** (istifadəçi idarəetmə) necə aparılır?
96. **Redis**-də **network security** (şəbəkə təhlükəsizliyi) necə təmin olunur?
97. **Redis**-də **encryption at rest** (sabit vəziyyətdə şifrələmə) necə tətbiq olunur?
98. **Redis**-də **data encryption** (məlumat şifrələməsi) necə həyata keçirilir?
99. **Redis**-də **audit logging** (audit qeydiyyatı) necə aktivləşdirilir?
100. **Redis**-də **firewall** konfiqurasiyası necə aparılır?
101. **Redis**-də **command restrictions** (komanda məhdudiyyətləri) necə təyin olunur?
102. **Redis**-də **secure communication** (təhlükəsiz rabitə) necə təmin olunur?
103. **Redis**-də **role-based access control** (rol əsaslı giriş nəzarəti) necə tətbiq olunur?
104. **Redis**-də **data exposure** (məlumat ifşası) riski necə azaldılır?
105. **Redis**-də **vulnerability scanning** (zəiflik skan etmə) necə aparılır?

### Spring ilə İnteqrasiya
106. **Spring Data Redis** nədir və necə istifadə olunur?
107. **Spring Boot** ilə Redis inteqrasiyası necə həyata keçirilir?
108. **Spring Data Redis**-də **RedisTemplate** sinfi nədir?
109. **Spring Boot**-da **Redis caching** (Redis keşləmə) necə konfiqurasiya olunur?
110. **Spring Boot**-da **@Cacheable** annotasiyası Redis ilə necə istifadə olunur?
111. **Spring Data Redis**-də **RedisRepository** nədir?
112. **Spring Boot**-da **Redis Pub/Sub** necə tətbiq olunur?
113. **Spring Data Redis**-də **message listener** (mesaj dinləyicisi) necə konfiqurasiya olunur?
114. **Spring Boot**-da **Redis connection pooling** (əlaqə hovuzu) necə təyin olunur?
115. **Spring Data Redis**-də **Redis serialization** (Redis seriyalaşdırması) necə idarə olunur?
116. **Spring Boot**-da **Redis Sentinel** ilə inteqrasiya necə aparılır?
117. **Spring Boot**-da **Redis Cluster** ilə inteqrasiya necə həyata keçirilir?
118. **Spring Data Redis**-də **Redis transactions** (Redis tranzaksiyaları) necə tətbiq olunur?
119. **Spring Boot**-da **Redis Lua scripting** necə istifadə olunur?
120. **Spring Boot**-da **Redis monitoring** (Redis monitorinqi) necə qurulur?

### Digər Mövzular
121. **Redis CLI** (Redis Komanda Xətti İnterfeysi) nədir və necə istifadə olunur?
122. **Redis**-də **SET** ilə **SETNX** komandaları arasındakı fərq nədir?
123. **Redis**-də **EXPIRE** ilə **SETEX** komandaları arasındakı fərq nədir?
124. **Redis**-də **INCR** və **DECR** komandaları nə üçün istifadə olunur?
125. **Redis**-də **MULTI/EXEC** ilə tranzaksiyalar necə idarə olunur?
126. **Redis**-də **Lua scripting** nədir və necə tətbiq olunur?
127. **Redis**-də **EVAL** komandası nədir?
128. **Redis**-də **pipeline** ilə **batch operations** arasındakı fərq nədir?
129. **Redis**-də **SCAN** komandası nədir və necə istifadə olunur?
130. **Redis**-də **KEYS** ilə **SCAN** arasındakı fərq nədir?
131. **Redis**-də **TTL** ilə **PERSIST** komandaları nədir?
132. **Redis**-də **ZSET** ilə **SET** arasındakı fərq nədir?
133. **Redis**-də **GEOADD** ilə geolokasiya əməliyyatları necə aparılır?
134. **Redis**-də **XADD** ilə Stream əməliyyatları necə tətbiq olunur?
135. **Redis**-də **XREAD** ilə **XREADGROUP** arasındakı fərq nədir?
136. **Redis**-də **Streams consumer groups** (axın istehlakçı qrupları) nədir?
137. **Redis**-də **Bloom Filter** necə tətbiq olunur?
138. **Redis**-də **Cuckoo Filter** nədir?
139. **Redis**-də **Time Series** modulu nədir?
140. **Redis**-də **JSON** modulu necə istifadə olunur?
141. **Redis**-də **Search** modulu nədir?
142. **Redis**-də **Graph** modulu necə işləyir?
143. **Redis**-də **Redis Modules** (Redis Modulları) necə əlavə olunur?
144. **Redis**-də **monitoring** (monitorinq) necə həyata keçirilir?
145. **Redis**-də **INFO** komandası hansı məlumatları göstərir?
146. **Redis**-də **SLOWLOG** komandası nədir?
147. **Redis**-də **MONITOR** komandası nə üçün istifadə olunur?
148. **Redis**-də **Prometheus** ilə monitorinq necə qurulur?
149. **Redis**-də **Grafana** ilə vizualizasiya necə təmin olunur?
150. **Redis**-də **log aggregation** (qeyd toplama) necə aparılır?
151. **Redis**-də **ELK Stack** (Elasticsearch, Logstash, Kibana) ilə inteqrasiya necə həyata keçirilir?
152. **Redis**-də **backup and restore** (ehtiyat nüsxə və bərpa) necə aparılır?
153. **Redis**-də **data migration** (məlumat miqrasiyası) necə həyata keçirilir?
154. **Redis**-də **replication lag** (təkrarlanma gecikməsi) necə idarə olunur?
155. **Redis**-də **eviction policies** ilə **TTL** arasındakı fərq nədir?
156. **Redis**-də **memory usage** (yaddaş istifadəsi) necə ölçülür?
157. **Redis**-də **memory fragmentation** ilə **memory optimization** arasındakı fərq nədir?
158. **Redis**-də **pipelining** ilə **multi/exec** arasındakı fərq nədir?
159. **Redis**-də **Lua scripting** ilə **batch operations** arasındakı fərq nədir?
160. **Redis**-də **Pub/Sub** ilə **Streams** arasındakı fərq nədir?
161. **Redis**-də **Bloom Filter** ilə **HyperLogLog** arasındakı fərq nədir?
162. **Redis**-də **Geo** ilə **ZSET** arasındakı fərq nədir?
163. **Redis**-də **Time Series** modulu ilə **Streams** arasındakı fərq nədir?
164. **Redis**-də **JSON** modulu ilə **Hash** arasındakı fərq nədir?
165. **Redis**-də **Search** modulu ilə **ZSET** arasındakı fərq nədir?
166. **Redis**-də **Graph** modulu ilə **Set** arasındakı fərq nədir?
167. **Redis**-də **persistence** ilə **replication** arasındakı fərq nədir?
168. **Redis**-də **Sentinel** ilə **Cluster** arasındakı fərq nədir?
169. **Redis**-də **eviction** ilə **expiration** arasındakı fərq nədir?
170. **Redis**-də **Pub/Sub** ilə **message queuing** (mesaj növbələmə) arasındakı fərq nədir?
171. **Redis**-də **Lua scripting** ilə **transactions** arasındakı fərq nədir?
172. **Redis**-də **monitoring** ilə **logging** arasındakı fərq nədir?
173. **Redis**-də **backup** ilə **persistence** arasındakı fərq nədir?
174. **Redis**-də **data migration** ilə **replication** arasındakı fərq nədir?
175. **Redis**-də **memory optimization** ilə **eviction policies** arasındakı fərq nədir?
176. **Redis**-də **pipelining** ilə **connection pooling** arasındakı fərq nədir?
177. **Redis**-də **Pub/Sub** ilə **Kafka Pub/Sub** arasındakı fərq nədir?
178. **Redis**-də **Streams** ilə **Kafka Streams** arasındakı fərq nədir?
179. **Redis**-də **Bloom Filter** ilə **Cuckoo Filter** arasındakı fərq nədir?
180. **Redis**-də **Time Series** ilə **ZSET** arasındakı fərq nədir?
181. **Redis**-də **JSON** ilə **String** arasındakı fərq nədir?
182. **Redis**-də **Search** ilə **Geo** arasındakı fərq nədir?
183. **Redis**-də **Graph** ilə **Hash** arasındakı fərq nədir?
184. **Redis**-də **persistence** ilə **backup** arasındakı fərq nədir?
185. **Redis**-də **replication** ilə **clustering** arasındakı fərq nədir?
186. **Redis**-də **eviction** ilə **TTL** arasındakı fərq nədir?
187. **Redis**-də **Pub/Sub** ilə **Streams** arasındakı fərq nədir?
188. **Redis**-də **Lua scripting** ilə **multi/exec** arasındakı fərq nədir?
189. **Redis**-də **monitoring** ilə **performance tuning** arasındakı fərq nədir?
190. **Redis**-də **data migration** ilə **data backup** arasındakı fərq nədir?
191. **Redis**-də **memory optimization** ilə **data compression** arasındakı fərq nədir?
192. **Redis**-də **pipelining** ilə **batch processing** arasındakı fərq nədir?
193. **Redis**-də **Pub/Sub** ilə **message queuing** arasındakı fərq nədir?
194. **Redis**-də **Streams** ilə **List** arasındakı fərq nədir?
195. **Redis**-də **Bloom Filter** ilə **Set** arasındakı fərq nədir?
196. **Redis**-də **Cuckoo Filter** ilə **HyperLogLog** arasındakı fərq nədir?
197. **Redis**-də **Time Series** ilə **Hash** arasındakı fərq nədir?
198. **Redis**-də **JSON** ilə **ZSET** arasındakı fərq nədir?
199. **Redis**-də **Search** ilə **Sorted Set** arasındakı fərq nədir?
200. **Redis**-də **Graph** ilə **List** arasındakı fərq nədir?
