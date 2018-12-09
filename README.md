<!DOCTYPE html>
<html lang="pl">

<head>
<meta charset="utf-8"/>
<title> A czas leci </title>

<script type="text/javascript">

function odlicz()

{

    var dzis = new Date();

    var dzien = dzis.getDate();
    if(dzien<10) dzien = "0"+dzien;

    var miesiac = dzis.getMonth()+1;
    if(miesiac<10) miesiac = "0"+miesiac;

    var rok = dzis.getFullYear();
    if(rok<10) rok = "0"+rok;

    var godzina = dzis.getHours();
    if(godzina<10) godzina = "0"+godzina;

    var minuta = dzis.getMinutes();
    if(minuta<10) minuta = "0"+minuta;

    var sekunda = dzis.getSeconds();
    if(sekunda<10) sekunda = "0"+sekunda;

    document.getElementById("zegarek").innerHTML = dzien+"/"+miesiac+"/"+rok+ " | " +godzina+":"+minuta+":"+sekunda;     // Konkatenacja - klejenie łańcuchów

    setTimeout("odlicz()", 1000);

}

</script>



</head>

<body onload="odlicz();">

<div id="zegarek"></div>

</body>

</html>
