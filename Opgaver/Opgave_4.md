### Opgave 4: Håndtering af services

#### Problemformulering:
Du er en systemadministrator, og du har bemærket, at nogle af systemtjenesterne på en server ikke starter korrekt ved opstart. For at sikre, at alle nødvendige tjenester kører, vil du skrive et PowerShell-script, der lister alle tjenester, starter dem, der ikke kører, og logger tjenestestatus før og efter handlingerne til en fil for fremtidig fejlfinding.

#### Instruktioner:
1. Brug `Get-Service` til at liste alle tjenester på computeren.
2. Brug en `foreach`-loop til at tjekke status på hver tjeneste.
3. Hvis en tjeneste er stoppet, start den med `Start-Service`.
4. Log tjenestens navn og status (før og efter handlingen) i en tekstfil.
   ```powershell
   $services = Get-Service
   foreach ($service in $services) {
       $statusBefore = $service.Status
       if ($statusBefore -eq 'Stopped') {
           Start-Service $service.Name
       }
       $statusAfter = (Get-Service $service.Name).Status
       Add-Content -Path "C:\log\tjenestelog.txt" -Value "$($service.Name): $statusBefore -> $statusAfter"
   }
   ```