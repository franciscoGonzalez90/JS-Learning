## Apuntes de JavaScript

**Whitespace**

> El espaciado en blanco entre var y that no puede ser eliminado.

```javascript
	var that = this;
	//var rm=/a*/.match('s'); 
```

>  Cuando se utiliza expresiones regulares se debe utilizar "//" para comentar.

```javascript
	//var rm=/a*/.match('s'); 
```


**Names**

> No se  debe utilizar ninguna de estas palabras reservadas

```javascript
	abstract
	boolean break byte
	case catch char class const continue
	debugger default  delete do double
	else enum export extends
	false final finally float for  function
	goto
	if implements import in instanceof int  inteface
	long
	native new null
	package private protected public 
	return
	short static super switch synchronized
	this throw throws transient true try typeof
	var volatile void
	while with
	undefined NaN Infinity
```


> Los nombres solo deben ser usados por bloques, parametros,
> nombres de propiedades, operadores y etiquetas.

```javascript
	var _variable1;
	var otraVariable;
	var Mi_variable_custom;
```

**Numbers**

> NaN es un valor numerico que no puede ser comparado con otro valor ni con el mismo, si no que con la funcion isNaN(number).

> Infinity es el valor que se utiliza para reprensentar valores mas grandes que 1.79769313486231570e+308.

> Number tiene metodos como la libreria Math.floor(number) que es utilizado para convertir numeros en interger.

```javascript
		var a=5;
    	var b=2.4;
    	var c=0.1e+2;
    
    	console.log(c);
    	console.log(Math.floor(2.2));
```


**Strings**

> Un string puede estar conformado por ''(comillas simples) o ""(comillas dobles).

> El \(backslash) es un caracter de escape.

> Una vez que un string esta hecho no se puede desarmar pero si se puede concatenar mas valores con el signo "+".

> Concatenar palabras 'c'+'a'+'t' === 'cat'.