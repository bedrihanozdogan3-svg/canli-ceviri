---
title: Gizlilik Politikası — Canlı Çeviri
---

<!-- surum: 2026-11-11 -->
# Canlı Çeviri — Gizlilik Politikası

Sürüm 2026-11-11 · Yayımcı: **Uygun Yazılım** · İletişim: **zeynepuygun.339@gmail.com**

Bu metin Canlı Çeviri programının bilgisayarınızda neyi okuduğunu, neyi sakladığını ve neyin bilgisayarınızdan çıktığını anlatır.
Programın davranışı bu metinle sınırlıdır; metin değişirse program açılışta yeniden onayınızı ister.

## 1. Program ne okur

- **Ekran:** Çeviri açıkken seçtiğiniz oyunun, videonun, belgenin ya da programın ekran görüntüsü alınır ve yazısı bilgisayarınızda
  okunur. Ekran görüntüsü hiçbir yere gönderilmez.
- **Normal programların ve tarayıcı sayfalarının yazısı:** Ayarlar penceresi, menü ve düğme yazıları ile tarayıcıda önde
  duran sayfanın yazısı Windows'un erişilebilirlik arayüzünden (UI Automation)
  okunur. Bu yazılar **hiçbir ayarda bilgisayarınızdan çıkmaz**; her zaman bilgisayarınızda çevrilir ve çeviri belleğine
  yazılmaz.
- **Ekrandan oku (Ctrl+F6):** fareyle seçtiğiniz kutunun yazısı yalnız o an bilgisayarınızda çevrilir; **hiçbir ayarda internete
  gitmez, diske (çeviri belleğine) yazılmaz**, ortak sözlüğe girmez.
- **Windows bildirimleri, arama, kilit ekranı ve oturum açma ekranı okunmaz** (mesaj önizlemesi, aranan sözcük, son dosyalar
  gibi kişisel yazı taşırlar).
- **Mesajlaşma ve e-posta:** "Programlar" açıkken mesajlaşma ve e-posta programlarının (Discord, WhatsApp, Telegram, Signal,
  Slack, Teams, Outlook, Thunderbird, Skype, Zoom, Messenger, Viber, WeChat, LINE) ve tarayıcıdaki mesaj / e-posta
  sayfalarının (Gmail, WhatsApp Web, Telegram Web gibi) yazısı da çevrilir. Mesaj ve e-posta yazısı **yalnız
  bilgisayarınızda çevrilir, hiçbir ayarda bilgisayarınızdan çıkmaz**, diske (çeviri belleğine) yazılmaz, ortak sözlüğe
  girmez. Sizin yazdığınız kutu (mesaj kutusu, arama, şifre) ve adres çubuğu okunmaz. Yapay zekâ sohbet uygulamaları ve
  sayfaları okunmaz.
- **Ses (sesli özellikler açıksa):** Oyun ya da video sesi bilgisayarınızda yazıya çevrilir. Ses kaydı dışarı gönderilmez.

## 2. Bilgisayarınızda ne saklanır

Deneme kaydı dışında hepsi program klasöründeki `veri` klasöründedir; programı kaldırsanız da siz silene kadar kalır.

- Ayarlarınız ve onay sürümü.
- Çeviri belleği (daha önce çevrilen yazılar ve çevirileri), oyun başına öğrenilen adlar ve altyazı yeri.
- **Ekran hafızası:** Aynı oyun ekranı yeniden açıldığında çeviriyi hemen gösterebilmek için o ekranın çok küçük, gri bir kopyası
  (96 × 54 nokta; yazı okunamaz) ve o ekranda okunan yazılar oyun başına saklanır (en çok 300 ekran).
- Programın kendi günlüğü (hata bulmak için; okunan yazıların kısa parçalarını içerebilir).
- **Deneme kaydı** (lisans anahtarı girilmeden kullanılan 2 saatlik deneme): kullanılan deneme süresi ve bu bilgisayara bağlı
  bir imza. `veri` klasörüne ek olarak kullanıcı klasörünüzde (`%LOCALAPPDATA%\UygunYazilim\CanliCeviri`) ve Windows kayıt
  defterinde (`HKCU\Software\UygunYazilim\CanliCeviri`) tutulur ve program kaldırılınca silinmez; böylece yeniden kurmak
  denemeyi sıfırlamaz. Kişisel bilgi içermez, bilgisayarınızdan dışarı gönderilmez.

