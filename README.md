## Wiki de JavaScript

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

> Concatenar palabras 'c'+'a'+'t' === 'cat'(TRUE).

```javascript
		console.log("\u0041");
    	console.log(("\u0041").length);
    	console.log("CAT".toLowerCase());	
```


**Statments**

> Cuando un statments esta dentro de una funcion este pasa a ser una variable privada.

> Statments tienden a ser ejecutadas en orden desde arriba hacia abajo.

> Las varibles deben estar definidas al comienzo, no en los bloques.

```javascript
		var variable = "asignacion";
```


**Statments - IF**

> if(expression){block;}else{block;}

> valores falsos: false, null, undefined, empty string(''), number 0 the number NaN.

> valores verdaderos: include, true, the string 'false' and all objects.

```javascript
		if(true)
		{
		    console.log('its true');
		}
		else
		{
		    console.log('false');
		}
```


**Statments - SWITCH**

>  switch(expression){case clause:statments;break; default: statments;}

```javascript
		switch('hi')
		{
        	case 'hi': console.log('say hi');
        	default: console.log('say bye');
        }
```


**Statments - WHILE**

> while(expression){statments;};

> Si la expression es verdadera se ejecuta el statments, si es falso no se ejecuta.

```javascript
			var h=0;
        			
        	while(h < 5){
        		console.log("while verdadero");
        		h++;
        	};
```


**Statments - FOR**

> Existen 2 tipos de for (for-forIn)

```javascript
			var obj=[{nombre:'francisco',apellido:'gonzalez'},{nombre:'cristina',apellido:'caro'}];
			
			for (var i = 0; i < 5; i++)
			 {
            	console.log('for normal');
            };
            
            for(o in  obj)
            {
            	console.log(obj[o].nombre+' '+obj[o].apellido);
            };
           
```


**Statments - DO WHILE**

> El bloque siempre es ejecuta al menos una vez.

```javascript
    	var incrementos=0;
    	
    	do{
    		incrementos++;	
    		console.log('do while');
    	}while(incrementos < 5);
```


**Statments - Try**

> try{block;}catch(variable name);

> El statment try ejecuta un bloque y atrapa alguna excepcion que
> fue lanzada por el bloque. 

>catch define  una nueva variable que 
> recive el objeto excepcion.


**Statments - THROW**

> Invoca una excepcion.

> Si esta dentro de una clausula try se envia directamente al catch , el cual retorna una mensaje.

> El objeto  que retorna entrega el name y el message property.

```javascript
    	var x=NaN;
        
        try
        {
         if(isNaN(x)) throw "Es NaN";
         
        }catch(e)
        {
        	console.log(e);
        };	
```

**Statments - Return**

> Especifica el valor que va a ser retornado.

> Si el valor return no esta especificado este se define por defecto como undefined.

```javascript
    	if(true)
    	{
    		console.log('antes del return');
    		 return; 
    	}
        //esta funcion no se muestra debido a que se lanza un return
    	console.log('despues del return');	
```


**Statments - Delete**

> Elimina una propiedad de un objeto.

> Las variables no pueden ser borradas.

```javascript
    	 _objeto=[
        	{nombre:'francisco',apellido:'gonzalez'},
        	{nombre:'cristina',apellido:'caro'}
        ];
        
        for(ob in _objeto)
        {
        	console.log(_objeto[ob].nombre);
        }
        
        delete _objeto[0];
        
        for(ob in _objeto){
        	console.log(_objeto[ob]);
        }
```


**Expression**

> Una expresion es un valor literal como un string o un number
> o un valor incorporado (true, false, null, undefined, NaN, Infinity)
> una invocacion precedida por new o delete, una expresion entre parentesis
> , una expresion precedida por un operador de prefijo o una expresion seguida
> por un ternario (?).

```javascript
    	foo={};
        foo.bar=123;
        console.log(foo);	
```


**Expressions - Order Precedence**

