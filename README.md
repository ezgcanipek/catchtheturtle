rastgele kullanici cevirme:

    import requests

     def rastgele_kullanici():
      url = "https://randomuser.me/api/"
    response = requests.get(url)
    
    if response.status_code == 200:
        data = response.json()
        kullanici = data['results'][0]
        
        ad = kullanici['name']['first']
        soyad = kullanici['name']['last']
        cinsiyet = kullanici['gender']
        email = kullanici['email']
        ulke = kullanici['location']['country']
        
        print(f"Ad: {ad} {soyad}")
        print(f"Cinsiyet: {cinsiyet.capitalize()}")
        print(f"E-posta: {email}")
        print(f"Ülke: {ulke}")
    else:
        print("Bir hata oluştu. Lütfen tekrar deneyin.")

     rastgele_kullanici()
