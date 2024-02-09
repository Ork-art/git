# Questions - Git

-
    1. Git Nedir?
-     Cevab: Git, versiya nəzarəti sistemi (VNS) olaraq bilinən və proqram kodu və sənədlər üçün
  istifadə edilən açıq mənbəli bir VNS-dır. Bu, fərqli developerlər tərəfindən eyni proqramın müxtəlif
  versiyalarını eyni anda inkişaf etdirmək və idarə etmək üçün istifadə olunan bir alətdir.
-
     2. "git pull" ile "git fetch" komutlarının farkı nedir?
-      Cevab: git pull remote da olan mövcud repodakı kodları götürmək üçün istifadə edilir.
  git fetch isə remote repositoryde olan son məlumatları yalnızca local
  repositorye gətirən bir git prosesidir. ancaq local repodakı dəyişiklikləri birləşdirmir.
  local repoda olan hər hansı bir dəyişiklikləridə pozmaz.

-
    3. Eğer takım arkadaşımız "kodlarımı gönderdim, benim geliştirmemin üzerine devam et" derse ve
       gönderdiği kodları "git pull" ile lokalimize alamıyorsak nerelerde hata yapılmış olabilir?

-     Cevab: ilk səbəbi işlədiyi kodları kommit etdikdən sonra git push etməməsi ola bilər.
-
    4. git fetch origin" komutundaki "origin" neye karşılık gelmektedir?
-     Cevab:localdakı repo.muzun daxilində olan branchlərin remote olan qarşılığıdır.

    5. "HEAD" kelimesi neyi temsil etmektedir? 
      Cevab: "HEAD" ifadəsi, hansı commitin və ya branchin əsas olaraq işləndiyini göstərir.
       Bir branchda işləyirsəniz, "HEAD" o branchın son commitini göstərir. Eyni zamanda, "HEAD"
       fayllarınızın mövcud versiyasını da işarə edə bilər.
        
    6."Staging Area" ya da "Index" diye isimlendirilen bölge tam olarak ne demektir?
-     cevab: biz giti öz filemızda git init etdikdən sonra git bizim proyektimizdə yaranır. "Staging
  Area" ya da "Index" etdiyimiz dəyişikliyi "git add ." etməzdən əvvəl etdiyimiz dəyişikliklərin
  saxlanıldığı sahədir.

    7."Untracked file" ne demektir?
-     cevab:Git-də "Untracked file" (izlənilməyən fayl), Git nəzarətində olmayan, yəni izlənilməyən və
  qeydə alınmayan faylları ifadə edir.

    8. ".git" klasörünü silersek ne olur?
-      cevab: Git repositoriyasını tamamilə ləğv etmək deməkdir. Bu file, Git nəzarətindəki bütün
  məlumatları saxlayır, beləki onu silmək, proyektin nəzarəti altındakı bütün commit tarixçəsini,
  branchləri, konfiqurasiya məlumatlarını, qısaməlumatları və s. itirəcək.
-
    9. Kendi lokalimizde her "git init" komutunu kullanıdığımızda otomatik olarak "ReadMe.md"
       dosyası oluşturulmasını istiyorsak ne yapmalıyız?
      cevab: git filelarinin harada saxlanacağın təyin edirik.git --exec-path edib onun olduğu yeri
      tapa bilərik.bu file init adında bir file olacaqdır.  "ReadMe.md" file əlavə etmək için bu filela
      bir "ReadMe.md" file.nı yaratmalıyıq. Artık herhangi bir yerde "git init" komutunu
      kullandığınızda, "ReadMe.md" dosyası otomatik olarak oluşturulacaktır.

    10. Git konusunda bahsi geçen "branch" yapısı nedir? Bize ne sağlar?
       cevab: branch yapısı proyekimizi layerlərə ayırıb rahat işləməyimizi təmin edir. məsələn
        eyni anda iki developer bir poyektin müxtəlif hissələrini işləyib sonra master
        branchində birləşdirə bilər.müxtəlif vəziyyətlər ola bilər. bunun kimi.

    11. Sıfırdan bir "branch" nasıl oluşturabiliriz?
        cevab: yeni brach yaradan da masterden son dəyişikliyi çəkib, sonra masterden new branch
        edib yaradırıq. bu sayədə ilkin ola biləcək merge confilictlərin qarşısını almış ala
        bilərik.

    12. Var olan bir "branch"e nasıl geçebiliriz?
        cevab: olduğumuz branchden getmək istədiymiz branche checkout edərək keçə bilərik.
        istədiymiz branch remotededisə git pull origin master edib, hemin qayda ilə keçə
        bilərik.

    13. "git clone" komutunu kullanırken belirli bir spesifik branch'i sadece çekmek istiyorsak
        nasıl yapabiliriz?
        cevab: git clone -b <branch_adı> <repo_URL>

    14. "Merge conflict" ne demektir?
