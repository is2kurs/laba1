# laba1
<HTML>
<HEAD>
<BODY>
  <div> ШИФРОВЩИК </div>
<SCRIPT LANGUAGE="JavaScript">
function crypter(message, key, decrypter) {
    var a = "абвгдежзийклмнопрстуфхцчшщъыьэюя".split("");
    message = message.split("") ;
    key = ("" + key).split("") ;
    return message.reduce(function(message, current) {
        var i = a.indexOf(current),
            b = +key.shift();
        key.push(b);
        decrypter ? (i -= b, i < 0 && (i += a.length)) : (i += b, i %= a.length);
        return message + a[i]
    }, "")
};
  document.write(crypter("аааааа", 22)+"<br>")
  </script>
  <div> ДЕШИФРОВЩИК </div>
  <SCRIPT LANGUAGE="JavaScript">
function crypter(message, key, decrypter) {
    var a = "абвгдежзийклмнопрстуфхцчшщъыьэюя".split("");
    message = message.split("") ;
    key = ("" + key).split("") ;
    return message.reduce(function(message, current) {
        var i = a.indexOf(current),
            b = +key.shift();
        key.push(b);
        decrypter ? (i -= b, i < 0 && (i += a.length)) : (i += b, i %= a.length);
        return message + a[i]
    }, "")
};
  document.write(crypter("вввввв", 22, true))
  </script>
</HEAD>
</BODY>
</HTML>
