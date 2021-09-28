**OBS:** Det här är ett komplement till en inspelad föreläsning.

## Vad är tester?

Ett "test" är en bit kod, precis som all annan Java-kod vi använder. Just nu kommer vi fokusera på JUnit, ett verktyg vi använder för att göra "unit-tester", eller "enhetstester". Syftet med enhetstester är att testa mindre bitar kod individuellt.

Det finns även andra sorters tester, som systemtester och integrationstester, vilket handlar om hur hela vårt program fungerar som helhet (systemtester), eller för att testa hur vårt program fungerar getenmot andra program (integrationstester).

Systemtester och integrationstester kan vara mycket värdefulla, men de är ofta mycket mer komplicerade än enhetstester.

## Vad är JUnit?

JUnit är ett ramverk för att göra enhetstester i Java. 

## Hur och när använder vi tester?

Vi börjar med att skriva ett enkelt program där vi använder oss av metoder. En metod tar ofta några argument, och retunerar någonting baserat på vad vi matade in.

## Vad är Gradle? Vad är Maven?

Maven och Gradle är hjälpredor som gör saker åt oss i våra projekt. Den hjälper till med beroenden (importer vi gör som är utanför standardbiblioteket - något vi inte gjort tidigare men som kommer senare i er Java-användning) och kör tester åt oss.

Maven och Gradle löser samma problem på lite olika sätt. Maven är en gammal klassiker, medan Gradle är lite mer modern och konfigurationsfilerna är mycket mer lättlästa, vilket är varför vi fokuserar på Gradle just nu.

Gradle är vad du använder om du gör Android-projekt.

# Exempel

## Förberedelser

* Skapa ett nytt projekt och kryssa i rutan om att vi vill använda Gradle
* Bekräfta att vår Gradle-fil (`build.gradle`) innehåller de beroenden ("dependencies") vi behöver och konfigurationen för att köra JUnit (se nedan)
* Skapa ett paket under main/java och döp det till exempelvis `com.jensen.caws21.testexempel`
* Skapa en klass i det paketet och döp det till exempelvis `MittProjekt`
* Skapa ett till paket under test/java och ge det precis samma namn som det under main/java
* Skapa en klass i paketet under test/java och döp det till precis samma sak som det under main/java fast med ordet "Test" efter, exempelvis `MittProjektTest`

build.gradle:

    plugins {
        id 'java'
    }

    group 'com.jensen.caws21.mittprojekt'
    version '1.0-SNAPSHOT'

    repositories {
        mavenCentral()
    }


    dependencies {
        testImplementation 'org.junit.jupiter:junit-jupiter-api:5.7.0'
        testRuntimeOnly 'org.junit.jupiter:junit-jupiter-engine:5.7.0'
    }

    test {
        useJUnitPlatform()
    }

# Annat material om tester

## JUnit med Maven (alternativ till Gradle, men fokusera på de andra bitarna)
* https://www.youtube.com/watch?v=flpmSXVTqBI Java Testing - JUnit 5 Crash Course 
* https://programmingtechie.com/2020/12/26/junit-5-complete-tutorial/