## 3. Bilgisayarınızdan ne çıkar

### 3.1 "Çeviri: yalnız yerel model (internetsiz)" ayarı (varsayılan)
Program bu ayarla gelir; internet çevirisi ve ortak sözlük paylaşımı **kapalıdır** ve ancak siz panelden açıp, ne
gönderileceğini anlatan izin penceresinde "Evet" derseniz açılır.
Bu ayarda **hiçbir yazı bilgisayarınızdan çıkmaz**: çeviri servisine istek, ortak sözlük gönderimi ya da indirmesi yapılmaz.
Yalnız siz istediğinizde program güncellemesi ve dil modeli indirmesi, bir de anahtarla alınan sürümde lisans
doğrulaması yapılır (3.4).

### 3.2 "Önce yerel, sonra internetle iyileşir" ve "Yalnız internet" ayarları (yalnız sizin izninizle)
- Bu ayarlar varsayılan olarak kapalıdır. Panelde seçtiğinizde ne gönderileceği bir izin penceresinde yazar; "Evet"
  demedikçe açılmaz. İstediğiniz an "Çeviri: yalnız yerel model" ile kapatabilirsiniz.
- Bilgisayardaki çeviri yetersiz kaldığında ya da o dil için bilgisayarda model yoksa, çevrilecek **yazı** (ekrandan okunan
  oyun / video / belge yazısı, sesten çıkan yazı) **MyMemory** çeviri servisine (Translated srl, İtalya,
  api.mymemory.translated.net) gönderilir. Gönderilen yalnız yazı ve dil çiftidir; ekran görüntüsü, ses, kimlik ya da hesap
  bilgisi gönderilmez. Günlük gönderilen yazı miktarı sınırlıdır. MyMemory'nin kendi gizlilik koşulları geçerlidir.
- Normal programların yazısı (1. madde) bu ayarlarda da gönderilmez.
- Menü yazısını kısaltmak için bir yapay zekâ servisi (DeepSeek) kullanma özelliği **bu sürümde kapalıdır**; açılırsa bu metin
  güncellenir ve onayınız yeniden istenir.

### 3.3 Ortak sözlük (oyun çevirilerinin paylaşımı)
Amaç: oyun menülerinin çevirisini bütün kullanıcılar için düzeltmek. **Paylaşım varsayılan olarak kapalıdır.** Panelin Oyun
sekmesindeki "Paylaşımı aç" ile, ne gönderileceğini anlatan izin penceresinde "Evet" derseniz açılır; "Paylaşımı kapat" ile
istediğiniz an kapatırsınız. Ortak sözlük de yalnız paylaşım açıkken indirilir.
Dayanak: sizin açık izniniz. Aşağıda sayılan veri kimliğinizi taşımayan kullanım verisidir (oyun menüsü yazıları ve
çevirileri). Kapatınca henüz gönderilmemiş kayıtlar bilgisayarınızdan silinir ve
bir daha hiçbir şey gönderilmez. "Yalnız yerel model" ayarında paylaşım da yapılmaz.

Gönderilen (yalnız **oyun** penceresinden; tarayıcı, mesajlaşma ve normal programlardan hiçbir şey):
- Oyunun dosya adı (örneğin `game.exe`).
- Kısa menü / arayüz yazısı ve çevirisi: en çok 6 kelime; yalnız İngilizce harfler. Rakam içeren (kullanıcı adı, skor, saat),
  e-posta ya da adres gibi görünen, sohbet biçimindeki (`Ad: mesaj`, `[Takım]`) ve oyuncu adı biçimindeki yazılar gönderilmez.
  Yalnız programın kendi çeviri modelinin çevirisi gider: **oyunların kendi (resmi) çevirileri paylaşılmaz**.
  Ortak sözlük Türkçedir: çeviri dili Türkçe değilken çeviri ve düzeltme gönderilmez.
