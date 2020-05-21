# JS style-guide

## 1 Размещайте комментарий на новой строке.
Если комментарий находиться в блоке кода - добавьте перед ним пустую строку.
Плохо:

    const count = 42 // is current count
	
Хорошо:

    // is current count
    const count = 4

Плохо:

    function getUser(name) {
    // check user name
    	if(name === undefined){
    		return console.log('User is not found')
    	}
    return console.log(`User name is ${name}`)
    }

Хорошо:

    function getUser(name) {
    
    // check user name
	    if(name === undefined){
		    return console.log('User is not found');
	    }	
    return console.log(`User name is ${name}`)
    }
## 2 Используйте /** ... */ для многострочного комментария.
Плохо:

    //set default num
    //check num type
    //catch err if need
    //return func result

Хорошо:

    /**
    * set default num
    * check num type
    * catch err if need
    * return func result
    */
## 3 Используйте const для объявления переменных.
Избегайте объявления переменных через var.
Используйте let если переменная в процессе работы будет меняться.
Плохо:

    var a = 1
    var b = 2

Хорошо:

    const a = 1
    const b = 2
    
## 4 Группируйте все объявления const и let

Плохо:

    let i
    const items = getItems()
    let isReady
    const repalceItem = true
    let sum

Хорошо:

    const items = getItems()
    const repalceItem = true
    let i
    let isReady
    let sum
    
## 5. Используйте метод push для добавления нового элемента в массив.

Плохо:

    const someArr = [];
    someArr[someArr.length] = 'abc';

Хорошо:

    const someArr = [];
    someArr.push('abc');
    
## 6. Размещайте параметры со значением по умолчанию в конце.

Плохо:

    function doSomething(sum = 42, name) {...}
 
Хорошо:

    function doSomething(name, sum = 42) {...}

## 7. Не используйте в параметрах функции  "arguments"

Плохо:

    function doSomething(item, name, arguments) {...}

Хорошо:

    function doSomething(item, name, args) {...}

## 8. Используйте шаблон строк вместо конкатенации.

Плохо:

    function hello(name) {
	    return 'How are you, ' + name + '?'
    }

Хорошо:

    function hello(name) {
    return `How are you, ${name}?`
    }

## 9. Для создания объекта используйте литерал вместо конструктор

Плохо:

    const item = new Object()

Хорошо:

    const item = {}

## 10. Используйте сокращенную форму записи для методов объекта

//Плохо:

    const car = {
	    cost: 25
	    showCost: function (cost) {
	    consol.log(`Car cost = ${cost}`)
	    }
    }

  

Хорошо:

    const car = {
	    cost: 25
	    showCost(cost) {
	    consol.log(`Car cost = ${cost}`)
	    }
    }

