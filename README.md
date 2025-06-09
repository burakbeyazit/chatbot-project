# Kitap Öneri Chatbotu

## Genel Bakış

Bu proje, **LLM tabanlı (GPT/Open Source) bir kitap öneri ve intent (niyet) sınıflandırma chatbotu**dur.  
Kendi kitap verisetinizi ve intent (niyet) tanımlarınızı kullanarak,  
- Kullanıcıdan gelen soruları otomatik olarak niyetine göre sınıflandırır  
- Kitap önerileri yapabilir ya da kitap hakkında bilgi verebilir  
- GPT-3.5-Turbo (OpenAI) ile açık kaynak Microsoft Phi-3-mini-4k-instruct (HuggingFace) sonuçlarını karşılaştırabilir.
- Modellerin doğruluk, precision, recall ve F1 skorlarını ölçebilirsiniz

## Özellikler

- Veri seti: https://www.kaggle.com/datasets/abdallahwagih/books-dataset  data.csv ve intents.json üzerinden çalışılmıştır
- **İki farklı model:** GPT-3.5-Turbo ve HuggingFace (ör. Phi-3-mini-4k-instruct)
- **Kitap arama ve bilgi getirme:** Fuzzy search desteği ile
- **Gradio tabanlı arayüz:** Web’den kolayca demo & değerlendirme
- **Otomatik metrik değerlendirme:** Precision, recall, F1-score

## Gereksinimler

- Python 3.8+
- Colab veya kendi makineniz
- Gerekli dosyalar requirements.txt dosyasında vardır.
- Google Colab'de rahatlıkla kullanılabilir.

- Dosya Yapısı
├── data.csv                # Kitap veri setiniz (başlık, yazar, açıklama vs.)
├── intents.json            # Intent (niyet) tanımları ve örnekleri
├── main.py                 # Ana kod dosyanız (paylaştığınız script)
├── keys.txt                # API anahtarlarınız (Ayrı, .gitignore'a ekleyin)


## Proje Raporu

Proje: Kitap Öneri Chatbotu – LLM Tabanlı Intent Sınıflandırma ve Model Karşılaştırması
1. Giriş
Bu projede, kullanıcının kitapla ilgili doğal dilde sorduğu soruları anlayıp doğru yanıtı verebilen, iki farklı büyük dil modeli (LLM) ile çalışan bir chatbot geliştirilmiştir. Proje kapsamında hem OpenAI GPT-3.5-Turbo hem de Microsoft tarafından sunulan açık kaynaklı (open source) LLM (ör: Phi-3 Mini) ile intent sınıflandırması ve kitap önerisi karşılaştırmalı olarak test edilmiştir.

2. Yöntem ve Uygulama
Veri Seti:

Kitaplar ve açıklamaları data.csv dosyasında,

Intent (niyet) türleri ve örnek cümleler ise intents.json dosyasında tutulmuştur.

Model Entegrasyonu:

GPT-3.5-Turbo: OpenAI API üzerinden,

Microsoft Open Source LLM (Phi-3 Mini): HuggingFace üzerinden erişilmiştir.

Arayüz:
Kullanıcı dostu web arayüzü Gradio ile sunulmuştur.

Ölçütler:
Modeller, hazır test örneklerinde "precision", "recall", "f1-score" ile ölçülmüştür.

**GPT-3.5-Turbo:**
Precision: 0.73
Recall: 0.80
F1: 0.76

**OpenSource LLM:**
Precision: 0.73
Recall: 0.80
F1: 0.76


GPT-3.5-Turbo, niyet sınıflandırmada ve kitap önerilerinde daha tutarlı ve doğru sonuçlar vermiştir.

Microsoft OS LLM (Phi-3 Mini) ise açık kaynaklı olmasının avantajıyla hızlıca entegre edilebilmiş, ancak bazı karmaşık intentlerde kararsız sonuçlar üretebilmiştir.