- Sizin düzelttiğiniz çeviriler (aynı süzgeçle, en çok 30 kelime).
- Oyundaki karakter / yer adları (tek kelime).
- Altyazının ekrandaki yeri (pencereye göre oran; ekran görüntüsü değil).
- Bilgisayarınızda rastgele üretilen bir kurulum sayısı (aynı yazının kaç ayrı kurulumdan geldiğini saymak için; sizinle,
  hesabınızla ya da bilgisayarınızla bağı yoktur).

Gönderilmeyen: adınız, e-postanız, hesap bilgileriniz, mesajlarınız, sohbetler, ekran görüntüsü, ses, dosyalarınız.

Sunucu tarafı: kayıtlar Google Cloud üzerinde (Avrupa, Belçika bölgesi) çalışan sunucumuza gider. Sunucu kurulum sayısını ve
bağlantının ağ bilgisini (IP adresinin ilk üç hanesi) yalnız tek yönlü özet (tuzlu karma) olarak saklar; **IP adresinin
kendisini, tarayıcı / program bilgisini ve başka bağlantı bilgisini saklamaz**; amaç aynı kişinin bir yazıyı birden çok kez
saymasını önlemektir. Bir çeviri, en az 3 ayrı kurulumdan ve 3 ayrı
ağdan aynı gelirse ortak sözlüğe girer ve herkesin programına günde bir kez iner. Barındırma sağlayıcısının (Google Cloud)
sözlük sunucusu için kendi istek kaydı da kapalıdır.

### 3.4 Güncelleme, dil modeli, lisans
- Program güncellemesi ve dil modeli indirmesi: yalnız indirme yapılır; yazınız gönderilmez.
- Lisans (mağaza dışı satışlarda): etkinleştirirken, etkinleştirmeden sonraki ilk 10 gün her açılışta, sonra ayda bir
  doğrulamak için (iade edilen anahtar kapansın diye)
  lisans anahtarınız ve rastgele bir cihaz adı (bilgisayarınızın adı değil) satış altyapısına
  (Lemon Squeezy) gönderilir; "Yalnız yerel" ayarında da. Bağlantı yoksa program açık kalır. Steam sürümünde sahiplik Steam'in kendi yazılımıyla denetlenir.
- Chrome eklentisi yalnız bu bilgisayardaki programla konuşur (127.0.0.1); dışarı bir şey göndermez.
- Dublaj (videonun sesli çevirisi) bu sürümde yoktur. Eklendiğinde izlediğiniz videonun sesi YouTube'dan indirilir; bu
  metin güncellenir ve onayınız yeniden istenir.

### 3.5 Windows'un kendi tanılama verileri
Windows, tanılama verisi ayarınıza göre bilgisayardaki programların kullandığı Windows bileşenleri hakkında kullanım
bilgisini kendi tanılama hizmetiyle Microsoft'a gönderebilir. Bu, Windows'un kendi hizmetidir; Canlı Çeviri bu yolla ekran
görüntüsü ya da yazı göndermez. Canlı Çeviri, okuma motorunun (ONNX Runtime) kendi kullanım olaylarını kapatır. Windows
ayarlarından kapatabilir, gönderilenleri "Tanılama Verileri Görüntüleyicisi" ile görebilirsiniz.

## 4. Haklarınız

