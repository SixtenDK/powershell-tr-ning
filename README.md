### Hvad er PowerShell?
PowerShell er et kommandolinje-interface og scriptsprog fra Microsoft, der er designet til automatisering af administrative opgaver. Det bruges ofte til systemadministration, netværksstyring og automation på tværs af Windows-systemer, og det fungerer også på Linux og macOS. PowerShell kan bruges til at arbejde med filer, systemprocesser og netværksressourcer på en kraftfuld og fleksibel måde.

### PowerShell Grundlæggende Kommandoer
- **Get-Command**: Viser alle tilgængelige kommandoer.
  ```powershell
  Get-Command
  ```
- **Get-Help**: Viser hjælp til en specifik kommando.
  ```powershell
  Get-Help Get-Command
  ```
- **Get-Service**: Viser en liste over tjenester på computeren.
  ```powershell
  Get-Service
  ```

### Opgaver til at komme i gang

#### Opgave 1: Introduktion til PowerShell-kommandoer
Formål: Lær at bruge grundlæggende PowerShell-kommandoer og hjælp.
1. Åbn PowerShell.
2. Kør kommandoen `Get-Command` for at se alle tilgængelige kommandoer.
3. Brug `Get-Help Get-Command` for at få hjælp til, hvad `Get-Command` gør.
4. Prøv at køre kommandoen `Get-Service` for at se, hvilke tjenester der kører på din maskine.

#### Opgave 2: Arbejde med filer og mapper
Formål: Lær at navigere og arbejde med filer og mapper.
1. Brug `Get-ChildItem` for at liste alle filer og mapper i din aktuelle placering.
   ```powershell
   Get-ChildItem
   ```
2. Skift til en anden mappe med `Set-Location`. Du kan fx skifte til skrivebordet.
   ```powershell
   Set-Location C:\Users\DitBrugernavn\Skrivebord
   ```
3. Opret en ny mappe ved hjælp af `New-Item`.
   ```powershell
   New-Item -Path . -Name "MinMappe" -ItemType Directory
   ```
4. Opret en tekstfil i den nye mappe med `New-Item`.
   ```powershell
   New-Item -Path .\MinMappe -Name "fil.txt" -ItemType File
   ```

#### Opgave 3: Arbejde med variabler og loops
Formål: Lær at bruge variabler og loops i PowerShell.
1. Opret en simpel variabel og tilføj en værdi til den.
   ```powershell
   $navn = "PowerShell"
   ```
2. Brug `Write-Output` til at udskrive værdien af din variabel.
   ```powershell
   Write-Output $navn
   ```
3. Opret en `for`-loop, der tæller fra 1 til 5 og udskriver tallet ved hver iteration.
   ```powershell
   for ($i=1; $i -le 5; $i++) {
       Write-Output $i
   }
   ```

Disse opgaver vil hjælpe dig med at forstå grundlæggende PowerShell-syntaks og give dig praktisk erfaring med nogle af de mest anvendte funktioner i PowerShell. Fortsæt med at eksperimentere og udforsk flere kommandoer ved at bruge `Get-Help` til at få mere detaljeret information om, hvad du kan gøre i PowerShell.