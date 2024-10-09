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