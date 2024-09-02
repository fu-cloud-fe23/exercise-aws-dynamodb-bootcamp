# AWS DynamoDB Bootcamp

Övningar där man får testa att använda sig av DynamoDB

## Nivå 1 : Studentdatabas

* Steg 1: Skapa manuellt upp en ny DynamoDB-databas där du lägger in 3 studenter med attributen *student_id*, *name*, och *e-mail*. 
* Steg 2: Skapa en vanlig lambdafunktion som kopplar upp sig mot databasen och som hämtar alla studenter. Koppla ihop den med API Gateway för att göra ditt anrop.
* Steg 3: Skapa ytterligare en lambdafunktion som med hjälp av pathParameters skall hämta och returnera en specifik student. Koppla ihop den med API Gateway för att göra ditt anrop.

## Nivå 2: Todo-API

Använd dig av Severless Framework och bygg om ditt Todo API så att du kan utföra alla CRUD-anrop från dina lambdafunktioner mot en databastabell.

## Nivå 3: Where it's @ - API AWS edition v2.0! - Veckans Code Review Uppgift!

I version 2 av denna övning ska du ta ditt API och göra om ditt API så du använder en DynamoDB-databas för att spara evenemangen och köpa biljetter.

### Funktionalitet

Det ska finnas endpoints för följande:
* Det ska gå att kunna hämta alla evenemang.
* Kunna beställa en biljett för ett evenemang och få tillbaka information om det evenemanget samt biljettnummer.
* Kunna verifiera ett biljettnummer. Det ska även kollas att detta biljettnummer finns samt att det inte redan blivit verifierat d.v.s ett biljettnummer kan bara bli verifierat en gång. Om något av detta inte stämmer ska det resultera i ett felmeddelande som svar. (Här kan ni antingen använda er av ytterligare en tabell, eller kombinera pk och sk för att lagra allt i samma tabell)

#### Level ups
* Lägg till så det finns ett visst antal biljetter på varje evenemang. När man lägger en beställning så dras en biljett från totalen. Ifall det är slutsålt kan man inte köpa en biljett. Här får du lägga till i din databas att det finns ett viss antal biljetter på varje evenemang.
* En admin skall kunna lägga till nya evenemang
* En admin skall kunna ta bort evenemang
* En admin skall kunna uppdatera ett evenemang