6698 sayılı KVKK ve (Avrupa Birliği'ndeyseniz) GDPR kapsamındaki haklarınız (bilgi isteme, düzeltme, silme, itiraz) için
**zeynepuygun.339@gmail.com** adresine yazabilirsiniz. Ortak sözlüğe giden kayıtlar kimliğinizle eşleştirilemediği için tek
tek bulunamayabilir; paylaşımı kapatmak gönderimi hemen durdurur. Program 13 yaşından küçükler için tasarlanmamıştır.

## 5. Telefon (Android) uygulaması

Bu bölüm yalnız telefon uygulaması içindir; 1–3. maddeler bilgisayar programını anlatır, 4. madde ikisi için de geçerlidir.
Telefon uygulaması (Google Play) için iletişim ve 4. maddedeki istekler: **bedrihanozdogan3@gmail.com**.

- **Ne okur:** Ekranın görüntüsü yalnız siz kenardaki **Çevir** düğmesine dokunduğunuzda ya da **Sürekli** kip açıkken alınır.
  Bunun için Android'in "ekran kaydı / paylaşımı" izni kullanılır ve telefon bunu bildirim çubuğunda gösterir. Yazı telefonda
  okunur; ekran görüntüsü kaydedilmez, hiçbir yere gönderilmez. Kopya korumalı ekranlar (Netflix, banka uygulamaları gibi)
  telefonun kuralıyla siyah gelir ve okunmaz.
- **Bu sürümde uygulama hangi uygulamanın açık olduğuna bakmaz:** mesajlaşma uygulamasındayken düğmeye dokunursanız ya da
  Sürekli kip açıksa o ekran da okunur ve çevrilir (telefonda kalır, dışarı gitmez).
- **Çeviri telefonda yapılır:** İngilizceden Türkçeye çeviriyi, uygulamayla birlikte gelen kendi çeviri modelimiz telefonda
  yapar. Öteki diller Google'ın ML Kit bileşeniyle, yine telefonda çevrilir. Okunan yazı internete gönderilmez. MyMemory,
  ortak sözlük ve lisans doğrulaması telefon uygulamasında yoktur.
- **İnternet:** Yalnız ilk kullanımda dil paketi ve ML Kit'in kendi çalışma ayarları Google sunucularından indirilir. Bu
  isteklerde ekran görüntüsü ve okunan yazı gönderilmez. Google indirme sırasında telefonun ağ adresini, indirme için gereken
  teknik bilgiyi (uygulama ve bileşen sürümü gibi) ve ML Kit'in bu kuruluma verdiği rastgele bir kimliği (kişiyi ya da
  telefonu tanımak için değildir) görür; bunlar Google'ın kendi gizlilik koşullarına tabidir.
- **Kullanım istatistiği kapalı:** ML Kit normalde Google'a kimliksiz kullanım istatistiği (cihaz modeli, uygulama adı, süre,
  dil; okunan yazı değil) gönderir. Canlı Çeviri'de bu gönderim kapatılmıştır.
- **Telefonda ne kalır:** Hepsi uygulamanın telefondaki kendi klasöründedir; başka uygulamalar erişemez.
  - İndirilen dil paketleri ve seçtiğiniz çeviri dili.
  - **Çeviri belleği:** Aynı yazıyı yeniden çevirmemek için okunan yazılar ve çevirileri. En çok 5.000 kayıt tutulur, en
    eskisi silinir.
  - **Ekran hafızası:** Görülmüş bir ekrana (menü, envanter, harita) dönülünce çeviriyi hemen koymak için tutulur. İçinde o
    ekranın kaba gri bir izi (ekranın her 40 × 40 noktalık parçası için 16 tonluk tek bir parlaklık değeri; görüntü değildir, yazı okunamaz), o ekranda okunan yazılar, yerleri ve
    çevirileri bulunur. En çok 300 ekran tutulur, en az kullanılan silinir.
  - Çeviri belleği ve ekran hafızası Canlı Çeviri kapanırken dosyaya yazılır, açılınca okunur. Ekran görüntüsünün kendisi
    diske yazılmaz.
  - Uygulamanın kendi günlüğüne yalnız sayı ve durum yazılır (kaç yazı okundu gibi; okunan yazı yazılmaz). Günlük 1 MB'ı
    geçince bir önceki günlük silinir.
  - Google'ın çeviri bileşeni çevirdiği cümleyi telefonun kendi sistem günlüğüne yazar. Bu günlük telefonda kalır, Canlı
    Çeviri onu dışarı göndermez.
- **Hiçbiri telefondan çıkmaz:** Canlı Çeviri bu dosyaları hiçbir yere göndermez. Dosyalar Android'in bulut yedeğine ve yeni
  telefona aktarmaya da girmez; ikisi de uygulamada kapalıdır.
- **Silmek için:** Telefonun Ayarlar → Uygulamalar → Canlı Çeviri → Depolama → Verileri sil adımlarını izleyin ya da uygulamayı
  kaldırın. İkisi de yukarıdakilerin hepsini siler.

---

# Live Translation (Canlı Çeviri) — Privacy Policy

Version 2026-11-11 · Publisher: **Uygun Yazılım** · Contact: **zeynepuygun.339@gmail.com**

