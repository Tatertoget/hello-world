<!DOCTYPE html>

<html>
    <head>
        <meta charset="UTF-8">
        <title>cool</title>
    </head>
    <body>
        <h1>Oblig 1</h1>
        
        <h2>Oppgave 1</h2>
        <?php
            $fornavn = "Per";
            $etternavn = "Hansen";
            $kjønn = "mann";
            $alderOppg1 = "23";
            $adresse = "Osloveien 23";
            $tlfnummer = "12345678";

            if ($kjønn === "mann") {
                echo "$fornavn $etternavn er $alderOppg1 år og bor i $adresse. Han har telefonnummer $tlfnummer.";
            } 
            elseif ($kjønn === "kvinne"){ 
                echo "$fornavn $etternavn er $alder år og bor i $adresse. Henne har telefonnummer $tlfnummer.";
            }
            else{
                echo "$fornavn $etternavn er $alder år og bor i $adresse. Hen har telefonnummer $tlfnummer.";
            }
        ?>
        <!--Slutt oppgave 1 -->
        <h2>Oppgave 2</h2>
        <?php
            $alder = 105;
            if ($alder < 0){
                echo "Du er under 0 år og <strong>ikke engang påtenkt</strong>";
            }
            elseif ($alder >= 0 and $alder < 18 ){
                echo "Du er mindre enn 18 år og <strong>umyndig</strong>";
            }
            elseif ($alder >= 18 and $alder <67){
                echo "Du er 18 år eller mer og <strong>myndig</strong>";
            }
            elseif ($alder >= 67 and $alder <105){
                echo "Du er 67 år eller mer og <strong>pensjonist</strong>";
            }
            elseif ($alder >= 105){
                echo "Du er 105 år eller mer og et <strong>mirakel</strong>";
            } 
        ?>
        <!--Slutt oppgave 2 -->
        <h2>Oppgave 3</h2>
        <?php
            $temperatur = 21;
            $frysepunkt = 0;
            $kokepunkt = 100;
                echo "Temperatur = $temperatur<br/>";
                echo "Frysepunkt = $frysepunkt<br/>";
                echo "Kokepunkt = $kokepunkt<br/>";
            if ($temperatur < $kokepunkt and $temperatur < $frysepunkt){
                echo "Temperaturen er under kokepunket og frysepunktet";
            }
            elseif ($temperatur === $frysepunkt){
                echo "Temperaturen er på frysepunktet. Dermed også under kokepunktet.";
            } 
            elseif ($temperatur > $frysepunkt and $temperatur < $kokepunkt){
                echo "Temperaturen er over frysepunktet, men under kokepunktet.";
            }
            elseif ($temperatur > $frysepunkt and $temperatur >= $kokepunkt){
                echo "Temperaturen er over frysepunktet og kokepunktet";
            }
            echo "<br/>";
            if($temperatur >= 20 and $temperatur <=25){
                echo "Dette er en behagelig sommertemperatur!";
            }

        ?>
        <!--Slutt oppgave 3 -->
        <h2>Oppgave 4</h2>
        
        
        <h3>For-loop</h3>
        <?php
            for ($teller1=0, $max=100; $teller1 <= $max; $teller1++){
                if (($teller1 % 3) == 0){
                    echo $teller1." ";

                }
            }
            echo"<h3>While-loop</h3>";

            $teller2 = 0;
            while($teller2<100) {
                echo "$teller2"." ";
                $teller2=$teller2+3;
            }
            echo"<h3>Sum</h3>";
            $sum = 0;
            for ($teller3=0; $teller3 <=100; $teller3++) {
                if ($teller3 % 3 == 0) {

                    $sum += $teller3;
                }
            }
            echo $sum." ";

            echo"<h3>Gjennomsnitt</h3>";
            $gjennomsnitt= $sum/34;
            echo $gjennomsnitt;
            
        
        ?>
        
        
        <!--Slutt oppgave 4 -->
        <h2>Oppgave 5</h2>
        
        <?php
            echo "<table border=2 width=30% >";
            echo"<tr>";
            echo"<td> :) </td>";
            for($teller1 = 0; $teller1 <= 10; $teller1++) {
                echo "<td>".$teller1."</toppRad>";
            }
            for ($teller1=0;$teller1 <= 10;$teller1++){
                echo"<tr>";
                echo"<td>".$teller1."</td>";
                for ($teller2=0;$teller2 <= 10;$teller2++){
                    $produkt = $teller1 * $teller2;
                    echo "<td>"."<strong>$produkt</strong>"."</td>" ;
                }
                echo"</tr>";
            }
            echo"</table>";
        ?>
        <!--Slutt oppgave 5 -->
        <h1>Oppgave 6</h1>
        <?php
            $balance=10000;
            $interest=(3/100)+1; 
            for($year=0; $year<=7; $year++){
                echo"Etter $year år i banken, med ei rente på 3%, har du en total på $balance kr.</br>";
                $balance=$balance*$interest;
            }
        ?>
        
    </body>
</html>
