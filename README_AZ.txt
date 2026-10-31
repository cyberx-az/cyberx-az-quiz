# CyberX AZ – IT Quiz

Bu layihə 10 suallıq test, iştirakçı adı, avtomatik bal hesablanması və admin panelindən ibarətdir.

## Vacib təhlükəsizlik qeydi
İştirakçılar brauzerdən nəticə göndərirlər. Bu sadə başlanğıc versiyada serverdəki balı istifadəçi texniki biliklərlə saxtalaşdıra bilər. Rəsmi müsabiqə və ya hədiyyəli yarış üçün cavabları server tərəfində yoxlayan Edge Function əlavə edilməlidir. Admin paneli isə e-poçt/şifrə ilə Supabase Auth istifadə edir.

## 1. Supabase layihəsi yarat
1. https://supabase.com saytında pulsuz layihə yarat.
2. Project Settings → API bölməsindən Project URL və anon/public key götür.
3. `index.html` faylında `SUPABASE_URL` və `SUPABASE_ANON_KEY` dəyərlərini öz məlumatlarınla əvəz et.
4. Supabase → SQL Editor bölməsində `supabase.sql` faylının mətnini icra et.

Anon/public key brauzerdə istifadə üçün nəzərdə tutulub. Heç vaxt `service_role` açarını HTML-ə yerləşdirmə.

## 2. Admin hesabı yarat
Supabase → Authentication → Users bölməsində admin üçün istifadəçi yarat (email təsdiqini ehtiyacına uyğun qur). Bu e-poçt və şifrə ilə saytdakı `#admin` səhifəsindən giriş et.
İstehsal istifadəsində admin icazəsini ayrıca `admins` cədvəli və ya xüsusi role ilə məhdudlaşdırmaq tövsiyə olunur. Hazırkı SQL-də authenticated istifadəçi SELECT edə bilir; ona görə bu demo layihədə başqa istifadəçilərə Supabase Auth hesabı yaratma.

## 3. Saytı pulsuz yayımla
1. GitHub-da yeni public repository yarat, məsələn `cyberx-az-quiz`.
2. `index.html` faylını repository-nin əsas qovluğuna yüklə.
3. Repository → Settings → Pages → Deploy from a branch → `main` və `/ (root)` seç → Save.
4. GitHub Pages bir neçə dəqiqəyə ictimai URL verəcək. Linki Instagram bio və paylaşımda yerləşdir.

## 4. İstifadə
- İştirakçı linki açır, adını yazır, 10 suala cavab verir.
- Nəticə Supabase cədvəlinə yazılır.
- Admin `SAYT-LINKI/#admin` ünvanından daxil olub iştirakçıların siyahısını görür.

## Qeydlər
- İştirakçı adı toplanır; Instagram adı tələb olunmur.
- İştirakçılara məlumatların nəticə cədvəlində saxlandığını qısa şəkildə bildirmək yaxşı təcrübədir.
- Bu demo bir dəfəlik test nəticələrini saxlayır; təkrar cəhdlər ayrıca sətir kimi görünür.