This explains what the program reads on your computer, what it stores, and what leaves your computer. If this text changes,
the program asks for your consent again at start-up.

## 1. What the program reads
- **Screen:** while translation is on, screenshots of the game, video, document or program you chose are read **on your
  computer**. Screenshots are never sent anywhere.
- **Text of regular programs** (settings windows, menus, buttons) is read through Windows UI Automation and **never leaves your
  computer in any setting** and is not stored in the translation memory.
- **Read from screen (Ctrl+F6):** the text of the box you draw is translated once on your computer; it **never goes online
  and is never written to disk** (translation memory) or to the shared dictionary.
- **Windows notifications, search, lock screen and sign-in screen are never read.**
- **Messaging and e-mail:** while "Programs" is on, the text of messaging and e-mail programs (Discord, WhatsApp, Telegram,
  Signal, Slack, Teams, Outlook, Thunderbird, Skype, Zoom, Messenger, Viber, WeChat, LINE) and of message / e-mail pages in
  the browser (such as Gmail, WhatsApp Web, Telegram Web) is translated too. Message and e-mail text is **translated only on
  your computer and never leaves your computer in any setting**; it is not written to disk (translation memory) and does
  not enter the shared dictionary. The box you type in (message box, search, password) and the address bar are not read.
  AI chat apps and pages are not read.
- **Audio** (if voice features are on) is transcribed on your computer and never sent.

## 2. What is stored on your computer
In the `veri` folder: your settings and consent version; translation memory; learned names and subtitle positions per game;
a **screen memory** (a tiny 96 × 54 grey thumbnail of a game screen, text not readable, plus the text read on it; at most 300
screens per game) so known screens are translated instantly; and the program's log (may contain short pieces of read text).
The **trial record** (2-hour trial before a licence key is entered: trial time used and a signature tied to this computer) is
also kept in `%LOCALAPPDATA%\UygunYazilim\CanliCeviri` and the Windows registry (`HKCU\Software\UygunYazilim\CanliCeviri`) and
is not removed on uninstall, so reinstalling does not reset the trial; it holds no personal data and never leaves your computer.

## 3. What leaves your computer
- **"Local model only (offline)" setting (default):** no text leaves your computer — no translation service, no shared dictionary. Only
  updates and language-model downloads you start, and the licence check of key-activated copies (every start in the first 10 days, then monthly).
- **"Local first, improved online" and "Internet only" settings (off by default; turned on only if you answer "Yes" in
  the permission window that states what is sent):** when local translation is weak or no local model exists for a language, the
  **text** to translate (game / video / document text, transcribed speech) is sent to the **MyMemory** translation service
  (Translated srl, Italy). Only text and the language pair are sent — no screenshots, audio, identity or account data. Daily
  volume is limited. Text of regular programs is never sent. The AI menu-shortening feature (DeepSeek) is **off in this
  version**.
- **Shared dictionary:** **sharing is off by default.** It is turned on with "Turn on sharing" on the Oyun (Game) tab of
  the panel only if you answer "Yes" in the permission window that states what is sent; "Turn off sharing" turns it off
  at any time and also deletes records not yet sent. The shared dictionary is downloaded only while sharing is on. Sent only from **game** windows: the game's file name; short menu / UI
  text and its translation (max 6 words, English letters only; no numbers, e-mail / addresses, chat lines or player names;
  only translations made by the program's own model — **games' own official translations are never shared**; nothing
  is sent while the target language is not Turkish, since the shared dictionary is Turkish);
  your corrections (same filter, max 30 words); character / place names (one word); the subtitle position (a ratio, not an
  image); a random install number generated on your computer (to count distinct installs; not linked to you). Never sent:
  your name, e-mail, accounts, messages, chats, screenshots, audio, files. Our server (Google Cloud, Belgium) stores the
  install number and the network (first three parts of the IP address) only as salted one-way hashes — never the IP address
  itself, the browser / program details or other connection data. Basis: this is not consent-based processing of personal
  data; the data is non-identifying usage data (game menu texts and translations) and can be turned off at any time.
  A translation enters the shared dictionary only when it arrives identically from at least 3 installs and 3 networks.
  The hosting provider's (Google Cloud) own request log for the dictionary server is switched off too.
