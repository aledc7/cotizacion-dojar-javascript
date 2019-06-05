# Cotizacion-dojar-javascript
[![aledc.com](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/aledc.com.svg)](https://aledc.com)
[![License](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/mit-license.svg)](https://aledc.com)
[![GitHub release](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/release.svg)](https://aledc.com)
[![Dependencies](https://github.com/aledc7/Scrum-Certification/blob/master/recursos/dependencias-none.svg)](https://aledc.com)



### Cotización del dolar Oficial 


### el código consume la siguiente API:  
http://ws.geeklab.com.ar/dolar/get-dolar-json.php


La api es consumida con javascript, luego mostrada en pantalla.

Eso es todo.






```js
<html>
<head>
<meta charset="iso-8859-1" >

<title>Test API dolar json</title>

<script language="JavaScript" type="text/javascript" >

function get_data(url){
  var result = '';

  var xmlhttp = new XMLHttpRequest();
  xmlhttp.overrideMimeType("application/json");
  xmlhttp.open("GET",url,false);
  xmlhttp.onreadystatechange = function()
  {
    if (xmlhttp.readyState == 4 && xmlhttp.status == 200)
    {
      result = xmlhttp.responseText;
    }
  }
  xmlhttp.send(null);
  result = JSON.parse(result);
  return result;
}

</script>

</head>
<body>
<br>
<br>
<br>
<br>
<script language="JavaScript" type="text/javascript" >

var url = 'http://ws.geeklab.com.ar/dolar/get-dolar-json.php';

var data_json = get_data(url);

document.write('<h4><b>Dolar Oficial: </b>' + data_json.libre + '</h4>');
document.write('<h4><b>Dolar blue: </b>' + data_json.blue + '</h4>');

//alert('LIBRE: ' + data_json.libre + '\n' + 'BLUE: ' + data_json.blue);

</script>

<p>Ale DC</p>
<a href="http://github.com/aledc7" target="_blank">github</a>

</body>
</html>

```
