---
title: Gizlilik Politikası — Canlı Çeviri
---

<!-- surum: 2026-11-06 -->
# Canlı Çeviri — Gizlilik Politikası

Sürüm 2026-11-06 · Yayımcı: **Uygun Yazılım** · İletişim: **zeynepuygun.339@gmail.com**

Bu metin Canlı Çeviri programının bilgisayarınızda neyi okuduğunu, neyi sakladığını ve neyin bilgisayarınızdan çıktığını anlatır.
Programın davranışı bu metinle sınırlıdır; metin değişirse program açılışta yeniden onayınızı ister.

## 1. Program ne okur

- **Ekran:** Çeviri açıkken seçtiğiniz oyunun, videonun, belgenin ya da programın ekran görüntüsü alınır ve yazısı bilgisayarınızda
  okunur. Ekran görüntüsü hiçbir yere gönderilmez.
- **Normal programların yazısı:** Ayarlar penceresi, menü ve düğme yazıları Windows'un erişilebilirlik arayüzünden (UI Automation)
  okunur. Bu yazılar **hiçbir ayarda bilgisayarınızdan çıkmaz**; her zaman bilgisayarınızda çevrilir ve çeviri belleğine
  yazılmaz.
- **Ekrandan oku (Ctrl+F6):** fareyle seçtiğiniz kutunun yazısı yalnız o an bilgisayarınızda çevrilir; **hiçbir ayarda internete
  gitmez, diske (çeviri belleğine) yazılmaz**, ortak sözlüğe girmez.
- **Windows bildirimleri, arama, kilit ekranı ve oturum açma ekranı okunmaz** (mesaj önizlemesi, aranan sözcük, son dosyalar
  gibi kişisel yazı taşırlar).
- **Mesajlaşma programları okunmaz:** Discord, WhatsApp, Telegram, Signal, Slack, Teams, Outlook, Thunderbird, Skype, Zoom,
  Messenger, Viber, WeChat, LINE, yapay zekâ sohbet uygulamaları gibi kişisel yazı içeren programlar hiç okunmaz.
- **Ses (sesli özellikler açıksa):** Oyun ya da video sesi bilgisayarınızda yazıya çevrilir. Ses kaydı dışarı gönderilmez.

## 2. Bilgisayarınızda ne saklanır

Hepsi program klasöründeki `veri` klasöründedir; programı kaldırsanız da siz silene kadar kalır.

- Ayarlarınız ve onay sürümü.
- Çeviri belleği (daha önce çevrilen yazılar ve çevirileri), oyun başına öğrenilen adlar ve altyazı yeri.
- **Ekran hafızası:** Aynı oyun ekranı yeniden açıldığında çeviriyi hemen gösterebilmek için o ekranın çok küçük, gri bir kopyası
  (96 × 54 nokta; yazı okunamaz) ve o ekranda okunan yazılar oyun başına saklanır (en çok 300 ekran).
- Programın kendi günlüğü (hata bulmak için; okunan yazıların kısa parçalarını içerebilir).

## 3. Bilgisayarınızdan ne çıkar

### 3.1 "Çeviri: yalnız yerel model (internetsiz)" ayarı
Bu ayarda **hiçbir yazı bilgisayarınızdan çıkmaz**: çeviri servisine istek, ortak sözlük gönderimi ya da indirmesi yapılmaz.
Yalnız siz istediğinizde program güncellemesi ve dil modeli indirmesi, bir de anahtarla alınan sürümde lisans
doğrulaması yapılır (3.4).

### 3.2 "Önce yerel, sonra internetle iyileşir" (varsayılan) ve "Yalnız internet" ayarları
- Bilgisayardaki çeviri yetersiz kaldığında ya da o dil için bilgisayarda model yoksa, çevrilecek **yazı** (ekrandan okunan
  oyun / video / belge yazısı, sesten çıkan yazı) **MyMemory** çeviri servisine (Translated srl, İtalya,
  api.mymemory.translated.net) gönderilir. Gönderilen yalnız yazı ve dil çiftidir; ekran görüntüsü, ses, kimlik ya da hesap
  bilgisi gönderilmez. Günlük gönderilen yazı miktarı sınırlıdır. MyMemory'nin kendi gizlilik koşulları geçerlidir.
