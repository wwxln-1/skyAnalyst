# ✈️ SkyAnalyst — BritAir Flight Data Analytics

Ushbu loyiha **BritAir** aviakompaniyasi uchun 2023–2024 yillardagi parvoz ma'lumotlarini tahlil qilishga bag'ishlangan. Loyiha ma'lumotlarni tavsiflovchi (descriptive), bashoratlovchi (predictive) va me'yorlovchi (prescriptive) tahlil bosqichlaridan iborat bo'lib, kechikishlar, yo'lovchilar mamnuniyati va narxlash omillarini o'rganadi.

## 📊 Loyiha haqida

Jupyter Notebook (`SkyAnalyst.ipynb`) quyidagi bosqichlarni o'z ichiga oladi:

1. **Ma'lumotlarni yuklash va tuzilishini o'rganish** — dataset shakli, ustunlar turlari (nominal, ordinal, uzluksiz, diskret)
2. **Analitika terminologiyasi** — populyatsiya, tanlanma (sample) va ularning tatbiqi
3. **Tahlil turlari** — descriptive, predictive va prescriptive analitika misollari
4. **Ma'lumotlarni tozalash** — bo'sh qiymatlarni aniqlash va to'ldirish strategiyalari
5. **Tavsiflovchi statistika** — markaziy tendensiya, tarqalish ko'rsatkichlari
6. **Eksploratsion tahlil (EDA)** — gistogrammalar, taqsimotlar
7. **Ikki o'zgaruvchili tahlil** — kechikish va mamnuniyat o'rtasidagi bog'liqlik
8. **Tanlanma taqqoslash** — 10% tasodifiy tanlanma populyatsiya bilan solishtirilishi
9. **Regressiya modellari** — oddiy va ko'p o'zgaruvchili chiziqli regressiya (masofa → kechikish)
10. **Vaqt qatorlari prognozi** — oylik o'rtacha kechikish tendensiyasi va harakatlanuvchi o'rtacha (MA3)

## 📁 Fayllar tuzilishi

```
├── SkyAnalyst.ipynb                # Asosiy tahlil notebook fayli
├── SkyAnalytics_FlightData.csv     # Parvoz ma'lumotlari (5000 qator, 21 ustun)
└── README.md
```

## 🗂️ Dataset haqida

`SkyAnalytics_FlightData.csv` fayli 2023–2024 yillar oralig'idagi **5000 ta parvoz** haqida ma'lumotlarni o'z ichiga oladi:

| Ustun | Tavsif |
|---|---|
| `flight_id` | Parvoz identifikatori |
| `flight_date`, `month`, `season`, `day_of_week` | Sana bilan bog'liq ma'lumotlar |
| `airline`, `aircraft_type` | Aviakompaniya va samolyot turi |
| `origin_airport`, `destination_airport`, `route` | Marshrut ma'lumotlari |
| `distance_km` | Masofa (km) |
| `scheduled_departure` | Rejalashtirilgan uchish vaqti |
| `departure_delay_min`, `arrival_delay_min` | Uchish va qo'nish kechikishlari (daqiqa) |
| `actual_elapsed_min`, `scheduled_duration_min` | Haqiqiy va rejalashtirilgan parvoz davomiyligi |
| `delay_cause` | Kechikish sababi |
| `cancelled` | Parvoz bekor qilinganligi (0/1) |
| `passengers_onboard` | Bortdagi yo'lovchilar soni |
| `ticket_price_gbp` | Chipta narxi (GBP) |
| `satisfaction_score` | Yo'lovchi mamnuniyat balli |

## 🛠️ Ishlatilgan texnologiyalar

- Python 3
- pandas, numpy — ma'lumotlarni qayta ishlash
- matplotlib, seaborn — vizualizatsiya
- scikit-learn — chiziqli regressiya modellari (`LinearRegression`, `train_test_split`, `r2_score`)

## 🚀 Ishga tushirish

```bash
git clone <repo-url>
cd <repo-nomi>
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook SkyAnalyst.ipynb
```

> **Eslatma:** Notebook ichida `df = pd.read_csv('SkyAnalytics_FlightData_2023_2024.csv')` qatori mavjud — bu qatorni repozitoriydagi haqiqiy fayl nomiga, ya'ni `SkyAnalytics_FlightData.csv` ga moslashtiring, aks holda fayl topilmaydi xatosi chiqadi.

## 📈 Asosiy natijalar (qisqacha)

- Kechikishlar taqsimoti **o'ngga siljigan** (right-skewed) — ko'pchilik parvozlar o'z vaqtida yoki ozgina kechikadi, lekin kam sonli parvozlar juda uzoq kechikadi.
- Kechikish va yo'lovchi mamnuniyati o'rtasida **salbiy korrelyatsiya** kuzatiladi.
- 10% tasodifiy tanlanma statistikalari populyatsiya statistikalariga yaqin — bu tanlanmaning ishonchli ekanligini ko'rsatadi.
- Chiziqli regressiya modeli masofa va narx asosida kechikishni bashorat qilishga urinadi, biroq R² ko'rsatkichi cheklangan bashoratlash kuchini ko'rsatadi.

## 📄 Litsenziya

Ushbu loyiha ta'lim maqsadida yaratilgan.
"# skyAnalyst " 