-            cevab: bir projedə eyni müxtəlif developer işləyə bilər və onların kodların merge edəndə 
              eyni yerə işlərdikləri sətirlərdə konflict yarana bilər. Bu zaman git öz başına qərar vermir.
-            Bunu developerin həll etməsini istəyir. və bunu merge resolve olaraq takım arkadaşınızla həll etmək
             daha məsləhətdir.

-    15."git log" komutu ile hangi bilgileri görebiliriz?
-          cevab: bir git repositoriyasındakı commit tarixçəsini göstərir. əvvəlki commitləri göstərir 
-          və hər bir commitin məlumatlarını, həmin commiti əlavə edən şəxsi, tarixi, commit
           mesajını və uniq SHA-1 identifikatorunu (commitin istifadə etməyə qərar verdiyi özəllikli kod)
           nümayiş etdirir.
-
     16. "git diff" ile kaç farklı iki durumun arasındaki değişiklikleri görebiliriz?
          cevab:  mövcud işlədiyimiz fayllarda hansı dəyişikliklərin olduğunu göstərir.
          əgər iki commit və ya branch arasında fərqi görmək istəyiriksək, onda git
          diff <commit1> <commit2> formada fərqi görərik və ya <commit> yerinə istənilən branch adını
         yazaraq arasındakı fərqi görə bilərik.

     17. Git reset ile neyi geri alıyoruz?
       cevab: əvvəlki commitlərə geri döndürür və əlavə edilmiş dəyişikliyi itirir.

     18. "git commit" ile "git push" arasındaki fark nedir?
-      cevab:git commit işlədiyiniz dəyişikləri yekun olaraq bir kommet altında sonlandıra bilərsiniz. amma 
-      bu kodlarını remote repo.ya göndərməz. bunun üçün git push dan istifadə etmək lazızdır.
       aralarında fərq git commit kodları remote repoya göndərməz amma git push göndərər.
-
    19. Atomic commit ne demektir?
        cevab: Git və digər vcs istifadə olunan bir konseptdir. Bir
        commit əməliyyatını ifadə edir və proyektdə dəyişiklikləri bir addımla qeyd etmək deməkdir.
        bir commitdə yalnız bir məqsəd və ya dəyişiklik qrupu yer almalıdır. hər commit konkret bir
        dəyişiklik və ya funksiyonal dəyişiklik paketi ilə əlaqəlidir. Atomic commit prinsipi təmiz
        və açıq commit tarixçəsi yaratmaqdır.

    20. Repository ne demektir?
        cevab: github veya git labda kodlarimizin saklandığı alan

    21. "git tag" nedir? "git branch"’ten farkı nedir?
        cevab: Bu komut, Git deposundaki belirli bir noktaya (commit'e) etiket eklemek için
        kullanılır.Bu komut, farklı çalışma dalları oluşturmak ve yönetmek için kullanılır."git tag"
        etiketleri işaretlemek ve belirli noktalara anlamlı isimler atamak için kullanılırken, "git
        branch" farklı çalışma dalları oluşturmak ve yönetmek için kullanılır.

    22. Git'i görsel olarak kullanabilmek için hangi üçüncü taraf araçları ve uygulamaları
        kullanabiliriz?
        cevab: genelde android kendisinde olan görsel kulanırım. sizin yazdıqlarına baxdım. 
        məlamat üçün özümdə saxladım.Teşekkür

    23. "GitHub" ile "git" arasındaki fark nedir? GitHub benzeri diğer siteler nelerdir? GitHub veya
        diğer sitelerdeki kullanıcı adlarını yazar mısınız?
        cevab:github kodlarımız saxladığı bir yerdir. git isə proyektimizdə baş verən
        dəyiliklikləri idarə etmək üçün olan tooldur.

    24. main ya da master branch'inin diğer branchlerden farkı nedir?
        cevab: bizim bütün branchlerimizden gelen kodlarimiz birleşdiyi yer olaraqda soymek
        olar.Veya branchlerimiz bir tester branchden toplayib, her şey okay olduqdan sonra mastere
        merge edib, sonra play markete gondere bilerik.