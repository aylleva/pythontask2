3b
# 1) salam
def salam():
    print("Salam, Dünya!")

# 2) kub_hesabla
def kub_hesabla(n):
    return n ** 3

# 3) birlesdir
def birlesdir(soz1, soz2):
    return soz1 + " " + soz2

# 4) cap_et
def cap_et(lst):
    for item in lst:
        print(item)

# 5) toplam
def toplam(*args):
    return sum(args)

# 6) ortalama
def ortalama(*args):
    if not args:
        return "Rəqəm yoxdur"
    return sum(args) / len(args)

# 7) adlar_rəqəmlər
def adlar_rəqəmlər(**kwargs):
    for ad, reqem in kwargs.items():
        print(f"ad: {ad}, rəqəm: {reqem}")

# 8) tip_yoxla
def tip_yoxla(dəyər):
    if isinstance(dəyər, str):
        print("mətn")
    elif isinstance(dəyər, (int, float)):
        print("rəqəm")
    else:
        print("başqa")

# 9) yas_kateqoriya
def yas_kateqoriya():
    yas = int(input("Yaşınızı daxil edin: "))
    if yas < 18:
        print("Gənc")
    else:
        print("Yetkin")

# 10) soz_uzunluq
def soz_uzunluq():
    soz = input("Söz daxil edin: ")
    print("Uzunluq:", len(soz))
3a
# 1) x dəyişəni
def yoxla_x(x):
    if x > 0:
        print("müsbət")
    elif x < 0:
        print("mənfi")
    else:
        print("sıfır")

# 2) cüt və ya tək
def cut_ve_ya_tek(n):
    if n % 2 == 0:
        print("cüt")
    else:
        print("tək")

# 3) ən böyük
def en_boyuk(a, b, c):
    print(max(a, b, c))

# 4) həftə günü
def heftenin_gunu(day):
    gunler = {
        1: "Bazar ertəsi", 2: "Çərşənbə axşamı", 3: "Çərşənbə",
        4: "Cümə axşamı", 5: "Cümə", 6: "Şənbə", 7: "Bazar"
    }
    print(gunler.get(day, "Yanlış gün"))

# 5) temperatur
def temperatur_yoxla(temp):
    if temp < 0:
        print("soyuq")
    elif 0 <= temp <= 20:
        print("normal")
    else:
        print("isti")

# 6) şifrə uzunluğu
def sifre_uzunlugu(password):
    if len(password) < 8:
        print("qısa")
    elif 8 <= len(password) <= 12:
        print("orta")
    else:
        print("uzun")

# 7) 3 və 5 bölünmə
def bolunme_yoxla(x):
    if x % 3 == 0 and x % 5 == 0:
        print("3 və 5")
    elif x % 3 == 0:
        print("3")
    elif x % 5 == 0:
        print("5")
    else:
        print("heç biri")

# 8) 0-dan 20-yə qədər cütlər
def cutler_0_20():
    for i in range(0, 21, 2):
        print(i)

# 9) stringin hər elementi
def string_elementleri():
    metn = "Bağda ərik var idi …"
    for herf in metn:
        print(herf)

# 10) 1-dən 10-a, 3 xaric
def reqemler_3_xaric():
    for i in range(1, 11):
        if i == 3:
            continue
        print(i)

# 11) 5-ə bölünən ilk ədəd
def ilk_5e_bolunen():
    i = 1
    while True:
        if i % 5 == 0:
            print(i)
            break
        i += 1

# 12) 5-in indeksi
def indeks_tap():
    lst = (1, 3, 5, 7, 9)
    for i in range(len(lst)):
        if lst[i] == 5:
            print("İndeks:", i)
            break

4a
# 1) Hesablayıcı
def hesablayici():
    try:
        a = float(input("Birinci rəqəm: "))
        b = float(input("İkinci rəqəm: "))
        operation = input("Əməliyyat (+, -, *, /): ")
        if operation == '+':
            print("Nəticə:", a + b)
        elif operation == '-':
            print("Nəticə:", a - b)
        elif operation == '*':
            print("Nəticə:", a * b)
        elif operation == '/':
            print("Nəticə:", a / b)
        else:
            print("Yanlış əməliyyat.")
    except ZeroDivisionError:
        print("0-a bölmək olmaz.")
    except ValueError:
        print("Yalnız rəqəm daxil edin.")
    except Exception as e:
        print("Xəta baş verdi:", str(e))
    finally:
        print("Hesablama bitdi.")

# 2) 1-50 arası 11-ə bölünənlər
def on_bire_bolunen():
    return [i for i in range(1, 51) if i % 11 == 0]

# 3) Sözlərin ilk hərfləri
def ilk_herfler():
    sozler = ["kitab", "qələm", "defter", "silgi"]
    return [soz[0] for soz in sozler]

# 4) Şəhər və kodları dictionary
def seher_kod_dict():
    seherler = ["Bakı", "Gəncə", "Sumqayıt"]
    kodlar = [12, 22, 18]
    return dict(zip(seherler, kodlar))

# 5) Lambda ilə km-dən milə
def km_to_mil():
    km_to_mile = lambda km: km * 0.621371
    dəyərlər = [1, 5, 10, 15, 20]
    for km in dəyərlər:
        print(f"{km} km = {km_to_mile(km):.2f} mil")

# 6) Qiymətlərə 18% vergi əlavə et
def vergi_əlavə_et():
    qiymetler = [100, 200, 300, 400]
    return list(map(lambda x: x * 1.18, qiymetler))

# 7) İki siyahı, ikiqat artır və cəmlə
def ikiqat_ve_toplam():
    list1 = [3, 7, 12]
    list2 = [2, 4, 6]
    ikiqat1 = list(map(lambda x: x * 2, list1))
    ikiqat2 = list(map(lambda x: x * 2, list2))
    return sum(ikiqat1 + ikiqat2)

# 8) Reduce ilə minimum
from functools import reduce
def en_kicik_tap():
    qiymetler = [150, 80, 220, 45]
    return reduce(lambda x, y: x if x < y else y, qiymetler)
            
    
