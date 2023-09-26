# SwiftEnumerationKonuAnlatimi
Swift programlama dilinde, "enumeration" veya kısaltmasıyla "enum" olarak adlandırılan bir tür bulunur. Enumerations, 
benzer türdeki değerleri gruplamak ve organize etmek için kullanılır. Bir enum, özellikle sabit değerlerin kullanılması gereken 
durumlarda çok işlevseldir. İşte Swift'te enumeration (enum) hakkında daha fazla bilgi:

Temel Enum Tanımı:

Bir enumeration, anahtar kelime "enum" kullanılarak tanımlanır. Örnek bir enum tanımı:

enum HaftaninGunleri {
    case pazartesi
    case sali
    case carsamba
    case persembe
    case cuma
    case cumartesi
    case pazar
}

Bu örnekte, HaftaninGunleri adında bir enum tanımlanmıştır ve bu enum, haftanın günlerini temsil eden değerleri içerir.

Enum Değerlerine Erişim:

Enum içindeki değerlere erişmek için, enum adı ve değerin adını kullanabilirsiniz. Örnek:

var gun = HaftaninGunleri.cuma
print(gun) // Output: cuma

Enum Switch İfadesi:

Enum değerlerini kontrol etmek için switch ifadesi kullanabilirsiniz. Örnek:

switch gun {
case .pazartesi:
    print("Bugün Pazartesi")
case .sali:
    print("Bugün Salı")
case .carsamba:
    print("Bugün Çarşamba")
case .persembe:
    print("Bugün Perşembe")
case .cuma:
    print("Bugün Cuma")
case .cumartesi:
    print("Bugün Cumartesi")
case .pazar:
    print("Bugün Pazar")
}


Değer Atama:

Enum değerlerine varsayılan değerler atayabilirsiniz. Örneğin:

enum HaftaninGunleri: Int {
    case pazartesi = 1
    case sali
    case carsamba
    case persembe
    case cuma
    case cumartesi
    case pazar
}

Bu örnekte, "pazartesi" değerine 1 atandı, ardından diğer değerler sırayla artırılarak atandı. Bu sayede enum değerlerine rastgele 
sayılar atanmış oldu.

Associated Values (İlişkilendirilmiş Değerler):

Enum, ilişkilendirilmiş değerlerle daha karmaşık veri yapısı oluşturmanıza da olanak tanır. Örneğin, bir ürünün türünü ve 
fiyatını içeren bir enum:

enum Urun {
    case elektronik(urunAdi: String, fiyat: Double)
    case giyim(urunAdi: String, beden: String)
    case gida(urunAdi: String, sonKullanmaTarihi: String)
}

Bu enum, ürünlerin farklı türlerini temsil ederken, her türün kendi ilişkilendirilmiş değerlerini içerir.

Enum, Swift'te daha karmaşık veri yapıları oluşturmanıza ve verileri gruplandırmanıza yardımcı olan güçlü bir araçtır. Swift'te enum kullanmak, 
kodunuzu daha okunabilir ve düzenli hale getirmenize yardımcı olabilir.
