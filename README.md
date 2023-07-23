# dotnet-7-temel-console-app-egitimi-btk-akademi
Egitmen sadık turan eşliginde kodlama egitimi


//if else kullanımı
//var name = "Cuma köse";
//var username = "admin";
//var password = "admin";
//if (username == "admin")
//    if (password == "admin")
//        Console.WriteLine($"hoş geldin {name}");
//    else Console.WriteLine("Parola dogru degil");
//else Console.WriteLine("Kullanıcı adı dogru degil");

//for kullanımı
//Console.Write("Başlangıç : ");
//var baslangic = Convert.ToInt32(Console.ReadLine());
//Console.Write("Bitiş : ");
//var bitis = Convert.ToInt32(Console.ReadLine());
//Console.Write("artış miktarı : ");
//var artis = Convert.ToInt32(Console.ReadLine());
//var toplam = 0;
//for (var i = baslangic; i < bitis; i = i + artis)
//{
//    toplam += i;
//}
//Console.WriteLine(toplam);

//string[] names = {"ali","veli","can","cihan","ahmet"};
//for (int i = 0; i < names.Length; i++)
//{
//    Console.WriteLine(names[i]);
//}


//for (int num = 0; num < 10; num++)
//{
//    Console.WriteLine(num);
//}

//while kullanımı
//var number = 0;
//while (number < 10)
//{
//    Console.WriteLine(number);
//    number++;
//}


//var secim = "e";
//var sayac = 1;
//var toplam = 0;
//while (secim=="e")
//{
//    Console.Write($"{sayac}. sayı: ");
//    toplam += Convert.ToInt32(Console.ReadLine());
//    Console.Write("devam etmek istiyor musunuz ? (e/h) ");
//    secim = Console.ReadLine();
//    sayac++;
//}
//Console.WriteLine($"{sayac-1} adet sayının toplamı: {toplam}");


//break & continue kullanımı
//var name = "Cuma Köse";
//for (var i = 0; i < name.Length; i++)
//{
//    if (name[i] == 'ö')
//        //continue; //atlatma işlemi yapar görmezden gelir devam eder
//        break; // döngüyü sonlandırır
//    Console.WriteLine(name[i]);
//}


//var x = 0;
//while (x<5)
//{
//    //eger if gibi koşul kullanılacak ise ve contunie kullanılacak ise x arttırma işlemi while içerisinde tepede tanımlanmalıdır ki devam edebilsin.
//    x++;
//    if (x == 3)
//        continue;
//    Console.WriteLine(x);
//}

//var rnd = new Random();
//int tutulan = rnd.Next(1, 100);
//int hak = 3;
//while (hak > 0)
//{
//    Console.WriteLine(tutulan);
//    Console.Write("sayı : ");
//    int sayi = Convert.ToInt32(Console.ReadLine());
//    hak--;

//    if (sayi == tutulan)
//    {
//        Console.WriteLine("Tebrikler kazandınız");
//        break;
//    }
//    else
//    {
//        if (tutulan > sayi)
//        {
//            Console.WriteLine("yukarı");
//        }
//        else
//        {
//            Console.WriteLine("aşagı");
//        }
//        if (hak == 0)
//        {
//            Console.WriteLine("Üzgünüm kazanamadın hakkın bitti");
//            break;
//        }
//    }
//}

//do-while kullanımı
//Console.Write("adet: ");
//int adet = Convert.ToInt32(Console.ReadLine());

//string[] urunler = new string[adet];
//int num = 0;
//do
//{
//    Console.Write(" ürün adı : ");
//    urunler[num] = Console.ReadLine() ?? "";
//    num++;
//} while (adet != num);

//Console.WriteLine("ürünler listeleniyor.");

//for (int i = 0; i < urunler.Length; i++)
//{
//    Console.WriteLine(urunler[i]);
//}

//string ad = "Cuma";
//foreach (var item in ad)
//{
//    Console.WriteLine(item);
//}


//oop Methodlar
//using ConsoleApp1;

//Ogrenci ogrenci1 = new Ogrenci()
//{
//    No = 1,
//    adSoyad = "Memati",
//    sube = "6 / A"
//};
//Ogrenci ogrenci2 = new Ogrenci()
//{
//    No = 2,
//    adSoyad = "Polat",
//    sube = "6 / A"
//}; Ogrenci ogrenci3 = new Ogrenci()
//{
//    No = 3,
//    adSoyad = "Abdulhey",
//    sube = "6 / A"
//};

//Ogrenci[] ogrenciler = { ogrenci1, ogrenci2, ogrenci3 };
//foreach (var item in ogrenciler)
//{
//    string sonuc = item.bilgiYazdir();
//    Console.WriteLine(sonuc);
//}

//namespace ConsoleApp1
//{
//    public class Ogrenci
//    {
//        public int No { get; set; }
//        public string adSoyad { get; set; }
//        public string sube { get; set; }

//        public string bilgiYazdir()
//        {
//            var sonuc = $"{this.No} Numaralı ögrencinin AdSoyad Bilgisi : {this.adSoyad} Sınıfı : {this.sube}";
//            return sonuc;
//        }
//    }
//}


//farklı bir örnek

//var soru1 = new Soru()
//{
//    SoruMetni = "Hangisi programlama dili degildir ?",
//    Secenekler = new string[4] { "Python", "C#", "Java", "Html"},
//    Cevap="Html"
//};
//var soru2 = new Soru()
//{
//    SoruMetni = "Hangisi en popülşer programlama platformudur ?",
//    Secenekler = new string[4] { "Djamgo", "Asp.net", "Spring", "Python"},
//    Cevap = "Python"
//};
//var sorular = new Soru[] { soru1, soru2 };

//foreach (var soru in sorular)
//{
//    Console.WriteLine(soru.SoruMetni);
//    foreach (var secenek in soru.Secenekler)
//    {
//        Console.WriteLine(secenek);
//    }

//    Console.Write("cevabınız : ");
//    var cevap = Console.ReadLine();
//    if (soru.cevapKontrol(cevap))
//        Console.WriteLine("dogru cevap");
//    else
//        Console.WriteLine($"yanlış cevap dogrusu ({soru.Cevap})");
//}
//public class Soru
//{
//    public string SoruMetni { get; set; }
//    public string[] Secenekler { get; set; }
//    public string Cevap { get; set; }

//    public bool cevapKontrol(string cevap)
//    {
//        return this.Cevap.ToLower() == cevap;
//    }
//}