- **Updates, language models, licence:** downloads only. Licence (non-store sales): on activation, at every start in the first 10 days after it, then once a month (so that a
  refunded key is switched off) your licence key and a random device name (not your computer's name) are sent to Lemon
  Squeezy, also in "Local model only"; without a connection the program stays open; on Steam, ownership is checked by Steam. The Chrome extension talks only to the
  program on this computer (127.0.0.1). Dubbing (spoken translation of videos) is not in this version; when added,
  the audio of the video you watch is downloaded from YouTube and this policy is updated.
- **Windows' own diagnostic data:** Windows may send usage information about the Windows components that programs on your
  computer use to Microsoft through its own diagnostics service, depending on your diagnostic data setting. This is
  Windows' own service; Canlı Çeviri sends no screenshots or text this way. Canlı Çeviri turns off the reading engine's
  (ONNX Runtime) own usage events. You can turn this off in Windows settings and see what is sent with "Diagnostic Data
  Viewer".

## 4. Your rights
For requests under Turkish KVKK or the EU GDPR (access, correction, deletion, objection) write to
**zeynepuygun.339@gmail.com**. Shared-dictionary records cannot be linked to you and may not be individually findable;
turning sharing off stops sending immediately. The program is not intended for children under 13.

## 5. Phone (Android) app
This section covers the phone app only; sections 1–3 describe the computer program, section 4 applies to both.
For the phone app (Google Play), contact and section 4 requests: **bedrihanozdogan3@gmail.com**.
- **What it reads:** a screenshot is taken only when you tap the **Çevir** (Translate) button at the edge of the screen or
  while **Sürekli** (Continuous) mode is on, through Android's screen recording / sharing permission, which the phone shows in
  the status bar. Text is read on the phone; screenshots are never saved or sent anywhere. Copy-protected screens (Netflix,
  banking apps and similar) come through black by the phone's own rule and are not read.
- **In this version the app does not check which app is open:** if you tap the button in a messaging app, or Continuous mode is
  on there, that screen is read and translated too (it stays on the phone).
- **Translation happens on the phone:** English-to-Turkish translation is done on the phone by our own translation model,
  which comes with the app. Other languages are translated with Google's ML Kit component, also on the phone. No text is
  sent online. MyMemory, the shared dictionary and licence checks do not exist in the phone app.
- **Internet:** only on first use, the language pack and ML Kit's own working settings are downloaded from Google's servers. No
  screenshot or read text is sent in these requests. Google sees the phone's network address, the technical details the
  download needs (such as app and component version) and a random identifier ML Kit gives this installation (not meant to
  identify you or the phone); these fall under Google's own privacy terms.
- **Usage statistics are off:** ML Kit normally sends Google anonymous usage statistics (device model, app name, duration,
  language; not the read text). This sending is switched off in Canlı Çeviri.
- **What stays on the phone:** everything below is in the app's own folder on the phone, which other apps cannot access.
  - Downloaded language packs and your chosen target language.
  - **Translation memory:** texts read and their translations, so the same text is not translated again. At most 5,000
    entries are kept; the oldest is deleted.
  - **Screen memory:** kept so that when you return to a screen you have seen (menu, inventory, map) the translation appears
    at once. It holds a coarse grey trace of that screen (one 16-level brightness value for each 40 × 40-pixel patch; not an image, text cannot be read), the texts read on
    it, their positions and translations. At most 300 screens are kept; the least used is deleted.
  - The translation memory and screen memory are written to a file when Canlı Çeviri closes and read when it opens.
    Screenshots themselves are never written to disk.
  - The app's own log holds only numbers and status (such as how many texts were read; never the read text). When it passes
    1 MB, the previous log is deleted.
  - Google's translation component writes the sentence it translates to the phone's own system log. That log stays on the
    phone and Canlı Çeviri never sends it anywhere.
- **None of this leaves the phone:** Canlı Çeviri sends none of these files anywhere. They are also excluded from Android's
  cloud backup and from transfer to a new phone; both are switched off in the app.
- **To delete:** go to the phone's Settings → Apps → Canlı Çeviri → Storage → Clear data, or uninstall the app. Either one
  deletes all of the above.
