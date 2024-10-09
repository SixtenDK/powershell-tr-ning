### Opgave 5: Overvågning af diskplads

#### Problemformulering:
Som systemadministrator skal du overvåge diskplads på flere servere. Lav et PowerShell-script, der kan overvåge diskforbruget på en computer, og hvis ledig diskplads falder under 10 %, skal scriptet sende en advarsel til dig.

#### Instruktioner:
1. Brug `Get-PSDrive` til at hente information om diskplads.
2. Beregn den procentvise ledige diskplads for hver drev.
3. Hvis ledig diskplads er under 10 %, brug `Write-Warning` til at vise en advarsel på skærmen.
   ```powershell
   $drives = Get-PSDrive -PSProvider FileSystem
   foreach ($drive in $drives) {
       $freeSpace = ($drive.Used/$drive.Maximum) * 100
       if ($freeSpace -ge 90) {
           Write-Warning "$($drive.Name) har mindre end 10% ledig plads."
       }
   }
   ```