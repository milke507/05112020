# 05112020

<!DOCTYPE html>
<html>

<body>

<h1>WEB SHOP</h1>
<br>

<p>Datum i vrijeme:</p>
<script>
document.write(Date());
</script>
<script language="JavaScript">
<!--
function kuneP(){
document.converter.euro.value = document.converter.kune.value / 7.5
document.converter.dollar.value = document.converter.kune.value / 6
}
function euroP(){
document.converter.kune.value = document.converter.euro.value * 7.5
document.converter.dollar.value = document.converter.euro.value * 1.17
}
function dollarP(){
document.converter.kune.value = document.converter.dollar.value * 6
document.converter.euro.value = document.converter.dollar.value / 1.17
}
//-->
</script>


<br>
<script>
var zbroj=0;
function monitor()
{
var obj=document.getElementById("p1");
obj.innerHTML=obj.innerHTML+"</br>Monitor";
zbroj=zbroj +500;
}
function mis()
{
var obj=document.getElementById("p1");
obj.innerHTML=obj.innerHTML+"</br>Miš!";
zbroj=zbroj +100;
}
function tipkovnica()
{
var obj=document.getElementById("p1");
obj.innerHTML=obj.innerHTML+"</br>Tipkovnica!";
zbroj=zbroj +250;

}
function racun()
{
var obj=document.getElementById("p1");
obj.innerHTML=obj.innerHTML+"</br>Račun iznosi "+zbroj+"$";
document.converter.dollar.value = zbroj;
document.converter.euro.value = zbroj / 1.17;
document.converter.kune.value = zbroj*6;
}
function isk()
{
var obj=document.getElementById("p1");
obj.innerHTML="";
zbroj=0;
document.converter.dollar.value = "0";
document.converter.euro.value ="0";
document.converter.kune.value = "0";
}
</script>


<h1>PROIZVODI</h1>
<p id="monitor">Monitor(500$) </p>
<input type="button" onClick="monitor()" value="Kupi"/>
<p id="mis">Miš(100$) </p>
<input type="button" onClick="mis()" value="Kupi"/>
<p id="tipkovnica">Tipkovnica(250$) </p>
<input type="button" onClick="tipkovnica()" value="Kupi"/>



<p id="p1">Račun</p>
<input type="button" onClick="racun()" value="RAČUN"/>
<input type="button" onClick="isk()" value="ISPRAZNI KOŠARICU"/>
<form name="converter">
<table border="0">
<tr>
<td>Kune: </td><td><input type="text" name="kune" onChange="kuneP()" /></td>
</tr>
<tr>
<td>Euro: </td><td><input type="text" name="euro" onChange="euroP()" /></td>
</tr>
<tr>
<td>Dolari:</td><td><input type="text" name="dollar" onChange="dollarP()" /></td>
</tr>
</table>
</form>


</body>
</html>
