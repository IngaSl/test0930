# test0930 pasitikrinti ar viskas veikia
Gerai, atidaryti terminalą IntelliJ – apačioje Terminal skirtukas.
Įvesti šias komandas po vieną (po kiekvienos paspauskite Enter ir palaukite):
1.
git add .
2.
git commit -m "Add Selenium POM tests"
3.
git remote add origin https://github.com/IngaSl/Bandomasis-egzaminas.git
4.
git push -u origin main
Jei po 4 komandos paprašo prisijungimo – įveskite GitHub vartotojo vardą ir slaptažodį (arba token, jei naudojate).

file:///C:/Users/Inga%C5%A0li%C5%BEien%C4%97/Downloads/egzamino_ruosinys_selenium_java.html

POM – tai projektavimo šablonas, kuriame kiekvienas puslapis aprašomas atskiroje klasėje. 
Lokatoriai (kaip rasti elementą) ir veiksmai (ką daryti) yra atskirti nuo pačių testų. 
Tai leidžia keičiant UI atnaujinti tik vieną vietą, o ne visus testus.

Thread.sleep() laukia fiksuotą laiką – per lėta arba per trumpa. 
Vietoj jo naudojame WebDriverWait, kuris laukia tol, kol elementas atsiranda. Tai greitesnė ir patikimesnė alternatyva.

Tipinė POM struktūra:
src/
  test/
    java/
      pages/          ← puslapių klasės (LoginPage, RegisterPage...)
      tests/          ← testų klasės (LoginTest, CrudTest...)
      utils/          ← pagalbiniai įrankiai (DriverFactory, TestData...)
    resources/
      testng.xml      ← testų konfigūracija
pom.xml               ← Maven priklausomybės

Kas yra @BeforeMethod ir @AfterMethod?
Tai TestNG anotacijos, kurios paleidžia kodą prieš ir po kiekvieno testo. Naudojamos naršyklei atidaryti ir uždaryti.
