## **Statikus osztály és statikus metódusok működése**



###### **1. A program felépítése**

A program két fő részből áll:



Messages nevű statikus osztály



Program nevű osztály, amely a Main() metódust tartalmazza





A két osztály együttműködik:



A Messages osztály tárolja az üzeneteket kiíró metódusokat.



A Program.Main() meghívja ezeket a metódusokat, így a program futásakor megjelennek a szövegek a konzolon.





###### **2. A statikus osztály szerepe**

A Messages osztály statikus, ami azt jelenti:



Nem lehet belőle példányt létrehozni (new Messages() nem működik).



Minden benne lévő metódusnak statikusnak kell lennie.



Az osztály célja, hogy közös, bárhonnan elérhető funkciókat biztosítson.



Ebben az esetben a statikus osztály három üzenetet kezel, mindegyik külön metódusban:



Hello() – üdvözlő üzenet



Waiting() – várakozással kapcsolatos üzenet



Bye() – elköszönő üzenet



A statikus osztály így egyfajta üzenetkezelő modul, amelyet a program más részei könnyen használhatnak.





###### **3. A statikus metódusok működése**

A statikus metódusok olyan függvények, amelyeket nem kell példányhoz kötni.

Ezért hívhatók így:



Kód

Messages.Hello();

A hívás felépítése:



Messages → az osztály neve



Hello → a metódus neve



() → a metódus meghívása



Ez a forma azt jelenti:

„Hívd meg a Messages osztály Hello nevű metódusát.”





###### **4. A Program osztály szerepe**

A Program osztály tartalmazza a Main() metódust, amely a program belépési pontja.

Amikor a program elindul, a Main() fut le először.



A Main() feladata:



Meghívni a Messages.Hello() metódust



Meghívni a Messages.Waiting() metódust



Meghívni a Messages.Bye() metódust



Várni egy billentyűlenyomásra (Console.ReadKey())



Ez a sorrend határozza meg a program futását.





###### **5. A program futásának menete**

Amikor elindítod a programot, a következő történik:



A konzolra kiíródik:

"Hello welcome to my program!"



Ezután megjelenik:

"I am waiting for something"



Majd kiíródik:

"Bye! Thanks for visiting"



A program megáll, és vár, hogy lenyomj egy billentyűt.

Csak ezután záródik be.





###### **6. A program célja**

A program bemutatja:



hogyan lehet statikus osztályt létrehozni,



hogyan lehet statikus metódusokat definiálni,



hogyan lehet ezeket példányosítás nélkül meghívni,



hogyan lehet egyszerű üzeneteket megjeleníteni a konzolon.



Ez egy alapvető, de nagyon fontos C# programozási technika, amelyet gyakran használnak:



segédosztályoknál (utility)



üzenetkezelésnél



konfigurációs funkcióknál



matematikai vagy logikai műveleteknél





###### **7. Miért hasznos így felépíteni?**

Átlátható: az üzenetek külön osztályban vannak, nem keverednek a fő programmal.



Moduláris: a Messages osztály bármikor bővíthető új metódusokkal.



Egyszerű hívás: nem kell példány, csak osztálynév + metódusnév.



Tanulás szempontjából fontos: megérted a statikus elemek működését.