- Normal programların yazısı (1. madde) bu ayarlarda da gönderilmez.
- Menü yazısını kısaltmak için bir yapay zekâ servisi (DeepSeek) kullanma özelliği **bu sürümde kapalıdır**; açılırsa bu metin
  güncellenir ve onayınız yeniden istenir.

### 3.3 Ortak sözlük (oyun çevirilerinin paylaşımı)
Amaç: oyun menülerinin çevirisini bütün kullanıcılar için düzeltmek. **Paylaşım varsayılan olarak açıktır; panelin Oyun
sekmesindeki "Paylaşımı kapat" ile istediğiniz an kapatabilirsiniz.**
Dayanak: paylaşım sizin rızanıza bağlı bir kişisel veri işleme değildir; aşağıda sayılan veri kimliğinizi taşımayan kullanım
verisidir (oyun menüsü yazıları ve çevirileri) ve her an kapatılabilir. Bu yüzden ayrıca sorulmaz. Kapatınca henüz gönderilmemiş kayıtlar bilgisayarınızdan silinir ve
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

## 4. Haklarınız

6698 sayılı KVKK ve (Avrupa Birliği'ndeyseniz) GDPR kapsamındaki haklarınız (bilgi isteme, düzeltme, silme, itiraz) için
**zeynepuygun.339@gmail.com** adresine yazabilirsiniz. Ortak sözlüğe giden kayıtlar kimliğinizle eşleştirilemediği için tek
tek bulunamayabilir; paylaşımı kapatmak gönderimi hemen durdurur. Program 13 yaşından küçükler için tasarlanmamıştır.

---

# Live Translation (Canlı Çeviri) — Privacy Policy

Version 2026-11-05.3 · Publisher: **Uygun Yazılım** · Contact: **zeynepuygun.339@gmail.com**

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
- **Messaging apps are never read** (Discord, WhatsApp, Telegram, Signal, Slack, Teams, Outlook, Thunderbird, Skype, Zoom,
  Messenger, Viber, WeChat, LINE, AI chat apps and similar).
- **Audio** (if voice features are on) is transcribed on your computer and never sent.

## 2. What is stored on your computer
In the `veri` folder: your settings and consent version; translation memory; learned names and subtitle positions per game;
a **screen memory** (a tiny 96 × 54 grey thumbnail of a game screen, text not readable, plus the text read on it; at most 300
screens per game) so known screens are translated instantly; and the program's log (may contain short pieces of read text).

## 3. What leaves your computer
- **"Local model only (offline)" setting:** no text leaves your computer — no translation service, no shared dictionary. Only
  updates and language-model downloads you start, and the licence check of key-activated copies (every start in the first 10 days, then monthly).
- **"Local first, improved online" (default) and "Internet only" settings:** when local translation is weak or no local model exists for a language, the
  **text** to translate (game / video / document text, transcribed speech) is sent to the **MyMemory** translation service
  (Translated srl, Italy). Only text and the language pair are sent — no screenshots, audio, identity or account data. Daily
  volume is limited. Text of regular programs is never sent. The AI menu-shortening feature (DeepSeek) is **off in this
  version**.
- **Shared dictionary:** **sharing is on by default; you can turn it off at any time with "Turn off sharing" on
  the Oyun (Game) tab of the panel**, which also deletes records not yet sent. Sent only from **game** windows: the game's file name; short menu / UI
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

## 4. Your rights
For requests under Turkish KVKK or the EU GDPR (access, correction, deletion, objection) write to
**zeynepuygun.339@gmail.com**. Shared-dictionary records cannot be linked to you and may not be individually findable;
turning sharing off stops sending immediately. The program is not intended for children under 13.
