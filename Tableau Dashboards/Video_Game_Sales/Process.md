<h1>Creating Parameters and Calculated Fields</h1>
Create Parameter = "Zone sales" <br>
Create Calculated Field = "Zone Sales" <br>
Calculated field Code:<br><br>
CASE [Zone sales]<br>
WHEN "EU Sales" THEN [EU Sales]<br>
WHEN "Global Sales" THEN [Global Sales]<br>
WHEN "JP Sales" THEN [JP Sales]<br>
WHEN "NA Sales" THEN [NA Sales]<br>
WHEN "Other Sales" THEN [Other Sales]<br>
END<br>
<br>
Create Parameter = "Start date", "End date"<br>
Create Calculated Field = "Study Period"<br>
Calculated field code:<br><br>
IF [Year] >= [Start date] AND [Year] <= [End date] THEN 1<br>
ELSE 0<br>
END<br><br>
Convert "Study Period" to dimension by right-clicking after applying the code.
