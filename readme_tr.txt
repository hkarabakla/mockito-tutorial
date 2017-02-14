Mockito annotasyonları :

@Mock : Mocklamak istediğimiz obje için kullanıyoruz. Burada aşağıdaki gibi mockladığımız metod'a çağrı yapılınca
        gerçek kod çalıştırılmıyor sadece aşağıda belirttiğimiz output dönülüyor.
    Kullanımı : Mockito.when(mockedObj.methodName(input)).thenReturn(output); -> mocklanan objenin methodName isimli
                methodu input parametresi ile çağrılırsa output objesini dön

@InjectMocks : Bu anotasyonla anote edilen objenin içindeki fieldlar mocklanmış objelerler değiştirilir, inject edilir.
               Burada önemli olan mocklanan obje ile inject edilmek istenen objenin içindeki field'ın adı aynı olmalı,
               farklı olduğunda injection başarılı bir şekilde yapılamıyor. Bu anotasyon hem @Mock hemde @Spy ile anote
               edilen objelerin inject edilmesi için kullanılır.

@Spy : Buda @Mock gibi çalışır fakat burada metod çağrıları mocklanmış sonuçlar üzerinden değil gerçek kod
            çalıştırılarak üretilir.