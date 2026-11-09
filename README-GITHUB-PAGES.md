# Monease GitHub Pages — TR/EN Privacy & Support

Bu paket Monease v0.17 `ReleaseWeb` taslaklarından türetilmiştir. **Taslaklar hukuken/operasyonel olarak doğrulanmış değildir.**

## Yayın öncesi zorunlu düzenlemeler

1. İletişim adresi dört HTML dosyasında `atilla.poyraz1998@gmail.com` olarak ayarlandı ve `mailto:` bağlantıları eklendi. **Gizlilik politikalarında `REPLACE_WITH_LEGAL_OPERATOR_NAME` yer tutucusunu doğrulanmış gerçek işletmeci kimliğiyle değiştirmelisiniz.**
2. `privacy-tr.html` ve `privacy-en.html` içindeki veri işleme açıklamalarını mevcut Monease koduyla, Apple ve RevenueCat privacy disclosures ile doğrulayın; gerekiyorsa profesyonel hukuki inceleme alın.
3. Kimlik ve metinler doğrulandıktan sonra gizlilik politikalarındaki TASLAK / DRAFT uyarılarını ve `index.html` üzerindeki taslak uyarısını kaldırın. Tarihleri gerçek yayın tarihine güncelleyin.
4. Destek e-posta adresine giden `mailto:` bağlantıları eklendi. E-posta adresinin gerçekten mesaj alabildiğini kontrol edin. Bu adres GitHub Pages yayınında herkese açık olacaktır.
5. GitHub Pages altında hiçbir gizli API anahtarı, `.p8` anahtarı veya finansal kayıt yayınlamayın. Site **herkese açıktır**.

## UNKNOWN gibi GitHub Pages kurulumu

1. GitHub üzerinde yeni **Public** depo oluşturun. Önerilen isim: `monease-site`.
2. Bu ZIP içindeki **dosyaları** depoya kök dizinde yükleyin; üst klasörü değil (`index.html` doğrudan root'ta olmalı).
3. Repository `Settings` → `Pages` → `Build and deployment` → `Source: Deploy from a branch` → `Branch: main` → `Folder: /(root)` → `Save`.
4. Yayın sonrasında depo sahibi `GITHUB_USERNAME` ise site: `https://GITHUB_USERNAME.github.io/monease-site/`.
5. Sayfaları Safari'de tek tek açıp kontrol edin.

## URL şablonları (YAYINLANMADAN AÇILMAZ)

- TR policy: `https://GITHUB_USERNAME.github.io/monease-site/privacy-tr.html`
- EN policy: `https://GITHUB_USERNAME.github.io/monease-site/privacy-en.html`
- TR support: `https://GITHUB_USERNAME.github.io/monease-site/support-tr.html`
- EN support: `https://GITHUB_USERNAME.github.io/monease-site/support-en.html`

## Monease Xcode bağlama

- Build Settings → `MONEASE_PRIVACY_POLICY_URL` = canlı gizlilik politikası HTTPS URL.
- Build Settings → `MONEASE_SUPPORT_URL` = canlı destek HTTPS URL.
- Bu iki değer hem Debug hem Release için doğru olmalı; iPhone'da TR/EN Privacy Center ve Premium Privacy bağlantılarını test edin.
- App Store Connect → App Privacy: canlı Privacy Policy URL girin; mümkünse TR/EN locale'lerinde farklı adresler sunun.
- App Store Connect → App Information / Version metadata: canlı Support URL girin.
- **Not:** Monease v0.17 `AppLinks.swift` aynı URL'leri dil değişimine göre otomatik seçmiyor; Xcode'da iki URL değerini belirlemek tek varsayılan adres sunar. Tam dil-duyarlı URL isteniyorsa kodda ek değişiklik gerekir.
- RevenueCat `appl_` production anahtarı ve App Store Sandbox/TestFlight satın alma doğrulamaları ayrı gerekliliklerdir.

Kaynak bilgi: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
