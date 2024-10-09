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