> Los parentesis son alteradores de la precedencia.

```javascript
	/*
				1.- . [] ()
				2.- delete new typeof + - !
				3.- * / %
				4.- + -
				5.- >= <= > <
				6.- === !==
				7.- &&
				8.- ||
				9.- ?:
	*/
```


**Expressions - typeof**

> Los valores producidos por typeof son 'number', 'string', 'boolean' , 'undefined', 'function' y 'object'.

> Si el operando es un array o null, el resultado es un 'object' lo cual esta malo.

> NaN lo marca como un valor number.

>  Los refinement son usados para especificar la propiedad o elemento de un objeto o array.

```javascript
    	var func=function()
    	{
    		return 'funcion';
    	};
    
    	arr=['nombre','francisco'];
    
    	console.log(typeof(true));			
    	console.log(typeof(3));
    	console.log(typeof('test'));
    	console.log(typeof(arr));
    	console.log(typeof(arr[1])); //string 
    	console.log(typeof({nombre:'francisco'}));
    	console.log(typeof(func));
    	console.log(typeof(NaN));
```


**Literals**

> Los nombres de las propiedades puedes ser especificadas como nombre o strings.

> Los nombres de las propiedades pueden ser conocidos en tiempo de compilacion.

> Los valores de las propiedades son expresiones.

> Los array literales son una forma conveniente de crear nuevos arrays.


```javascript
    	objetoLiteral={nombre:'francisco'};
    	
    	arrayLiteral=['hola','soy','francisco'];
    	
    	function funcionLiteral(){return 'hola'}	
```


**Literals**

> Los objetos en javascript son mutables.

> En JS los arrays son objetos, las funciones son objetos, las expresiones regulares son objetos y los objetos son objetos.

> Un objeto es un contendor de propiedades, definidos por una propiedad
> nombre/valor, el nombre de una propiedad puede ser un string, incluyendo
> un string vacio. La propiedad valor puede ser cualquier valor JS menos
> undefined.

> Los objetos en JS son sin clases. No existen restricciones en los
> nombres de las propiedades de un objeto(clave/valor). Los objetos son
> usados para organizar y coleccionar datos.

> Los objetos puedes contener otros objetos, estos son formas faciles de representar arboles o grafos estructurales de datos.

> JS incluye herencia por prototypes. el cual permite pasar las funcionalidades a otro objeto. 

> Cuando esto es usado de forma correcta reduce el tiempo y el consumo de memoria.


```javascript
      	persona=[{nombre:"francisco"},{nombre:"cristina"}];
      	personas={persona,otraPersona:persona};
      	console.log(persona);
      	console.log(personas);  
```

**Objetc Literals**

> Proveen una conveniente notacion para crear nuevos objetos.

> Un objeto literal esta conformado por un par de llaves {} teniendo
> cero o más(name/value) datos.

> (nombre/valor) El nombre puede tener o no comillas dobles, pero estas
> ayudan a conformar nombres complejos como "first-name", al no tener
> las comillas nos lanzaria un error de Sintaxis.

> Se pueden conformar objetos anidados.

```javascript
      	        //definicion de un objeto literal
      			var empty_object={};
      
      			var stooge={
      				"first-name":"jerome",
      				"last-name": "Howard"
      			};
      
      			console.log("Valor obtenido con []: "+stooge["first-name"]);
      			console.log(stooge["third-name"]);
      
      
      			var persona4 = {
      		    	/* definiendo propiedades */
      		    	nombre : "adan",
      		    	edad   : 33,
      		   		 /* método simple */
      			    comer  : function(){
      			        return this.nombre + " esta comiendo.<br>";
      		    	},
      
      		    	dormir:function(){
      		    		document.writeln(this.nombre+" esta durmiendo<br>");
      		    	}
      			};
      			
      			/* accediendo al método comer de nuestro objeto literal persona */
                document.writeln(persona4.comer());
                persona4.dormir();
```



