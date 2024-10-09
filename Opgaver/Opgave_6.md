### Opgave 6: Automatisering af brugerkonti

#### Problemformulering:
Din virksomhed ansætter mange nye medarbejdere, og du har brug for at oprette brugerkonti automatisk. Skriv et PowerShell-script, der opretter nye brugerkonti baseret på en liste med navne, indlæser dataene fra en CSV-fil, og automatisk tildeler adgang til en standardgruppe.

#### Instruktioner:
1. Brug `Import-Csv` til at indlæse en CSV-fil med oplysninger om medarbejderne (fx navn og afdeling).
2. Brug `New-ADUser` (Active Directory) til at oprette nye brugere.
3. Tilføj hver bruger til en standardgruppe med `Add-ADGroupMember`.
   ```powershell
   $employees = Import-Csv -Path "C:\path\to\employees.csv"
   foreach ($employee in $employees) {
       $username = $employee.FirstName + "." + $employee.LastName
       New-ADUser -Name $username -GivenName $employee.FirstName -Surname $employee.LastName -Department $employee.Department -SamAccountName $username -UserPrincipalName "$username@domain.com" -AccountPassword (ConvertTo-SecureString "DefaultPassword123" -AsPlainText -Force) -Enabled $true
       Add-ADGroupMember -Identity "StandardGroup" -Members $username
   }
   ```