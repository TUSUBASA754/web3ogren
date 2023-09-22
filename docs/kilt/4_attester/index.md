---
id: attester
title: Attester 🛡️
---

# Attester 

Bu başlık altında, attester bireyinin ne tür işlemler gerçekleştireceğini öğreneceğiz.

![alternative text](../../../static/img/kilt/attesterr.jpeg "Welcome")

1. **Ödeme Hesabı Oluşturma:**  Öncelikle attestation işlemleri için oluşacak ödemeleri gerçekleştirmek üzere bir hesap oluşturacağız. 💳
2. **DID Kimlik Oluşturma:** İkinci adımda, bir DID oluşturacağız. Bu DID, attestation işlemleri için kullanılacak kimliğimiz olacak. 🆔

:::tip DID ve Hesaplar Doğrudan bağlı değil! 
Zincir üzerindeki depozito ve işlem ücretlerini farklı bir cüzdan adresi ile de gerçekleştirebiliriz, fakat DID'miz güvenilirlik kaynağımız olduğu için bu adres sabit kalacaktır.
:::

3. **CTYPE Tanımlama:** Attest etmeye başlamadan önce, neyi ve nasıl attest edeceğimizi belirten bir CTYPE'a ihtiyacımız olacak. 📋
4. **Attestation İşlemlerine Başlangıç:** İşlem ücretleri ve depozitolar için bir ödeme yöntemi belirledikten ve uygun bir CTYPE bulduktan sonra, attestation işlemlerine başlayabiliriz. 🚀

## Dosya Mimarisi 🗂️

Aşağıda attester klasörü içerisine ekleyebileceğimiz dosyaları görüyorsunuz. Her bir dosya, farklı bir Attester işlevini temsil eder.

```bash
└─ kilt-rocks/ # proje klasörü 📁
  └─ attester/ # tüm attester kodları 👩‍💻👨‍💻
     ├─ attestCredential.ts # attestation'ları onaylama kodu ✅
     ├─ ctypeSchema.ts # yerelde bir CTYPE şeması oluşturma 📑
     ├─ generateAccount.ts # attester hesabı ve DID oluşturmak 🌐
     ├─ generateCtype.ts # CTYPE'ı zincire kaydetmek 📊
     ├─ generateDid.ts # Attester'ın zincir üzerinde kayıtlı DID'sini oluşturmak 🆔
     └─ generateKeypairs.ts # Attester için anahtarlar oluşturmak 🔐
```
